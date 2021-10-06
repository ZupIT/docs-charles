---
title: Configurando o chart template
weight: 37
description: Esta seção descreve como configurar o chart template no ambiente do Charles. 
---

---

# **O que é o Helm?**

O Helm Charts é um gerenciador de pacotes que permite você definir, instalar e atualizar as aplicações no Kubernetes, independente do grau de complexidade.  

## **Chart template no contexto do CharlesCD**

O [**Chart Template**](https://helm.sh/docs/chart_template_guide/getting_started/) é usado como uma coleção de arquivos relacionados a configurações do Kubernetes.

Os charts devem seguir o [**padrão do Helm**](https://helm.sh/docs/topics/charts/), e precisam estar contidos dentro de uma pasta com o nome da componente cadastrada no Charles. Você não precisa executar nenhum comando para empacotar o chart, o Charles faz o download dos arquivos e finaliza tudo automaticamente.  
  
Veja abaixo o exemplo de um repositório contendo o chart da componente **http-https-echo** no GitHub:

![](https://lh5.googleusercontent.com/Rt7_Lw1DbK152QKt3brsCYyzF0DAQ4wuoWsdCVyUaZjf9Hlh64EaK7YnHjF16W_xo2BQzlUJyUeUsooPzqwmMIKF7ttUXRej3eM56uWu6WH4QNCiByixeV4zEdHLwEGRq7NCruhH)

O módulo de deploy Butler utiliza charts helm para disponibilizar as suas aplicações no Cluster. Esses charts devem estar disponíveis em um repositório Github ou Gitlab e acessíveis por meio do token cadastrado na configuração de deployment. A URL deles é providenciada junto ao cadastro do módulo.

{{% alert color="info" %}}
Se você não tiver configurado o **seu módulo,** [**veja como fazer na seção: 'Criando seu primeiro módulo'**](/pt/primeiros-passos/criando-seu-primeiro-módulo/visao-geral/). É importante lembrar que você deve cadastrar a URL no módulo.
{{% /alert %}}

### **Templates**

O único requisito para que os templates funcionem com o Charles é que as **labels component** e **tag** estejam presentes nos manifestos do recurso Deployment. 

{{% alert color="info" %}}
Não é necessário inserir os valores no arquivo de _**values**_  do seu chart, o Charles irá provê-los automaticamente.
{{% /alert %}}

Veja o exemplo abaixo:

```text
component: {{ .Values.component }}
tag: {{ .Values.tag }}
```

Internamente o Butler armazena os charts compilados em entidades que representam cada solicitação de deploy. Desta forma, o Charles realiza rollbacks mais eficientes.  


# **Como configurar o chart template?** 

Siga os próximos passos para configurar o app de exemplo.

### **Passo 1: Crie um diretório do chart template**

Salve os seus templates na sua ferramenta de versionamento. Assim que você criar um novo chart template, você precisa nomear o diretório com o mesmo nome do componente ao qual ele se refere. 
A estrutura abaixo contém os templates necessários para fazer o deployment de um módulo que possui um componente chamado **“circles-sample”**.  O seu diretório precisa estar dessa forma:  

![ Diret&#xF3;rio de chart template do circle-sample](/shared/screen-shot-2020-08-13-at-09.16.04.png)

### **Passo 2: Configure os itens do diretório** 

Configure o diretório, veja abaixo quais arquivos são necessários para você configurar: 

1. **templates/ :** contém os modelos. 

  * **deployment.yaml:** descreve a estrutura de [**deployment**](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/).
  * **service.yaml:** descreve a estrutura do [**service**](https://kubernetes.io/docs/concepts/services-networking/service/). 

2. O arquivo **Chart.yaml** contém uma descrições como version, name, description. É necessário definir a version como **"darwin"**. 

3. O arquivo **circles-sample.yaml** possui os valores que serão utilizados nos nossos templates. 

Essas são as informações que o Charles precisa ter no templates, você também pode [**incrementar os templates**](https://github.com/ZupIT/charlescd/tree/main/samples/circles/circles-sample/templates) como quiser.

### **Passo 3: Adicione informações do Charles no seu template** 
O Charles sobrescreve alguns campos nos arquivos de [**Values do Helm**](https://helm.sh/docs/chart_template_guide/values_files/) que podem ser adicionados ao seu template. Veja abaixo:

- **"`.Values.tag`"**: A tag escolhida na hora de criar a release.
- **"`.Values.component`"**: O nome do componente selecionado para o deployment.
- **"`.Values.circleId`"**: ID do círculo em que o deploy foi realizado.
- **"`.Values.image.url`"**: URL completa da imagem em que o deployment irá acontecer.

Para mais informações de como criar seu próprio template, acesse [**alguns exemplos no repositório do Charles**](https://github.com/ZupIT/charlescd/tree/main/samples/circles/circles-sample/templates).

### **Passo 4:  Execute o comando `"helm package ."`** 
Depois que você configurou o diretório:
- Acesse a pasta "circles-sample";
- Execute o comando "`helm package .`".  

Depois disso, você terá uma arquivo **tgz**  com o nome de **circles-samples-darwin**. O Charles procura o **tgz** para executar o template. 

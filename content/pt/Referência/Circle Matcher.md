---
title: Circle Matcher
weight: 51
description: 'Nesta seção, você encontra detalhes sobre como funciona o Circle Matcher.'
---

---

O Circle Matcher é um recurso que permite você validar se os seus [**círculos**]({{< ref path="/Referência/Círculo.md" lang="pt">}}) estão com segmentações coerentes. Você também pode utilizá-lo em suas aplicações para determinar em qual círculo os seus usuários se encaixam.

{{% alert color="info" %}}
Uma boa prática é realizar essa identificação sempre que o usuário faz login na aplicação. Porém, isso pode ser alterado de acordo com a necessidade da sua regra de negócio.
{{% /alert %}}

Para mais informações de como configurar seu Circle Matcher em um workspace,[ **veja a seção Definindo um Workspace**]({{< ref path="/Primeiros Passos/Definindo um Workspace/Visao geral.md" lang="pt">}}).

### **Como é realizada a identificação de círculos?**

1. A aplicação realiza uma busca em toda a sua base de dados por círculos que tenham as mesmas regras informadas na requisição. 
2. Caso não haja um círculo compatível com as regras informadas cadastrado, o Circle Matcher verifica se o usuário irá ser selecionado pelos círculos com segmentação por porcentagem através de seu algoritmo que utiliza probabilidade na seleção.
3. Para finalizar, se nenhum círculo se encaixar, o Circle Matcher irá retornar o círculo default cadastrado.  

### Identificando círculos através do CharlesCD

Ao utilizar a interface é possível perceber que existe uma forma de realizar a identificação dos círculos. Para isto, acesse o menu **Circles** dentro de um **workspace** e selecione o ícone indicado abaixo:

![](/shared/circle-matcher%20%282%29.png)

Você adiciona manualmente chaves e valores que definem as características de um usuário de teste. E, com base nisso, ao executar o **Try**, você receberá todos os círculos que ele se encaixa.  

![](/shared/circle-matcher.gif)

{{% alert color="warning" %}}
Se você passar informações que estejam fora das condições lógicas configuradas nos círculos, o sistema irá retornar que aquele usuário está no círculo _Default_, ou seja, na versão padrão da sua aplicação.
{{% /alert %}}

## **Identificação de círculos por meio da API**

Você pode integrar nas suas aplicações o recurso **Identify** do módulo [`circle-matcher`](https://github.com/ZupIT/charlescd/tree/master/circle-matcher) para detectar os círculos que o seu usuário pertence.

Por exemplo, dada a utilização dos seguintes parâmetros ao segmentar:

![](/shared/circlematcher-identificacao-de-circulos-atraves-da-api.png)

Ao realizar a requisição de identificação com as seguintes informações, círculos compatíveis serão retornados.

#### `POST Identify` `https://api.charlescd-circle-matcher.com/identify` 

Esta requisição implanta a release composta criada anteriormente em um círculo.

### **Requisição**

**Body Parameters**: Todos obrigatórios:

| Key | Tipo | Descrição |
| :--- | :--- | :--- |
| requestData | object | { "state": "NY", "profession": "Lawyer", "age": 46, "city": "Stony Brook"  |
| workspaceId | String | UUID |


### **Resposta**
```text
{
  "circles": [
    {
      "id": "6577ae92-648c-11ea-bc55-0242ac130003",
      "name": "NY Lawyers"
    },
    {
      "id": "6577b112-648c-11ea-bc55-0242ac130003",
      "name": "Stony Brook's Citizens"
    }
  ]
}
```


Como nesse exemplo existem círculos correspondentes com as informações sobre o usuário, o **`charlescd-circle-matcher`**retorna uma lista com eles. Aqui, dois círculos se encaixaram: NY Lawyers e Stony Brook’s Citizens. A ordem de retorno dos círculos é feita pela data de criação, portanto o círculo mais recente será o primeiro da lista.

O corpo da requisição é totalmente flexível, porém vale lembrar que as chaves devem ter a mesma nomenclatura definida nas regras de segmentação do círculo. Veja no caso a seguir:

![](/shared/circle-matcher-stony-brooks-citizens.png)

O círculo **Stony Brook’s Citizens** foi criado para a identificar usuários que tenham como característica a chave **`city`** e o exato valor **`London`**. Sendo assim, ele não estará na listagem ao realizar uma requisição para o **`Identify`** caso seja informado o corpo da requisição como no exemplo abaixo:

#### `POST Identify` `https://api.charlescd-circle-matcher.com/identify` 

Esta requisição implanta a release composta criada anteriormente em um círculo.

### **Requisição**

**Body Parameters**: Todos obrigatórios:

| Key | Tipo | Descrição |
| :--- | :--- | :--- |
| requestData | object | { "age": 46, "city": "London" } |
| workspaceId | String | UUID |


### **Resposta**
```
{
  "circles": [
    {
      "id": "6577ae92-648c-11ea-bc55-0242ac130003",
      "name": "Default"
    }
  ]
}
```
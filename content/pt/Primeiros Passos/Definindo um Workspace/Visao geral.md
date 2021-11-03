---
title: Visão Geral
weight: 20
description: Nesta seção, você encontra como você deve configurar seu workspace dentro do Charles.
---

---

O workspace permite que você segmente o uso do CharlesCD dentro da sua empresa ou do seu time. Com ele se define as **permissões personalizadas dos usuários**, o que garante mais segurança para o seu projeto.

{{% alert color="info" %}}
Com apenas uma instalação, vários times podem utilizar o Charles com configurações distintas ou, se preferir, criar um workspace para representar diferentes ambientes de desenvolvimento como, por exemplo, homologação, produção, etc. 
{{% /alert %}}

### **Configurações do workspace**

Cada workspace possui as seguintes configurações:

* Definição dos acessos e [**permissões dos grupos de usuários**]({{< ref path="/Referência/Grupo de Usuários.md" lang="pt">}}).
* Cadastros de credenciais do [**Git**](https://github.com/), [**Docker Registry**]({{< ref path="/Primeiros Passos/Definindo um Workspace/Docker Registry.md" lang="pt">}}) e de [**Continuous Deployment \(CD\)**]({{< ref path="/Primeiros Passos/Definindo um Workspace/Ambiente de deploy.md" lang="pt">}}). 
* Personalização do [**Circle Matcher**]({{< ref path="/Referência/Circle Matcher.md" lang="pt">}}).
* Registro do [**Provedor de Métricas**]({{< ref path="/Primeiros Passos/Definindo um Workspace/Adicionando o Datasource.md" lang="pt">}})
 das suas aplicações.

![](/shared/defining-workspace.png)

{{% alert color="warning" %}}
A criação do workspace pode ser feita apenas pelo usuário **root**. Entretanto, o preenchimento das configurações podem também ser feitas pelos usuários associados ao workspace com perfil de **mantenedor**.
{{% /alert %}}

### **Como obter o identificador do meu workspace?**

Assim que seu workspace é criado, mesmo sem a definição das configurações, ele já possui um identificador único. 

Para obter essa informação, selecione o workspace desejado e, no menu à esquerda, clique em **Copy ID**:

![](/shared/workspace_copyid%20%281%29.gif)

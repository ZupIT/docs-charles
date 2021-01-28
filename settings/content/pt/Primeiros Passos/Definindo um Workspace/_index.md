---
title: Definindo um Workspace
weight: 22
description: Esta seção descreve como você deve configurar seu workspace dentro do Charles.
---

---

O workspace permite que você segmente o uso do CharlesCD dentro da sua empresa ou do seu time. Com ele se define as **permissões personalizadas dos usuários**, o que garante mais segurança para o seu projeto.

{{% alert color="info" %}}
Com apenas uma instalação, vários times podem utilizar o Charles com configurações distintas ou, se preferir, criar um workspace para representar diferentes ambientes de desenvolvimento como, por exemplo, homologação, produção, etc. 
{{% /alert %}}

### Configurações do workspace

Cada workspace possui as seguintes configurações:

* Definição dos acessos e [**permissões dos grupos de usuários**.](../../../../../referencia/grupos-de-usuarios#permissoes-para-o-grupo-de-usuarios-no-workspace)
* Cadastros de credenciais do [**Git**](credenciais-do-git)**,** [**Docker Registry**](docker-registry) e de [**Continuous Deployment \(CD\)**](../../../../referencia/configuracao-cd).
* Personalização do [**Circle Matcher**](../../../referencia/circle-matcher).
* Registro do [**Provedor de Métricas**](adicionando-o-datasource) das suas aplicações.

![Configura&#xE7;&#xF5;es do workspace](/ docs-charles/settings_-_workspace_-_11.4_-_add_group_permissions2x.png)

{{% alert color="warning" %}}
A criação do workspace pode ser feita apenas pelo usuário **root**. Entretanto, o preenchimento das configurações podem também ser feitas pelos usuários associados ao workspace com perfil de **mantenedor**.
{{% /alert %}}

### Como obter o identificador do meu workspace?

Assim que seu workspace é criado, mesmo sem a definição das configurações, ele já possui um identificador único. 

Para obter essa informação, selecione o workspace desejado e, no menu à esquerda, clique em **Copy ID**:

![](/ docs-charles/workspaceid.gif)

---
title: Ambiente de deploy
weight: 10
description: >-
  Nesta seção, você vai encontrar mais informações sobre ambiente de deploy.
---

---

Ao configurar seu workspace é preciso cadastrar as credenciais de acesso ao cluster [**Kubernetes**](https://kubernetes.io/). Essas configurações são específicas para cada uma das ferramentas de _Continuous Deployment_ \(CD\) que são integradas ao CharlesCD. No momento, damos suporte ao  [**Spinnaker**](https://www.spinnaker.io/) e _Octopipe_. 

{{% alert color="info" %}}
O **Octopipe** foi desenvolvido pela equipe do Charles. É mais leve, de baixo custo e consegue fazer deploys em clusters Kubernetes.
{{% /alert %}}

Segue abaixo o exemplo de como realizar seu deploy utilizando o _Octopipe_ no mesmo cluster de instalação:

1. Clique em **Add CD Configuration**;
2. Selecione a opção **Octopipe.**

Após esses passos, preencha os campos a seguir:

1. **Name:** nome da configuração que será criada.
2. **Namespace:** defina o namespace que será utilizado nos deploys no cluster _Kubernetes._
3. **Git provider**: defina o provedor de git a ser utilizado \(**GitHub ou GitLab**\).
4. **Git token:** insira o token de autenticação para o seu repositório git. Este será utilizado para a obtenção dos templates Helm que são definidos ao cadastrar os seus [**módulos**](/pt/primeiros-passos/criando-seu-primeiro-módulo/).
5. Selecione a opção **Default**.

Depois de finalizar sua configuração, você pode futuramente associá-la a um módulo. Para mais informações, acesse [**Configurações de CD**](/pt/referência/configuração-de-cd/).

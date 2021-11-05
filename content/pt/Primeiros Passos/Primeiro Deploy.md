---
title: Primeiro Deploy
weight: 42
description: >-
  Nesta seção, você encontra os passos para realizar o seu primeiro deploy
  utilizando o Charles.
---

---

{{% alert color="info" %}}
Após criar o seu primeiro [**módulo**]({{< ref path="/Primeiros Passos/Definindo um Workspace/Visao geral.md" lang="pt">}}) e cadastrar as [**credenciais do seu cluster**,]
({{< ref path="/Primeiros Passos/Definindo um Workspace/Ambiente de deploy.md" lang="pt">}}) você completou todos os passos de configuração necessários para a realização do seu primeiro deploy. 

Agora, é necessário criar uma [**release**]({{< ref path="/Referência/Release.md" lang="pt">}}) e disponibilizá-la no cluster configurado.
{{% /alert %}}

### **Como fazer o primeiro deploy?**

No CharlesCD, é preciso utilizar imagens de containers já disponíveis no [**registry** ](/pt/primeiros-passos/definindo-um-workspace/docker-registry/) configurado para criar uma release. 

Para fazer seu primeiro deploy, siga os passos abaixo:

1. Acesse a área "**Círculos**" **\(Circles\)**;
2. S Selecione um [**círculo**]({{< ref path="/Referência/Círculo.md" lang="pt">}}). Caso você não tenha criado um ainda, a opção que irá aparecer é a do **círculo default** para que seja possível você realizar o  primeiro deploy;
3. Altere o filtro do círculo de ativo para **inativo;** 
4. Selecione a opção "**Insert a release**";
5. Depois selecione "**Create a release**" e preencha os campos: 
   1. **'Release name':** escolha um nome para a sua release;
   2. **'Select a module':** selecione um módulo;
   3. **'Select a component':** selecione um componente;
   4. '**Version name**': digite o nome da tag \(é necessário ser o mesmo  nome que aparece cadastrado em seu Registry\).

5 . Clique no botão "**Deploy**" e aguarde o status no card verde. Enquanto estiver em processo, irá aparecer "**deploying**", mas ao final irá aparecer "**deployed**".

{{% alert color="success" %}}
Depois que você realizou o processo acima, sua release está pronta para o deploy!
{{% /alert %}}

### **Deploy em mar aberto**

O **deploy em** [**mar aberto**]({{< ref path="/Principais Conceitos.md" lang="pt">}}) é aquele em que você envia sua aplicação para toda segmentação cadastrada no Charles. 

Para realizar o deploy neste caso, siga os passos abaixo:

1. Na tela inicial do Charles, clique em **Circles**;
2. Clique no círculo **Default** \(Este representa o mar aberto\);
3. Clique em **Override release** no canto direito superior;
4. Clique em **Search for ready releases**;
5. Digite o nome da release criada nos passos acima \(ou os reproduza novamente com uma nova versão\), a selecione e clique em **Deploy.**

Depois disso, o Charles se encarregará de disponibilizar a release criada no cluster configurado em mar aberto. O status do deploy será exibido e atualizado conforme o progresso.

![](/shared/first-deploy.gif)

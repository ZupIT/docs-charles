---
title: Instalando via Helm
weight: 6
description: 'Nesta seção, você encontra como instalar o Charles via Helm.'
---

---

{{% alert color="warning" %}}
Antes de prosseguir, tenha certeza de que todos os [**pré-requisitos**](/pt/primeiros-passos/instalando-o-charles/visão-geral/) estão devidamente instalados.
{{% /alert %}}

## **Como instalar?**

Esta instalação é customizável, para você instalar acesse um **template helm** com todos os campos disponíveis para alteração, incluindo os de banco de dados e recursos consumidos. Veja a [**documentação dos campos editáveis**](https://github.com/ZupIT/charlescd/tree/master/install/helm-chart) 

{{% alert color="info" %}}
As senhas utilizadas pelo Charles estão armazenadas no arquivo [**values.yaml**](https://github.com/ZupIT/charlescd/blob/main/install/helm-chart/values.yaml) As principais senhas para personalizar são:

* CharlesApplications.butler.database.password
* CharlesApplications.moove.database.password 
* CharlesApplications.villager.database.password
* CharlesApplications.circlematcher.redis.password
* CharlesApplications.keycloak.keycloak.extraEnv.DB_PASSWORD
* CharlesApplications.postgresql.postgresqlPassword
* CharlesApplications.redis.password
* CharlesApplications.compass.database.password
* CharlesApplications.hermes.database.password
* CharlesApplications.rabbitmq.auth.password
* CharlesApplications.gate.database.password
* CharlesApplications.compass.moove.database.password

Para mais detalhes, acesse os [**campos editáveis**](https://github.com/ZupIT/charlescd/tree/master/install/helm-chart).
{{% /alert %}}

- Para garantir que as dependências dos charts estão presentes e atualizadas com uma versão compatível, utilize dentro da pasta **`/charlescd/install/helm-chart`** o comando abaixo:

```
helm dependency update
```

- Para instalar com Helm Charts, depois que você customizou os campos, execute o comando abaixo dentro da pasta **`/charlescd/install/helm-chart`**: 

```
helm install --create-namespace -n <namespace> charlescd . -f values.yaml
```

{{% alert color="warning" %}}
Se você não fizer nenhuma customização, por padrão o Charles instala o **PostgreSQL**, **Redis**, **Keycloak** e **RabbitMQ**.  Por isso, não deixe de customizar os campos se você precisa de algo gerenciável. 
{{% /alert %}}

### **Troque a senha padrão \(default password\)** 

Depois de instalar o CharlesCD, troque algumas **senhas padrão**, veja abaixo: 

- **Senha do Keycloak**:   
**1.** Acesse: **http://&lt;charlescd-url&gt;/keycloak/auth;**  
**2.** Clique em **Administration Console;**   
**3.**  Insira a senha do usuário do Keycloak \(admin - firstpassword\) e troque a senha padrão.

- **Senha do CharlesCD:**  
Acesse o CharlesCD e logue com  
**1. Usuário:** charlesadmin@admin; 
**2. Senha**: charlesadmin;  
**3.** Vá até **Account &gt; Profile** e depois em **Change Password** e escolha sua nova senha.
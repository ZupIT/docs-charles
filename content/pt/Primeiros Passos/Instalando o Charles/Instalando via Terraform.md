---
title: Instalando via Terraform
weight: 6
description: 'Nesta seção, você encontra como instalar o Charles no seu ambiente local via Terraform.'
---

---

# **Como fazer o deploy do CharlesCD no Kubernetes com o Terraform**

{{% alert color="warning" %}}
Para essa instalação não é necessário o `kubectl`, mas sem ele, você não poderá realizar alguns exemplos na nossa documentação. Se você quiser instalar, acesse a [**docs de instalação.**](https://kubernetes.io/docs/tasks/tools/install-kubectl/).
{{% /alert %}}


## **Requisitos**

Veja o que você precisa instalar na sua máquina: 
- [**Docker**](https://docs.docker.com/get-docker/)
- [**Terraform**](https://www.terraform.io/downloads.html)


### **Como instalar?**
Siga os passos abaixo:  

**Step 1** Faça o download no repositório [**`charlescd-local-cluster`**](https://github.com/ZupIT/charlescd-local-cluster). Na pasta **charles-local-cluster**, rode o comando: 

```
make up
```

**Step 2** Acesse o [**http://charles.lvh.me/**](http://charles.lvh.me/ ) no seu navegador e faça o login com: 
- Usuário: **`charlesadmin@admin`** 
- Senha: `g_wl!U8Uyf2)$KKw` 

Agora você pode usar o CharlesCD!
---
title: Installing via Terraform
weight: 6
description: 'In this section, you will find how to install Charles via Terraform in your local environment.'
---

---

# **Deploying CharlesCD on Kubernetes with Terraform**

{{% alert color="warning" %}}
This installation does not require `kubectl`, but you can't perform some of the examples in our documentation without it. If you want to install it, check out the [**installation docs**](https://kubernetes.io/docs/tasks/tools/install-kubectl/).
{{% /alert %}}


## **Requirements**

See below what you need in your machine: 
- [**Docker**](https://docs.docker.com/get-docker/)
- [**Terraform**](https://www.terraform.io/downloads.html)


### **How to install?**
Follow the steps below: 

**Step 1** Download at  [**`charlescd-local-cluster`**](https://github.com/ZupIT/charlescd-local-cluster) repository. From **charles-local-cluster** folder run:

```
make up
```

**Step 2** Access [**http://charles.lvh.me/**](http://charles.lvh.me/ ) on your browser and log in with:
- User: **`charlesadmin@admin`** 
- Password: `g_wl!U8Uyf2)$KKw` 

Now you can start to play with CharlesCD!
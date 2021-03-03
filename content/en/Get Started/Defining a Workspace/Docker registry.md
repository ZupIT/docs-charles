---
title: Docker registry
weight: 24
---

---

{{% alert color="warning" %}}
This is mandatory information.
{{% /alert %}}

One of the steps to configure your workspace is to inform Charles which docker registry you store your application's images. This access is important because CharlesCD can watch newly generated images and list the ones already saved in your registry to deploy them in circles.

Charles is already integrated with some docker registries, choose one and add the information:

* [**Azure Container Registry;**](/docs-charles/reference/registry/azure-container-registry/)

- [**Docker Hub;**](/docs-charles/reference/registry/docker-hub/) 

-  [**ECR**;](/docs-charles/reference/registry/ecr/)

* [**GCR**.](/docs-charles/reference/registry/gcr/)

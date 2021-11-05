---
title: Configurando sua ingress
weight: 15
description: 'Nesta seção, você encontra sobre como configurar a sua ingress.'
---

---

Caso você queira utilizar sua ingress, ao invés da que possui na instalação do Charles, siga o seguinte passo:

* em **`charlescd/install/helm-chart/values.yaml`**, nas configurações de ingress, mude o valor de **`enabled`** para **`true`** como no exemplo abaixo:

```text
ingress:
  enabled: true
  host: charles.info.example
  class: nginx

```

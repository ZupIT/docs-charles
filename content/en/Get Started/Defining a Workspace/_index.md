---
title: Defining a Workspace
weight: 6
---

---

The workspace allows you to segment CharlesCD's use in your team, defining **personalized users permissions** that will assure safety to your project.

{{% alert color="info" %}}
You need only one installation, and the teams will be able to use Charles with different configurations, or you may create a workspace to represent different development environments, such as staging, production, etc.
{{% /alert %}}

Each workspace has the following configuration:

* Access control and **user groups permissions**;
* Register on [**Docker Registry**](docker-registry), [**Git**](github) **and** [**Continuous Deployment \(CD\)**;](../../../../../reference/cd-configuration)
* Customize the [**Circle Matcher**](../../../../reference/circle-matcher);
* Register your applications [**metrics provider**](../../../reference/metrics/register-metrics-provider). 

{{% alert color="warning" %}}
The **root** user gives you the permission to create a workspace. However, users with **mantainer** profile are able to configure with the necessary information as well.
{{% /alert %}}

### How to get an identifier on my workspace?  <a id="como-obter-o-identificador-do-meu-workspace"></a>

Once your workspace is created, even without the configuration definitions**,** it already has a single identifier. 

To get this information, select the workspace you want and then on the left menu, click on **Copy ID.**

![](//workspaceid%20%282%29.gif)

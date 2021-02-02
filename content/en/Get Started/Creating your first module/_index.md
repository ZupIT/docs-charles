---
title: Creating your first module
weight: 37
---

---

After creating and configuring your workspace, it is necessary to add the modules.

{{% alert color="info" %}}
A **module** is your application stored in a [**Git repository previously registered**](/docs-charles/get-started/defining-a-workspace/_index2/).
{{% /alert %}}

To add it, access the **Modules** menu on your workspace and set the following properties:

* **Name**: this field should be the junction of the organization and the module names, as it is in your git. For example: `ZupIt/charlescd`.
* **Git URL**: your repository's URL. For example: [https://github.com/ZupIT/charlescd](https://github.com/ZupIT/charlescd).
* **Helm repository URL:**  your repository where the helm template of your application it is in. 

{{% alert color="info" %}}
For more information about Helm Repository, [**access here**](/docs-charles/get-started/creating-your-first-module/how-to-configure-chart-template/). 
{{% /alert %}}

If you have a lot of applications on your repository, register them with the components and add the following:

* **Name**: application's name, the same on your repository;
* **Metrics**: latency \(ms\) and HTTP error \(%\). Both cases you must add a risk value that you want to receive an alert if your component reaches the rate. 

In both cases, you need to inform the minimum risk value you'd like to be alerted.

![Creating a module screen](/docs-charles/criac-a-o-de-modulo%20%282%29%20%281%29.png)

## **Components**

{{% alert color="info" %}}
Components are abstractions of the applications. If in your repository there are many applications, every component will match one of them.
{{% /alert %}}

### **Health metrics**

For every component, it is possible to register metrics for health analysis: **latency** \(ms\) and **HTTP error** \(%\). When the limits are reached, or at least 10%, you will receive an alert that will show your application status on the circle that may have an issue.

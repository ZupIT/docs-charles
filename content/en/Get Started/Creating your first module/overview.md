---
title: Overview
weight: 35
description: In this section, you will find more how to create your modules.
---

---

After creating and configuring your workspace, it is necessary to add the modules.

{{% alert color="info" %}}
A **module** is your application stored in a [**Git repository previously registered**](https://docs.charlescd.io/get-started/defining-a-workspace).
{{% /alert %}}

To add it, access the **Modules** menu on your workspace and set the following properties:

* **Name**: This field should be the junction of the organization and the module names, as it is in your git. For example: `ZupIt/charlescd`.
* **Git URL**: Your repository's URL. For example: [https://github.com/ZupIT/charlescd](https://github.com/ZupIT/charlescd).
* **Helm repository URL:**  your repository where the helm template of your application is in. 

{{% alert color="info" %}}
For more information about Helm Repository, [**access here**](how-to-configure-chart-template). 
{{% /alert %}}

If you have a lot of applications on your repository, register them with the components and add the following:

* **Name**: application's name, the same on your repository;
* **Metrics**: latency \(ms\) and HTTP error \(%\). In both cases, you must add a risk value that you want to receive an alert if your component reaches the rate. 

In both cases, you need to inform the minimum risk value you'd like to be alerted.

![](/shared/image%20%2813%29.png)

## Components

{{% alert color="info" %}}
Components are abstractions of the applications. If in your repository there are many applications, every component will match one of them.
{{% /alert %}}

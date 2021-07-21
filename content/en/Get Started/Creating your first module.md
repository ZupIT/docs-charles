---
title: Creating your first module
weight: 15
description: >-
  In this section, you will find more information on how to create your first module. 
---

---

After creating and configuring your workspace, it is necessary to add the modules.

{{% alert color="info" %}}
A **module** is your application stored in a [**Git repository previously registered**](defining-a-workspace/github).
{{% /alert %}}

To add it, access the **Modules** menu on your workspace and set the following properties:

* **Name**: the module name must be exactly your repository name; 
* **Git URL**: your repository's URL. For example: [https://github.com/ZupIT/charlescd](https://github.com/ZupIT/charlescd).

If you have a lot of applications on your repository, register them with the components and add the following:

* **Name**: application's name, the same on your repository;
* **Metrics**: latency \(ms\) and HTTP error \(%\). Both cases you must add a risk value that you want to receive an alert if your component reaches the rate. 

In both cases, you need to inform the minimum risk value you'd like to be alerted.

![Creating a module screen](/shared/criac-a-o-de-modulo%20%282%29%20%281%29.png)

## Components

{{% alert color="info" %}}
Components are abstractions of the applications. If in your repository there are many applications, every component will match each one of them.
{{% /alert %}}

### Health metrics

For every component, it is possible to register metrics for health analysis: **latency** \(ms\) and **HTTP error** \(%\). When the limits are reached, or at least 10%, you will receive an alert that will show your application status on the circle that may have an issue.

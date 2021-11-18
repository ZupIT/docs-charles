---
title: Circle Matcher
weight: 26
description: 'In this section, you will find information about the circle matcher.'
---

---

## **Why do you have to configure it?**

When [**creating a workspace**]({{< ref path="/Get Started/Defining a Workspace/Overview.md" lang="en">}}), you have to inform Charles to which Circle Matcher that current workspace will point to. It is possible to have a Circle Matcher for each environment since Charles can handle different environments at the same time in multiple workspaces.

Circle Matcher is an independent module, despite that, it is possible to install it in any area you want inside its architecture, for example, a public cluster.

This configuration is necessary, so you are able to perform operations in Charles, like creating and editing segments in a circle.

{{% alert color="info" %}}
It is important to remember, in Charle's context, the Circle Matcher module receives most of the environment's requests because it is the application that identifies the user based on the rules that you have configured while managing a circle.
{{% /alert %}}

If you want to know more about **Circle Matcher**, check out the [**Reference section**]({{< ref path="/Reference/Circle Matcher.md">}}). 

## **How must be configured?**

#### **Option 1: Configure Circle Matcher in a separate architecture**

You have to configure the public DNS that points to your desired Circle Matcher.

> Example: **http://charles.info.example/charlescd-circle-matcher**.



#### **Option 2: Configure Circle Matcher in the same Charles' namespace**  

If you want to use Circle Matcher in the same namespace that Charles is installed, you can use the same DNS reference.

The difference is in terms of performance, it is recommended to use Kubernetes service name.

> Example: **http://charlescd-circle-matcher:8080**.

## Next steps

Continue your workspace configuration, Charles offers metrics that need to be configured. 
- Go to [**Setting up your metrics**]({{< ref path="/Reference/Metrics/Setting up your metrics.md" lang="en">}}) and find out how Charles uses metrics.
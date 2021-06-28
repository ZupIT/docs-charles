---
title: Metrics group
weight: 78
description: >-
  In this section, you will find more information about how to use the metrics
  group on Charles.
---

---

The metrics group is a functionality that allows you to register and organize any kind of metrics in a group inside your application. These metrics are related to the [**data source you previously registered**](../../../get-started/defining-a-workspace/datasource) 

## **How to create?**

To create your metrics group, follow the next steps: 

     **Step 1:**  Go to the **"Circles"** section, on the left menu and choose the circle  you want to create a new metric group;

     **Step 2:** In **'Add metrics group'**, type the name you want for your group and click on **'Add group'**: 

![](//criacaogroup%20%281%29.gif)

Now you are able to register your metrics**:**

   **Step 3**: Click on '**Add metric'**  and put the metrics name you want; 

   **Step 4:** Click on **'Select a Datasource':** select your metrics Datasource already registered;

  **Step 5:** Click on **Metric:**  **Choose one** and use the **Filter** option to customize with the value and the conditional you need.  Here is where your Datasource will return the metrics. 

See the example below: 

![](//metric+filter%20%281%29.gif)

   **Step 6:** Define a **Threshold** to establish a limit to your metric. 

{{% alert color="info" %}}
**Thresholds** are predetermined limits that you can configure in Charles. It informs you when one of them reaches the goal.

For example, if you want to know if your application hits 50 errors, just customize the **threshold** and you will be notified when you hit this metric. 
{{% /alert %}}

![](//threshold%20%281%29.gif)

{{% alert color="success" %}}
Done! You have registered your metrics group.
{{% /alert %}}

Now, you can follow up the result with graphics and the available information, as you can see below: 

![](//graficos%20%281%29.gif)

## **Metrics group: Advanced**

You can customize your own metric with the metrics' group advanced function. This option is for users that already have the knowledge to do queries in the Datasource they are using, it also gives them the power to create any metric possible using that tool.

Check out the example below, it shows where to use **PromQL** to build queries in Prometheus, creating a new metric type: 

![](//advanced%20%281%29.png)

{{% alert color="info" %}}
To see more examples of the advanced mode, check out [**this section**](metric-groups-to-health-monitoring)
{{% /alert %}}

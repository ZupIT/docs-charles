---
title: Metrics group
weight: 74
description: >-
  In this section, you will find more information about how to use the metrics
  group on Charles.
---

---

The metrics group is a functionality that allows you to register and organize any kind of metrics in a group inside your application. These metrics are related to the [**provider you previously registered.** ](/reference/circles/)

### **How to create?**

To create your metrics group, follow the next steps: 

1. In **add metrics group**, type the name you want for your group and click on **add group**: 

![](/shared/criacaogroup%20%281%29.gif)

After you have created your group, now you are able to register your metrics.

   2 Click on **Add metric**  and put the metrics name you want; 

  3. In **select a data source**, select your metrics provider already registered;

 4. **Metric** is the field where your provider will return the metrics, choose one, and after that use the **Filter** option to customize with the value and the conditional you need. 

See the example below: 

![](/shared/metric+filter%20%281%29.gif)

5.  After that, define a **Threshold** to establish a limit to your metric. 

For example, if you want to know if your application hits 50 errors, just customize the **threshold** and you will be notified when you hit this metric. 

![](/shared/threshold%20%281%29.gif)

{{% alert color="success" %}}
Done! You have registered your metrics group.
{{% /alert %}}

Now, you can follow up the result with graphics and the available information, as you can see below: 

![](/shared/graficos%20%281%29.gif)

### **Metrics group: Advanced**

There is an **advanced** function inside the metrics group, you can customize your own metric, like for example, a database query, or specifically according to what you need.

See the example below: 

![](/shared/advanced%20%281%29.png)

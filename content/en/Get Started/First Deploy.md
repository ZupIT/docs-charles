---
title: First Deploy
weight: 42
description: 'In this section, you will find how to make your first deployment.'
---

---

{{% alert color="info" %}}
After you have created your first [**module**]({{< ref path="/Get Started/Creating your first module/Overview.md" lang="en">}}) and registered your [**cluster crendentials**]({{< ref path="/Get Started/Defining a Workspace/Docker registry.md" lang="en">}}) you have finished all the steps needed to make your first deployment.

Now, it is necessary to create a [**release**]({{< ref path="/Reference/Releases.md" lang="en">}}) and provide it on the configured cluster.
{{% /alert %}}

### **How to make the first deployment?** 

On Charles you have to use container images already available in your configured [**registry**](/reference/registry/) to create a release.

To make your first deployment, follow the steps below: 

1. Go to **Circles** area;
2. Select a [**circle**]({{< ref path="/Reference/Circles.md" lang="en">}}). If you haven't created one yet, there is a **default circle** option that makes your first deploy possible; 
3. Change the active circle filter to **inactive**;
4. Select the "**Insert a release**" option;
5. After that, select "**Create a release**" and fill the fields: 
   * **'Release name':** choose a name for your release;
   * **'Select a module';**
   * **Select a component';**
   * **Version name**': type the name of your tag \(it is necessary to be the same one shown in your Registry\). 

5 . Click on '**Deploy**' button and wait for a status on the green card. When processing, you will see "**deploying**", but at the end, it will show up as "**deployed**".

{{% alert color="success" %}}
After the process above, your release is ready to deploy. 
{{% /alert %}}

### **Open Sea deploy**

The [**open sea**]({{< ref path="/Key concepts.md" lang="en">}}) deployment is where you send your application to the registered segmentation on Charles.

Now, follow the next steps to the [**open sea**]({{< ref path="/Key concepts.md" lang="en">}}) deploy:

1. On Charles homepage, click on **Circles**; 
2. Click on the Default circle \(it represents the open sea\) 
3. Click on **Override release** in upper right corner; 
4. Click on **Search for ready releases**;
5. Type the release name created above \(or use it again with a new version\) and click on **Deploy**.

Finally, Charles will provide the created release on a cluster in the Open Sea. The deploy status will be shown and updated along the process.

![](/shared/first-deploy%20%281%29.gif)

### **Incremental deploy**

The incremental deployment allows you to use the previous deployments and add them to the actual one. For example, you already made a Beagle deployment and now you want to do a Ritchie one, you will see both of them in your current circle status.  

{{% alert color="warning" %}}
If you don't choose the incremental deployment (choose override release, for example) what has been deployed before in your circle will be removed and it will remain only the current deployment. 
{{% /alert %}}

To make an incremental deployment, follow the steps below:

1. On Charles homepage, click on  **Circles**;
2. Click on **Default circle**;
3. Click on  **Incremental Deployment** on the left corner;
4. Clique em **Search for ready releases**;
5. Type your release name created in the previous steps  (or you can reproduce again with a new version), select, and click on **Deploy**.

Check out below: 

![](/shared/deploy-incremental.gif)
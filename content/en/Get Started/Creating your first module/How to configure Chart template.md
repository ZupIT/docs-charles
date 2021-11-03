---
title: How to configure Chart template
weight: 37
description: 'In this section, you will find how to configure chart template.'
---

---

## **What is Helm?**

Helm Charts is a package manager that allows you to define, install and update Kubernetes applications, regardless of the complexity.

## **Charts template in CharlesCD context**
[**Chart Template**](https://helm.sh/docs/chart_template_guide/getting_started/) is used like a file collection related to the Kubernetes configuration.

The charts must follow the [**Helm pattern**](https://helm.sh/docs/topics/charts/) and they need to be contained in a folder with the registered component on Charles. You don't need to run any command to bundle the chart, Charles downloads and it finishes automatically.   
  
See the below an example of a repository containing the component's chart  **http-https-echo** on GitHub:

![](https://lh5.googleusercontent.com/Rt7_Lw1DbK152QKt3brsCYyzF0DAQ4wuoWsdCVyUaZjf9Hlh64EaK7YnHjF16W_xo2BQzlUJyUeUsooPzqwmMIKF7ttUXRej3eM56uWu6WH4QNCiByixeV4zEdHLwEGRq7NCruhH)

The deployment module Butler uses helm charts to make your application available in the cluster.  These charts must be available in a Github or Gitlab repository and accessible through a token, previously registered in the deployment configuration. The URL is provided along with the module registration. 

{{% alert color="info" %}}
If you haven't configured your module yet, [**see how to do it in the 'Creating your module' section**]({{< ref path="/Get Started/Creating your first module/How to configure Chart template.md" lang="en">}}). It is important to remember, you have to register the URL in this module. 
{{% /alert %}}

### **Templates**

The only requirements for templates to work with Charles are **labels component** and **tag** to be present in the Deployment resource manifests. 

{{% alert color="info" %}}
It is not necessary to insert the values in the _**values**_ files of your chart, Charles will provide them. 
{{% /alert %}}

See the example below: 

```text
component: {{ .Values.component }}
tag: {{ .Values.tag }}
```

Butler internally stores the compiled charts in entities that represent each deployment request. Thereby, Charles can perform more efficient rollbacks.


# **How to configure the chart template?** 

Follow the next steps to try out our sample app.

### **Step 1: Create a chart template directory**

Save your templates in your versioning tool. When you create a new chart template, you need to name the directory with the same component's name it refers to. 

The structure below has the necessary templates to deploy a module that contains a component called **"circles-sample"**, your directory needs to look like this: 

![ Diret&#xF3;rio de chart template do circle-sample](/shared/screen-shot-2020-08-13-at-09.16.04.png)

### **Step 2: Configure the directory's items** 

After you have created the directory, now you have to configure it. See below the files you need to configure: 

1. **templates/:** It has the models.
    * **deployment.yaml:** Describes the [**deployment**](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) structure.
    * **service.yaml:** Describes the [**service**](https://kubernetes.io/docs/concepts/services-networking/service/) structure. 

2. The **Chart.yaml** file contains the descriptions like version, name, description. It is necessary to define the version as **"darwin"**. 

3. The **circles-sample.yaml** file has the values that will be used in the templates. 

These are the information Charles needs to have on the templates, you can [**customize them**](https://github.com/ZupIT/charlescd/tree/main/samples/circles/circles-sample/templates) if you want to.  

### **Step 3: Add Charles' information to your template** 
Charles overwrites some [**Helm Values**](https://helm.sh/docs/chart_template_guide/values_files/) file fields, you can add them to your template. Check out below: 

- **"`.Values.tag`"**: A tag you choose when creating arelease.
- **"`.Values.component`"**: Component's name for the deployment.
- **"`.Values.circleId`"**: Circles ID where the deployment was made. 
- **"`.Values.image.url`"**: Image's URL where the deployment will happen.

For more information on how to create your own template, [**access Charles' repository examples**](https://github.com/ZupIT/charlescd/tree/main/samples/circles/circles-sample/templates).

### **Step 4:  Run the `"helm package ."` command** 

After you have configured your directory:
- Access the **"circles-sample"** folder;;
- Execute o comando "`helm package .`".  

After that, you will have a **tgz** file with the **circles-samples-darwin** name. Charles looks for the **tgz** to execute the template.
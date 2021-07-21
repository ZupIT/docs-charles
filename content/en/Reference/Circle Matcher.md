---
title: Circle Matcher
weight: 49
description: >-
  In this section, you will find more information about how Circle Matcher works
  on Charles.
---

---

Circle Matcher is a resource that allows you to validate if your [**circles**](/reference/circles/) are incoherent segmentations. You can also use it in your applications to determine in which circle your users fit better.

{{% alert color="info" %}}
One good practice is to always make this identification when a user logs in to the application. However, this can be changed according to your business needs.
{{% /alert %}}

For more information on how to configure your **Circle Matcher in a workspace**, [**see Defining Workspace section**](/get-started/defining-a-workspace/circle-matcher/) 

## Identifying circles through CharlesCD

Once you start using the interface, it's possible to notice that there are two ways to perform the circle identification. For that, access the **Circles** menu inside a **workspace** and select the icon indicated below:

![](/shared/image%20%2816%29.png)

You can make the validation as shown bellow:

* In this option, you add manually keys and values to define the characteristics of a user test. Based on that, once you run the **Try**, **you will receive all the circles related to this user.**  

![](/shared/circle_matcher.gif)

{{% alert color="warning" %}}
If you pass some information that is off the preconfigured logic conditions in the circles, the system will return indicating that the user is on _Default_ circle, on the standard version of your application.
{{% /alert %}}

## Circle identification through API

You can integrate with your applications the **Identify** resource on the [`charles-circle-matcher`](https://github.com/ZupIT/charlescd/tree/master/circle-matcher) module to detect the circles the user belongs to.

For example, considering the use of the parameters below to segment:

![](/shared/image%20%2817%29.png)

Once you send the identification request with some information, compatible circles will be returned.

#### `POST Identify` `https://api.charlescd-circle-matcher.com/identify` 

This request used to identify circles based on the user's characteristicsEsta requisição implanta a release composta criada anteriormente em um círculo.

### **Request**

**Body Parameters**: All required:

| Key | Type | Description |
| :--- | :--- | :--- |
| requestData | object | { "state": "NY", "profession": "Lawyer", "age": 46, "city": "Stony Brook"  |
| workspaceId | String | UUID |


### **Response**
```text
{
  "circles": [
    {
      "id": "6577ae92-648c-11ea-bc55-0242ac130003",
      "name": "NY Lawyers"
    },
    {
      "id": "6577b112-648c-11ea-bc55-0242ac130003",
      "name": "Stony Brook's Citizens"
    }
  ]
}
```


As the example above shows, there are circles with the given information of the user, which means that **`charlescd-circle-matcher`** will return a list with all the circles. Here, there are two circles that fit with this description: NY Lawyers e Stony Brook’s Citizens. The order of the circles returned will be by the date of creation, so the newest circle created will be the first of the list.
The requisition body is totally flexible, but it's good to remember that the keys must have the same nomenclature defined by segmentation's rules of the circle. 

![](/shared/circle-matcher-stony-brooks-citizens.png)

The Stony Brook’s Citizens circle was created to identify users that contain as one of its characteristics the key city and the exact value London. That means that this user won't be listed if you send a request to Identify and inform on the request body the information presented on the example below:

#### `POST Identify` `https://api.charlescd-circle-matcher.com/identify` 

This request implants the release created before in a circle. 

### **Request**

**Body Parameters**: All required:

| Key | Type | Description |
| :--- | :--- | :--- |
| requestData | object | { "age": 46, "city": "London" } |
| workspaceId | String | UUID |


### **Response**
```
{
  "circles": [
    {
      "id": "6577ae92-648c-11ea-bc55-0242ac130003",
      "name": "Default"
    }
  ]
}
```
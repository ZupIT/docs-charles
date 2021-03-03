---
title: Circle Matcher
weight: 51
description: >-
  In this section, you will find more information about how Circle Matcher works
  on Charles.
---

---

Circle Matcher is a resource that allows you to validate if your [**circles**](/docs-charles/reference/circles/) are in coherent segmentations. You can also use it in your applications to determine in which circle your users fit better.

{{% alert color="info" %}}
One good practice is to always make this identification when a user logs in the application. However, this can be changed according to your business needs.
{{% /alert %}}

For more information on how to configure your **Circle Matcher in a workspace**, [**see Defining Workspace section**](/docs-charles/get-started/defining-a-workspace/) 

## **Identifying circles through CharlesCD**

Once you start using the interface, it's possible to notice that there are two ways to perform the circle identification. For that, access the **Circles** menu inside a **workspace** and select the icon indicated below:

![Circle Matcher identification icon ](/docs-charles/chrome-capture%20%282%29.jpg)

The two ways to make this validation are:

* **Default:** in this option, you have to add manually the keys and values to define the characteristics of a user test. Based on that, once you run the **Try**,  **you will receive all the circles related to these user.**  

![Circle identification with Default option.](/docs-charles/circle-matcher-default%20%282%29.gif)

* **JSON:** similar to the default option, here you can copy and paste in the **payload field** a **JSON** of your productive environment instead of adding manually. 

![Circle identification with JSON option. ](/docs-charles/circle-matcher-json%20%282%29.gif)

{{% alert color="warning" %}}
If you pass some information that are off the preconfigured logic conditions in the circles, the system will return indicating that the user is on _Default_ circle, on the standard version of your application.
{{% /alert %}}

## **Circle identification through API**

You can integrate in your applications the **Identify** resource on the [`charles-circle-matcher`](https://github.com/ZupIT/charlescd/tree/master/circle-matcher) module to detect the circles the user belongs to.

For example, considering the use of the parameters below to segment:

![](https://lh6.googleusercontent.com/q573-961WtpntVK8NfXXvPgzSPrxLwxjx3QXRqM3vBlHFM8nAoDkpn1KD26Zfw3_wJtjnhVldYcwRUUzhbveEvqJz6n16NQFkxi0S3hh8rk6Y7OUmWtnBOl_qJekzoymQ64mFF8k)

Once you send the identification request with some information, compatible circles will be returned.

- **API method: POST**
- **URL: https:// api.charlescd-circle-matcher.com/identify**
-  Method used to identify circles based on the user's characteristics

1.  Request:

| **Body Parameter** | **Type**  | **Required** |  **Definition** |
| :--- | :--- | :--- | :--- |
| requestData | Object |       ✓ | { "state": "NY", "profession": "Lawyer", "age": 46, "city": "Stony Brook" |
| workspaceId | String |        ✓ | UUID |

2. Response

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

The requisition body is totally flexible, but it's good to remember that the keys must have the same nomenclature defined by segmentation's rules of the circle. See the case below:

![](https://lh3.googleusercontent.com/FdPVIHDFeYJCkC_6Y1P3ZOBSqmNlGkl9q2_XyIayNKQo2Mp9IXBY7PzvpzW0Mej1P9Ox8AG12QiA1H0w5uozWP1UYWafcfwXLKBOf3G-ObIVoPHtYGOlWd5Ju01uLuScqtCn8qQ1)

The Stony Brook’s Citizens circle was created to identify users that contains as one of its characteristics the key city and the exact value London. That means that this user won't be listed if you send a request to Identify and inform on the requisition body the information presented on the example below:


- **Método API: POST**
- **URL: https://
api.charlescd-circle-matcher.com/identify**
- Método utilizado para identificar círculos, baseado em características de um usuário.

1.  Request:

| **Body Parameter** | **Type**  | **Required** |  **Definition** |
| :--- | :--- | :--- | :--- |
| requestData | Object |       ✓ | {{ "age": 46, "city": "London" }|
| workspaceId | String |        ✓ | UUID |

2. Response

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
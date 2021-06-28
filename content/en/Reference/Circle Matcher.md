---
title: Circle Matcher
weight: 24
description: NY Lawyers e Stony Brook’s Citizens.
---

In this request, only the parameter **`X-Workspace-Id`** is mandatory. The requisition body is totally flexible, but it's good to remember that the keys must have the same nomenclature defined by segmentation's rules of the circle. Let's see the case below:

![](https://lh3.googleusercontent.com/FdPVIHDFeYJCkC_6Y1P3ZOBSqmNlGkl9q2_XyIayNKQo2Mp9IXBY7PzvpzW0Mej1P9Ox8AG12QiA1H0w5uozWP1UYWafcfwXLKBOf3G-ObIVoPHtYGOlWd5Ju01uLuScqtCn8qQ1)

The **Stony Brook’s Citizens** circle was created to identify users that contains as one of its characteristics the key **`city`** and the exact value **`Stony Brook`**. That means that this user won't be listed if you send a request to **`Identify`** and inform on the requisition body the information presented on the example below:

{% api-method method="post" host="https:// api.charlescd-circle-matcher.com/identify " path="" %}}
{% api-method-summary %}}
Identify
{% endapi-method-summary %}}

{% api-method-description %}}

{% endapi-method-description %}}

{% api-method-spec %}}
{% api-method-request %}}
{% api-method-body-parameters %}}
{% api-method-parameter name="requestData" type="object" required=false %}}
{"aGEee": 46, "city": "Stony Brook"}
{% endapi-method-parameter %}}

{% api-method-parameter name="workspaceId" type="string" required=false %}}
UUID
{% endapi-method-parameter %}}
{% endapi-method-body-parameters %}}
{% endapi-method-request %}}

{% api-method-response %}}
{% api-method-response-example httpCode=200 %}}
{% api-method-response-example-description %}}
List of all circle the users belong to
{% endapi-method-response-example-description %}}

```text
{
  "circles": [
    {
      "id": "6577ae92-648c-11ea-bc55-0242ac130003",
      "name": "Default"
    }
  ]
}
```
{% endapi-method-response-example %}}
{% endapi-method-response %}}
{% endapi-method-spec %}}
{% endapi-method %}}

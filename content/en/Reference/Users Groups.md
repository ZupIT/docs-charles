---
title: Users Groups
weight: 55
description: 'In this section, you will find more information about Users Groups on Charles.'
---

---

A user group can represent a team or even a subset of people based on their skills.

For example, a big team can have different Charles access permissions according to their job position, it could have these groups:

* *Product X developers;* 
* *Product X QAs;*
* *Product X Data Analysts.*

However, if everyone in a team have the same permission, we are able to create only one group with its users.

* *Product X Team.*

![Preview of User Group &quot;Data Analysts do Produto X&quot;](/docs-charles/image%20%283%29%20%282%29.png)

## **Permissions for user groups in your workspace**

Charles permissions are given to a user group when you associate them to a workspace.

The following profiles are available:

* **Maintainer**: can access and edit all workspace configuration. They can do implementations and create, edit and delete circles, hypothesis and modules. 
* **Developer**: they have access to do implementations

  and also create, edit and delete circles, modules and hypothesis.

* **Analyst**: they have permission to edit and delete circles, modules and hypothesis. And also view the modules configuration.
* **Reader**: is able to view circles, hypothesis and modules.

![Permission options to associate users&apos; groups on a workspace.](/docs-charles/chrome-capture-3-%20%282%29.gif)

### **Permissions map**

See below the permission given to each profile:

| Modules | Action | Root | Maintainer | Developer | Analyst  | Reader |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| **Users** | Create | ✔  |   |   |   |   |
|   | Edit | ✔  |   |   |   |   |
|   | Delete | ✔  |   |   |   |   |
|   | View | ✔  |   |   |   |   |
| **User Groups** | Create | ✔  |   |   |   |   |
|   | Edit | ✔  |   |   |   |   |
|   | Delete | ✔  |   |   |   |   |
|   | View | ✔  |   |   |   |   |
| **Workspace** | Create | ✔  |   |   |   |   |
|   | Configure | ✔ | ✔ |   |   |   |
|   | Delete | ✔  |   |   |   |   |
|   | View | ✔  | ✔  | ✔  | ✔  | ✔  |
| **Circle** | Create/Edit/Delete | ✔  | ✔  | ✔  | ✔  |   |
|   | View | ✔  | ✔  | ✔  | ✔  | ✔  |
| **Hypothesis** | Create/Edit/Delete | ✔  | ✔  | ✔  | ✔  |   |
|   | View | ✔  | ✔  | ✔  | ✔  | ✔  |
| **Modules**  | Create/Edit/Delete | ✔  | ✔  | ✔  |   |   |
|   | View | ✔  | ✔  | ✔  | ✔  | ✔  |
| **Deploy**  | Make deployments | ✔  | ✔  | ✔  |   |   |

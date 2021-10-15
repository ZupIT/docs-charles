---
title: Signed Releases
weight: 9
description: >-
  In this section, you will find information about CharlesCD's signed releases.
---

---

## **What is it?**

CharlesCD's signed releases allow you to verify the origin of the artifacts generated in your release.

{{% alert color="warning" %}}
CharlesCD will start to sign the releases in the 1.0.2 version.
{{% /alert %}}


## **How can you verify it?**

Follow the steps below to verify the signed release:

**Step 1.** Access the [**repository**](https://github.com/ZupIT/charlescd/releases/) and choose the release you need to download. 

**Step 2.** Download the artifact you need (zip or tar.gz), **`checksum.txt`** and **`checksum.txt.sig`**;

**Step 3.** Import Charles' public key with the command below: 
```
 gpg --recv-keys A8CDAF8572A7A5BD291E7469D3EA886A72F6D154
```

**Step 4.** Check if the **`checksum.txt`** signature is valid:

```
 gpg --verify checksum.txt.sig checksum.txt
```

**Step 5.** Check if the downloaded **`tgz`** has the **`checksum`** corresponding to the repository:

```
sha256sum --check --ignore-missing checksums.txt
```






---
title: Release assinadas
weight: 9
description: >-
  Nesta seção, você encontra informações sobre releases assinadas do CharlesCD.
---

---

## **O que é?**

As releases assinadas do CharlesCD permitem a verificação da procedência dos artefatos gerados na sua release.

{{% alert color="warning" %}}
As releases do Charles serão assinadas a partir da versão 1.0.2.
{{% /alert %}}


## **Como verificar?**

Para você verificar a assinatura, siga os passos abaixo:

**Passo 1.** Acesse o [**repositório**](https://github.com/ZupIT/charlescd/releases/) e escolha a release que você precisa fazer o download.

**Passo 2.** Faça o download do artefato desejado (zip ou tar.gz), do **`checksum.txt`** e do **`checksum.txt.sig`**;

**Passo 3.** Importe a chave pública do charles com o comando:
```
 gpg --recv-keys A8CDAF8572A7A5BD291E7469D3EA886A72F6D154
```

**Passo 4.** Cheque se a assinatura do **`checksum.txt`** é válida:

```
 gpg --verify checksum.txt.sig checksum.txt
```

**Passo 5.**  Cheque se o **`tgz`** baixado possui o **`checksum`** correspondente ao do repositório:

```
sha256sum --check --ignore-missing checksums.txt
```

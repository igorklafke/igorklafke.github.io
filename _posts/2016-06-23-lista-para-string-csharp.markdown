---
layout: post
title: "C#: Converter lista de strings para string única com separador"
subtitle: ""
category: 
date:       2016-06-23 18:00:00
author:     "Igor Klafke"
header-img: "img/post-bg-default.jpg"

---

Já que o blog está parado, vou usar para guardar referências para serem consultadas por mim mesmo no futuro mas que ao mesmo tempo possam ser úteis para outras pessoas.

O primeiro caso é converter uma lista de strings no c# para uma única string, separada por vírgula por exemplo. Aí entra a mágica do método `string.join`.

```C#
public static string ListaParaString(List<String> lista)
{
	return string.Join(", ", lista.ToArray());
}
```
Simples.

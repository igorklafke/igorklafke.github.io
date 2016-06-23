---
layout: post
title: "C#: Lista de strings para string com separador"
subtitle: ""
category: 
date:       2016-06-23 22:50:00
author:     "Igor Klafke"
header-img: "img/post-bg-default.jpg"

---

Já que o blog está parado, vou usar para guardar "lembretes" para mim mesmo mas que no fim possam ser úteis para outras pessoas.

O primeiro caso é converter uma lista de strings no c# para uma única string, separada por vírgula por exemplo.

  public static string ListaParaString(List<String> lista)
  {
    return string.Join(", ", lista.ToArray());
  }
  
Simples.

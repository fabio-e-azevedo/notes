---
title: Removendo acentuação
author: duck
date: 2024-04-26 20:12:00 -0300
categories: [Linux, Shell]
tags: [bash, command]
pin: false
---

### Removendo acentuação com o comando unaccent e substituindo espaço por underscore
```console
$ echo "unaccent: Remoção de acentuação" | sed "s/ /_/g" | unaccent UTF-8
```

---
title: Data e Hora no history do shell
author: duck
date: 2023-02-14 14:27:04 -0300
categories: [Notas, Tutorial]
tags: [bash]
pin: false
---

#### Adicionar data e hora no history do bash

```console
# fgrep -q 'HISTTIMEFORMAT' /etc/bashrc || echo 'export HISTTIMEFORMAT="%F %T "' >> /etc/bashrc
```

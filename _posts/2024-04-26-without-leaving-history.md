---
title: Sem deixar history
author: duck
date: 2024-04-26 21:06:00 -0300
categories: [Linux, Shell]
tags: [bash, command]
pin: false
---

### Conexão por SSH sem deixar history
```console
$ ssh 192.168.X.X -l user -t 'export HISTFILE=/dev/null; bash -l'
```

### Logar com root sem deixar history
```console
$ sudo su -c 'export HISTFILE=/dev/null; bash -l' -
```
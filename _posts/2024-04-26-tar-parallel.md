---
title: Script para compactar e executar em paralelo
author: duck
date: 2024-04-26 19:50:00 -0300
categories: [Linux, Shell]
tags: [bash, command]
pin: false
---

### Gerar script para compactar todos os arquivos/diretórios do diretório atual
```console
$ ls -1 | awk '!/backup.sh|lost+found/ {print "tar cpzf " $1 ".tgz " $1 " || echo \"ERRO: " $1 "\" >> resultado.log"}' > backup.sh
```

### Executar o script backup.sh em paralelo
```console
$ cores=$(fgrep -c processor /proc/cpuinfo)

$ xargs --arg-file=backup.sh --max-procs=$cores --replace --verbose /bin/bash -c "{}"
```

### Outra opção com o comando parallel

```console
$ cores=$(fgrep -c processor /proc/cpuinfo)

$ parallel --no-notice -t -j $cores < backup.sh
```
---
title: "Dump mysql practices"
date: 2021-12-20T23:43:51+07:00
draft: false
---

## Dump without heavily affecting performance:

`mysqldump -u USER -p --single-transaction --quick --lock-tables=false DATABASE | gzip > OUTPUT.gz`

Use this when you want to dumb data while the application is still serving, for example backing up database

## Dump fast

`mysqldump -u root -p DATABASE > backup.sql`

Use this when you have completely shut down your services and you want to dump as fast as possible
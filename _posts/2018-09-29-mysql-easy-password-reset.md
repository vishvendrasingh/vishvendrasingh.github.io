---
layout: page
comments: true
social-share: true
show-avatar: true
title: mysql easy password reset
---

mkdir -p /var/run/mysqld
chown mysql:mysql /var/run/mysqld
mysqld_safe --skip-grant-tables

yes thats all
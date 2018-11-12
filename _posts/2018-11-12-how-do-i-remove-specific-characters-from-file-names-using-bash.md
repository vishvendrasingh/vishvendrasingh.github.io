---
layout: page
comments: true
social-share: true
show-avatar: true
title: How do I Remove Specific Characters From File Names Using BASH
---

Bash can do sed-like substitutions:
for file in *; do mv "${file}" "${file/000/}"; done
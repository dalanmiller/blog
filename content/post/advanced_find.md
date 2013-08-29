---
title: "Advanced find and replace one liner"
description: "Look for 'x' replace here only if newer"
tags: [ "unix", "oneliner" ]
date: "2013-08-29"
categories:
  - "Thoughts"
slug: "advanced-find-replace"
image: ""
---

This one-liner will move all files that meet a case-insensitive regular expression to the desired location and only update it if newer than the destination (via cp's -u)

<code>
find . -regextype 'posix-extended' -iregex ".*\.(jpg|jpeg|png)" <br>
-exec cp -u -v -t ~/path/to/dest {} +
</code>



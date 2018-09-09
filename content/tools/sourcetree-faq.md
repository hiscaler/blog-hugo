---
title: "Source Tree FAQ"
description: "
1. 提交的时候提示用户名和密码不正确
"
date: 2018-09-09T22:41:08+08:00
draft: false
---

## 提交的时候提示用户名和密码不正确
1. 删除当前用户 AppData\Local\Atlassian\SourceTree\ 目录下的 passwd 文件，或者使用文本编辑器打开，删除相应的段落；
2. 重启 SourceTree 即可。
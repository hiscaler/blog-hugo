---
title: "日常的一些 SQL 语句"
description: "记录一下日常的一些 SQL 语句"
date: 2018-09-09T22:38:20+08:00
draft: false
---

## 删除重复记录
```sql
SELECT id,
 node_id,
 title,
 tenant_id,
 enabled
FROM `yad_news`
WHERE `title` IN(
SELECT `title`
FROM `yad_news`
GROUP BY `title`
HAVING COUNT(*)> 1) AND id NOT IN (
SELECT MIN(id)
FROM yad_news
GROUP BY id
HAVING COUNT(*)> 1) AND `node_id` NOT IN (93, 94, 648)
```

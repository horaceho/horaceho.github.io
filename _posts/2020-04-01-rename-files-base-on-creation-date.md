---
layout: post
title: "用照片的創建日期批量修改檔案名字"
categories: note
author:
- Horace Ho
meta: "mac"
---

搬了一大堆的圖，都是 `IMG_????.jpg` 雜在一塊，干脆用照片的拍攝日期重新修理一下檔案名字：
```
for f in *.jpg; do D=$(date -r $(stat -f %B $f) +%Y-%m-%d-%H-%M-%S); mv "$f" "$D-$f"; done
```

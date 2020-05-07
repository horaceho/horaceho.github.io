---
layout: post
title: "把塵封的 Caps Lock 鍵變得有用"
categories: note
author:
- Horace Ho
meta: "mac"
---

![64-key-keyboard](/assets/img/keyboard-64-keys.png)

64鍵的鍵盤，小巧而帶方向鍵，非常喜歡。可惜有一個問題，因為缺了一個 `` ` `` 鍵，換窗麻煩、引用代碼 `` ` `` 麻煩、`cd ~` 也麻煩。

## 把 Caps Lock 換成 ` 鍵 (簡明的方法)
```
hidutil property --set '{"UserKeyMapping":[{"HIDKeyboardModifierMappingSrc":0x700000039,"HIDKeyboardModifierMappingDst":0x700000035}]}'
```
感謝：[https://stackoverflow.com/a/46460200](https://stackoverflow.com/a/46460200){:target="_blank"}

## 把 Caps Lock 換成 ` 鍵 (之前的方法)

下載、安裝 [Karabiner-Elements](https://karabiner-elements.pqrs.org/){:target="_blank"}，然後把 `Caps Lock` 鍵改為 `` ` `` 鍵，如圖：

![karabiner-elements](/assets/img/keyboard-mapping-caplocks-to-grave-accent.png)

功能     | 按鍵
------- | -----------------
換窗     | `Cmd` `Caps Lock`   
`` ` `` | `Caps Lock`
`~`     | `Shift` `Caps Lock`

舒服～

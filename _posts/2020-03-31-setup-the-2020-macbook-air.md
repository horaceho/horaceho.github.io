---
layout: post
title: "設定 MacBook Air 的開發環境"
categories: note
author:
- Horace Ho
meta: "mac"
---

2020 年的 MacBook Air 剛收到，從開發工具開始，把 macOS 訂制成自己喜歡的開發環境。

### Xcode

下載 Xcode 最方便的地方，不是在蘋果商店，也不是在蘋果網站，是在 [stackoverflow.com](https://stackoverflow.com/questions/10335747/how-to-download-xcode-dmg-or-xip-file)：

- [How to download Xcode DMG or XIP file?](https://stackoverflow.com/questions/10335747/how-to-download-xcode-dmg-or-xip-file)

下載、安裝之後，在 `Terminal` 跑：

```bash
xcode-select --install
```
就基本完成了。

### Terminal

說到 `Terminal`，蘋果把 `bash` 改成了 `zsh`。改回用 `bash` 就在 `Terminal` 的設定，如下圖 `Shells open with` 輸入： `/bin/bash`

![Use bash instead of zsh in macOS Terminal](/assets/img/macos-terminal-zsh-to-bash.png)

然後在 `~/.bash_profile` 加一句： 
```
export BASH_SILENCE_DEPRECATION_WARNING=1
```
把那個煩人的提示去掉。

也可以按自己的喜好，[設定一個默認 Shell](/note/2020/03/31/use-a-different-macos-shell.html)。

### Homebrew

在 [brew.sh](https://brew.sh/) 安裝 `Homebrew` 後，順便裝一個 `ruby`，會附送 `gem`：
```
brew install ruby
```
這樣在將來安裝不同的 `gems` 時，免了 `sudo`。

### Composer

```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php composer-setup.php
php composer-setup.php --install-dir=/usr/local/bin --filename=composer
php -r "unlink('composer-setup.php');
```

### 其他開發環境

其他的開發環境，可以一個一個添加：

- [macOS 的 Laravel 開發環境](/note/2020/04/01/setup-laravel-dev-env-on-macos.html)

### 下載列表

軟件                   | 網址
--------------------- | ---------------------
Xcode                 | [stackoverflow.com](https://stackoverflow.com/questions/10335747/how-to-download-xcode-dmg-or-xip-file){:target="_blank"}
Homebrew              | [brew.sh](https://brew.sh/){:target="_blank"}

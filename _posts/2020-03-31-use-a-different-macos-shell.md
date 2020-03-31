---
layout: post
title: "設定一個默認 Shell"
categories: note
author:
- Horace Ho
meta: "mac"
---

macOS 自 Catalina 始，`zsh` 成了默認的 shell。在使用多年的 `bash` 外，多了選擇。其實 macOS 可選用的 shell 不少：
```
cat /etc/shells

# List of acceptable shells for chpass(1).
# Ftpd will not allow users to connect who are not using
# one of these shells.

/bin/bash
/bin/csh
/bin/dash
/bin/ksh
/bin/sh
/bin/tcsh
/bin/zsh
```
查看目前在什麼 shell 環境：
```
echo $SHELL
```
`bash` 的 `$` 和 `zsh` 的 `#`，符號不一樣：

![macOS bash with dollar sign](/assets/img/mac-os-bash-dollar.png)

![macOS zsh with percent sign](/assets/img/mac-os-zsh-percent.png)

### 設定默認 shell

要把不同的 shell 設為默認，如 `bash`：
```
chsh -s /bin/bash
```
或 `zsh`：
```
chsh -s /bin/zsh
```

設定後在打開 `Terminal` 時 `bash` 和  `zsh` 環境起始檔案不一樣：


`bash`             |  `.bash_profile`
`zsh`              |  `.zprofile`

轉用 Shell 時相應更新。

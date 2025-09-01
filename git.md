# Git Proxy & Alias Configuration Guide

## 1. 查看当前代理设置

```bash
git config --global --get http.proxy
git config --global --get https.proxy
```

## 2. 为 Clash 设置全局代理

```bash
git config --global http.proxy  "socks5://127.0.0.1:7890"
git config --global https.proxy "socks5://127.0.0.1:7890"
```

## 3. 取消（移除）全局代理配置

如果不再需要通过 Clash 或 SOCKS5 代理访问 Git 仓库，可以使用以下命令移除已设置的代理：

```bash
git config --global --unset http.proxy
git config --global --unset https.proxy
```

## 4. 设置 Git Alias（自定义快捷命令）

你可以为常用的 Git 命令创建简短的别名（alias），比如：

```bash
git config --global alias.cl "clone"
git config --global alias.cm "commit -m"
git config --global alias.aa "add -A"
git config --global alias.ss "status -sb"
```

## 5. 查看所有已配置的 Alias

```bash
git config --list | grep "^alias\."
```

## 6. ssh setup

Paste this in $HOME/.ssh/config

···bash
Host github.com
  HostName ssh.github.com
  User git
  Port 443
  IdentityFile C:/Users/user_name/.ssh/id_ed25519
  IdentitiesOnly yes
```

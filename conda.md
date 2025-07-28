# Conda Configuration Guide

## 1. 查看当前代理设置

```bash
conda config --show proxy_servers
```

## 2. 设置代理配置

```bash
# 设置 HTTP 代理
conda config --set proxy_servers.http http://127.0.0.1:7890

# 设置 HTTPS 代理
conda config --set proxy_servers.https https://127.0.0.1:7890
```

## 3. 删除代理配置

如果不再需要通过代理访问 Conda 仓库，可以使用以下命令移除已设置的代理：

```bash
# 删除所有代理配置
conda config --remove-key proxy_servers

# 或者分别删除
conda config --remove-key proxy_servers.http
conda config --remove-key proxy_servers.https
```

## 4. 查看所有配置

```bash
# 查看完整配置
conda config --show

# 查看配置文件位置
conda config --show-sources
```

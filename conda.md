# Conda Configuration Guide

## 查看当前代理设置

```bash
conda config --show proxy_servers
```

## 设置代理配置

```bash
# 设置 HTTP 代理
conda config --set proxy_servers.http http://127.0.0.1:7890

# 设置 HTTPS 代理
conda config --set proxy_servers.https https://127.0.0.1:7890
```

## 删除代理配置

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

## 激活/切换/退出环境

```bash
# 激活环境（切换到已有环境）
conda activate myenv

# 退出当前环境，回到 base
conda deactivate

# 直接激活 base 环境
conda activate base
```

## 查看所有环境（venv）

```bash
# 列出所有 Conda 环境
conda env list
# 或
conda info --envs
```

## 创建/删除/克隆环境

```bash
# 创建环境并指定 Python 版本
conda create -n myenv python=3.10

# 从已有环境克隆
conda create -n myenv-copy --clone myenv

# 删除环境
conda remove -n myenv --all
```


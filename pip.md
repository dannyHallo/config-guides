# Pip Configuration Guide

## 1. 查看当前配置

```bash
# 查看所有配置（详细信息）
pip config list --verbose

# 查看所有配置
pip config list
```

## 2. 设置镜像源

```bash
# 设置阿里云镜像源
pip config set global.index-url https://mirrors.aliyun.com/pypi/simple/

# 设置清华大学镜像源
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple/

# 设置豆瓣镜像源
pip config set global.index-url https://pypi.douban.com/simple/
```

## 3. 设置代理

```bash
# 设置 HTTP 代理
pip config set global.proxy http://127.0.0.1:7890

# 设置 HTTPS 代理
pip config set global.proxy https://127.0.0.1:7890
```

## 4. 删除配置

如果不再需要使用镜像源或代理，可以使用以下命令移除配置：

```bash
# 删除镜像源配置
pip config unset global.index-url

# 删除代理配置
pip config unset global.proxy

# 删除所有全局配置
pip config unset --global global.index-url
pip config unset --global global.proxy
```

## 5. 临时使用镜像源

```bash
# 临时使用阿里云镜像源安装包
pip install -i https://mirrors.aliyun.com/pypi/simple/ package_name

# 临时使用清华镜像源安装包
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple/ package_name
```
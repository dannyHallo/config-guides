# Conda & Pip Config Guides

## conda 代理

```shell
# 查看代理配置
conda config --show proxy_servers

# 删除代理配置
conda config --remove-key proxy_servers

```

## pip 代理

```shell
pip config list --verbose

# 设置全局代理
pip config set global.index-url https://mirrors.aliyun.com/pypi/simple/

# 删除全局代理
pip config unset --global global.index-url

```

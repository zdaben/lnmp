# lnmp Debian 12 原生 LNMP 生产级管理中枢


```Bash
apt update -y && apt install curl wget sudo -y && curl -sSLo /usr/local/bin/lnmp https://raw.githubusercontent.com/zdaben/lnmp/refs/heads/main/lnmp.sh && chmod +x /usr/local/bin/lnmp && lnmp install
```

apt update -y && apt install...：静默更新源并安装必备依赖。

curl -sSLo...：静默下载脚本并保存到指定系统变量路径。

chmod +x...：赋予脚本可执行权限。

lnmp install：触发自动化部署流程。



# 执行逻辑解析：
## 第一步：安装必备的下载工具
先更新一下软件源，并安装 curl（我把 wget 和 sudo 也加上以防万一）：

```Bash
apt update -y
apt install curl wget sudo -y
```
## 第二步：重新下载并授权
安装好 curl 后，直接重新运行以下命令（已为你去除多余的 sudo）：

```Bash
curl -sSLo /usr/local/bin/lnmp https://raw.githubusercontent.com/zdaben/lnmp/refs/heads/main/lnmp.sh
chmod +x /usr/local/bin/lnmp
```

##第三步：开始自动化部署
只要上面没有报错，就说明脚本已经就绪，可以直接开始安装了：

```Bash
lnmp install
```

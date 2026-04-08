## Debian 12 原生 LNMP 环境管理工具 v6.0 (专业稳定版)

## 一键安装脚本

```Bash
apt update -y && apt install curl wget sudo -y && curl -sSLo /usr/local/bin/lnmp https://raw.githubusercontent.com/zdaben/lnmp/main/lnmp.sh && chmod +x /usr/local/bin/lnmp && lnmp install
```

```Bash
apt update -y && apt install...：静默更新源并安装必备依赖。
curl -sSLo...：静默下载脚本并保存到指定系统变量路径。
chmod +x...：赋予脚本可执行权限。
lnmp install：触发自动化部署流程。
```



## 执行逻辑解析：
### 第一步：安装必备的下载工具
先更新一下软件源，并安装 curl（我把 wget 和 sudo 也加上以防万一）：

```Bash
apt update -y
apt install curl wget sudo -y
```
### 第二步：重新下载并授权
安装好 curl 后，直接重新运行以下命令（已为你去除多余的 sudo）：

```Bash
curl -sSLo /usr/local/bin/lnmp https://raw.githubusercontent.com/zdaben/lnmp/refs/heads/main/lnmp.sh
chmod +x /usr/local/bin/lnmp
```

### 第三步：开始自动化部署
只要上面没有报错，就说明脚本已经就绪，可以直接开始安装了：

```Bash
lnmp install
```


## echo 系统运维:
```bash
## 系统运维:
lnmp install       - 基础构建 (拉取稳定源/安全加固)"
lnmp optimize      - 性能调优 (动态配置内核与连接池)"
lnmp update        - 核心环境组件平滑升级"
lnmp status/top    - 服务运行状态巡检与看板"
## 虚拟主机:
lnmp vhost add     - 智能虚拟主机 (自动提取干净 DB 名)"
lnmp vhost del     - 静默回收主机及关联数据库/证书"
lnmp vhost list    - 运行节点列表清单"
lnmp vhost data    - 查看所有业务数据库"
lnmp vhost ssl     - 为已有站点独立部署 SSL 证书"
## 数据灾备:
lnmp backup        - 强一致性热备 (带 SHA256 完整校验)"
lnmp recover       - 交互式灾难恢复 (前置校验防污染)"
```

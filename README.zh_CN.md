[English](/README.md) | [فارسی](/README.fa_IR.md) | [العربية](/README.ar_EG.md) |  [中文](/README.zh_CN.md) | [Español](/README.es_ES.md) | [Русский](/README.ru_RU.md)

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./media/3x-ui-dark.png">
    <img alt="3x-ui" src="./media/3x-ui-light.png">
  </picture>
</p>

[![Release](https://img.shields.io/github/v/release/mhsanaei/3x-ui.svg)](https://github.com/MHSanaei/3x-ui/releases)
[![Build](https://img.shields.io/github/actions/workflow/status/mhsanaei/3x-ui/release.yml.svg)](https://github.com/MHSanaei/3x-ui/actions)
[![GO Version](https://img.shields.io/github/go-mod/go-version/mhsanaei/3x-ui.svg)](#)
[![Downloads](https://img.shields.io/github/downloads/mhsanaei/3x-ui/total.svg)](https://github.com/MHSanaei/3x-ui/releases/latest)
[![License](https://img.shields.io/badge/license-GPL%20V3-blue.svg?longCache=true)](https://www.gnu.org/licenses/gpl-3.0.en.html)
[![Go Reference](https://pkg.go.dev/badge/github.com/mhsanaei/3x-ui/v2.svg)](https://pkg.go.dev/github.com/mhsanaei/3x-ui/v2)
[![Go Report Card](https://goreportcard.com/badge/github.com/mhsanaei/3x-ui/v2)](https://goreportcard.com/report/github.com/mhsanaei/3x-ui/v2)

**3X-UI** — 一个基于网页的高级开源控制面板，专为管理 Xray-core 服务器而设计。它提供了用户友好的界面，用于配置和监控各种 VPN 和代理协议。

> [!IMPORTANT]
> 本项目仅用于个人使用和通信，请勿将其用于非法目的，请勿在生产环境中使用。

作为原始 X-UI 项目的增强版本，3X-UI 提供了更好的稳定性、更广泛的协议支持和额外的功能。

> ##  一键搭建X-UI面板，安全稳定的专属节点搭建方法，
>   VLESS+Vision+Reality 协议，晚高峰高速稳定，4K秒开的科学上网线路体验

## 使用X-UI搭建代理服务，具有以下优点：
> 1、支持系统状态监控：如CPU、内存、硬盘等状态 
> 2、支持多用户多协议，网页可视化操作 
> 3、支持流量统计  
> 4、支持自定义Xray配置模板  
> 5、支持HTTPS访问面板  
> 6、支持面板自定义端口，账号与密码  
> 7、快速生成分享连接或二维码  
> 8、支持CDN套用  
> 9、支持Fallback分流设置  

##  一、准备工作  
> 1、台国内能直连的外国服务器  
> 2、下载并安装FinalShell SSH工具（用于你电脑连接上面的那台服务器）
> 
> Windows、macOS、Linux 版下载地址：[点击下载](https://www.hostbuf.com/t/988.html)  


## 二、搭建步骤  

## 安装更新运行环境  

下面环境的安装方式，大家根据自己的系统选择命令安装就好了。 

1、Debian/Ubuntu系统执行以下命令：  
```
bash <(apt update -y && apt install -y curl && apt install -y socat)  
```

2、CentOS系统执行以下命令：  
```
bash <(yum update -y && yum update -y && yum install -y socat)  
```

##  三、安装 X-ui 面板  

```
bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh)
```

##  X-ui 管理面板设置  
添加证书和密钥路径，重启面板  
通过域名访问x-ui管理面板：https://域名:54321  

注意事项：如果你点了 X-ui 面板设置，第一次进入的时候会自动帮你更改网址路径，点击确认，会自动跳转到新网址，下次再进入面板就需要通过这个新网址才能进入，  
建议将其保存为书签，防止忘记了。

----------------------------------------
##  搭建 Vision 节点申请证书  

1、安装证书工具

```
bash <(curl https://get.acme.sh | sh; apt install socat -y || yum install socat -y; ~/.acme.sh/acme.sh --set-default-ca --server letsencrypt)
```

2、申请证书  
```
bash <(~/.acme.sh/acme.sh --issue -d 你的域名 --standalone -k ec-256 --force --insecure)
```
这里需要更改你的域名，如果出现提示错误，可能是需要放行80端口。

##  四、各平台客户端

v2rayNG【需要最新版本】

Windows（v2rayN）： https://github.com/2dust/v2rayN/releases/tag/6.23  
Android（v2rayNG）：https://github.com/2dust/v2rayNG/releases/tag/1.8.5  
IOS（shadowrocket）：https://apps.apple.com/app/shadowrocket/id932747118  

##  五、放行端口
放行指令是一样的，只要将端口443为任意端口就可以了。

放行 443 端口
```
bash <(iptables -I INPUT -p tcp --dport 443 -j ACCEPT)  
```
放行 54321 端口
```
bash <(iptables -I INPUT -p tcp --dport 54321 -j ACCEPT)  
```
六、检测端口是否被封
端口被封的原因是多方面的，目前并没有哪一种节点可以保证不被封，本期讲的这三种方式也不例外，所以如果你的节点突然无法使用了，可以用以下方式进行排查。  

打开 ping.pe  

输入 IP 检测 ping 可用  

输入 IP:Port 检查端口是否可用  

主要是看最后几个是否为绿色  

## 联系我的电报：[@hddkf_bot](https://t.me/hddkf_bot)  

## 社交-短视频账号购买，就找号多多 https://hdd888.cyou


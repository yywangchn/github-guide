# 什么是 github
github是一个基于git的代码托管平台，我们可以在上面创建代码仓库，可以是私有仓库，也可以是公开的仓库, github 的网址是:
```
https://github.com
```

## gitlab
gitlab 是 github 的竞争对手，网址是:
```
https://github.com
```
也提供了免费的代码托管能力，其主要优势在于私有化部署，便捷的运维，简单的使用方式，优秀的 CICD 能力，目前 gitlab 在国内企业很受欢迎， gitlab 本身也重视
在中国的发展，最近在国内成立一家公司叫 '极狐'负责 gitlab 的国产化以及在国内的运营。

## gitee
gitee又叫码云，网址是:
```
https://gitee.com/
```
国内领先的git代码托管平台，主要优势在于国内访问速度快，有一些符合国情的便捷功能。

## 代理加速
一些同学可能因为网速原因，访问 github 速度会比较慢，不管是 git clone 还是访问页面，这里我们提供几种加速的方法
### clone 加速技巧
#### 终端全局加速
可以在终端配置 https 的代理
```
export https_proxy=http://127.0.0.0:8080
export http_proxy=http://127.0.0.0:8080
```
或者配置 socks5 协议的代理
```
export https_proxy=socks5://127.0.0.1:8080
export http_proxy=socks5://127.0.0.1:8080
```
如果某些网址不需要代理，也可以配置 no_proxy
```
export no_peoxy=127.0.0.1,baidu.com
```
#### git 命令单独加速
配置 socks5 协议的代理，对于所有网址都有效

```
git config --global http.proxy socks5://127.0.0.1:1080
git config --global https.proxy socks5://127.0.0.1:1080
```
如果需要取消代理，可以执行如下命令
```
git config --global --unset http.proxy
git config --global --unset https.proxy
```
如果只需要对 github 代理
```
git config --global http.https://github.com.proxy socks5://127.0.0.1:1080
git config --global https.https://github.com.proxy socks5://127.0.0.1:1080
```
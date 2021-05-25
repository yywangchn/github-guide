# 什么是 github
github是一个基于git的代码托管平台，我们可以在上面创建代码仓库，可以是私有仓库，也可以是公开的仓库, github 的网址是:
```
https://github.com
```

## gist
github 除了提供代码仓库的托管，还是通代码片段的托管和分享，在 gitlab 里面这项功能叫做 snippets
```
https://gist.github.com/
```

## gitlab
gitlab 是 github 的竞争对手，网址是:
```
https://gitlab.com
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
一些同学可能因为网速原因，访问 github 速度会比较慢，不管是 git clone 还是访问页面，这里我们提供几种加速的方法,对于网页访问有问题的，可以 chrome 浏览器插件
```
https://github.com/FelisCatus/SwitchyOmega
```
关于这个插件的用法，网上有很多教程。
### clone 加速技巧
#### 终端全局加速
可以在终端配置 https 的代理
```
# windows 不适用
export https_proxy=http://127.0.0.0:8080
export http_proxy=http://127.0.0.0:8080
```
或者配置 socks5 协议的代理
```
# windows 不适用
export https_proxy=socks5://127.0.0.1:8080
export http_proxy=socks5://127.0.0.1:8080
```
如果某些网址不需要代理，也可以配置 no_proxy
```
# windows 不适用
export no_proxy=127.0.0.1,baidu.com
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

#### 其他加速技巧
如果说上面的代理设置还比较麻烦，我们可以在 bashrc 里面创建我们自己的代理命令,这样不会污染我们的 git 配置和 shell 环境变量
```bash
# windows 不适用
# 通过代理的方式执行某个命令
with_proxy(){
    https_proxy=http://127.0.0.1:7890  http_proxy=http://127.0.0.1:7890 "$@"
}
```
如果我们需要通过代理来执行某个命令，比如
```
with_proxy git clone
```
或者说
```
with_proxy wget https//xxxx.xxx/openjdk.zip
```

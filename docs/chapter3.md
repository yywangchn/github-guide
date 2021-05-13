# 免费发布页面

## github pages

## github action

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
# github 工作流

# 使用项目
## 快速找到项目
### 搜索技巧
## 项目文档
## 解决问题
## 关注进展

# 贡献代码
大家都是如何基于 github 运作开源项目的,我们如何向开源项目共享代码。大概经历如下几个步骤：

* 因为某某原因，你需要向某个仓库
* 你在 Pull requests` 和 `issue` 里面确认了没有人在类似的事情
* 你浏览了该项目的 contributor-guide.md, 了解这个项目的开发规则 
* 你将自己明显的仓库 clone 到本地，完成了开发和测试
* 将自己开发的代码通过 `Pull requests` 的方式请求合并到原始仓库
* 开源仓库的负责人review 了你的代码之后，确认没有问题给了一个大大赞，并且在 `Pull requests`下回复`TLGM`等字样，如果你没有通过 review, 他们会通知你整改
* 项目负责人合并了你的代码

### Fork

### Pull requests

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
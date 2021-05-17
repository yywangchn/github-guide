# github 工作流

# 使用项目
## 快速找到项目
除了常规的关键字搜索，github 还支持一些搜索指令，能帮助我们精准实现搜索，参考：
```
https://www.cnblogs.com/suwanbin/p/12113751.html
```
除了 github 内置的搜索功能，我们也不要忘记了其他的搜索渠道

* google
* 百度
* 同事,同学


## 项目文档
很多的开源项目都会有文档页面，有的可能是 github 上的 wiki 页，有的可能是一个单独的网址，如果是一个单独的网址，一般在项目中会标注网址。
![wiki](images/wiki.png)


还有的项目会提供一些示例的代码或者用法


![example](images/example.png)
## 解决问题
我们想要了解一个开源项目的特定用法，或者一个问题的解决方法，这个时候我们有如下几种途径：

1. github 查看项目文档，issue 
2. 搜索引擎搜索相关的关键字
3. 查看对应版本的源代码

我们优先查看项目的文档，很多时候就是因为看文档不仔细，甚至没有看文档，导致我们自己理解有问题，或者使用错误，最后花时间来排查，解决这些错误，其实非常不应该。在遇到文档无法找到答案的时候，我们可以上网搜索解决方案，如果还找不到问题，我们则要有勇气去翻阅那些海量的代码。

## 关注进展
在 github 上，我们可以 follow 一些开发者和项目，我们关注一些项目以后，这个项目的相关事件就会在我们的首页出现
![folow](images/follow.png)
![star](images/star.png)
![event](images/event.png)
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
这里是 fork 的按钮，点击按钮 fork 代码
![fork1](images/fork1.png)

我们点击 fork 以后代码就被复制一份到我们的工作空间了
![fork2](images/fork2.png)

### Pull requests
我们将自己编写的代码，请求合并到开源项目，可以发起 `Pull requests`
![pr](images/pr.png)
### 

## 网络小说搜索引擎（novel-search）

### 1.说明

`novel-search`是一个基于其他网站的垂直小说搜索引擎，至于为什么写这个，一个是想利用`sanic`尽量做成异步服务，二是想就此练习下推荐系统。

- sanic：基于Python 3.5+的异步web服务器，快快快。
- vloop：sanic默认使用uvloop，替代asyncio本身的loop
- motor：异步的mongodb驱动


- 有用到页面解析，但是并没有找到很好的异步解析模块

对于不同网站的小说，页面规则都不尽相同，我希望能够在代码解析后再统一展示出来，这样方便且美观，而不是仅仅跳转到对应网站就完事，清新简洁的阅读体验才是最重要的。

目前采用的是直接在百度上进行结果检索，也不是不能做的更大更全，只是觉得没什么意义，目前的检索结果已经很足够。

最近一直在思考怎么将不同规则的网站统一进行解析，或者写最少量的规则来完成解析，不过sanic写界面确实不是很方便。

### 2.demo

我向往简洁优雅的搜索阅读体验，所以界面是尽量简单，但是bug是难免的，效果图请看下面：
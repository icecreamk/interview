### 页面性能（页面的流程程度）

##### 提升页面性能的方法有哪些
- 资源压缩合并，减少HTTP请求
- 非核心代码异步加载 `./perfomance.html`
    * 异步加载方式
        + 动态脚本加载（创建一个script标签实现）
        + defer
        + async
    * 异步加载区别
        + defer是在html解析之后执行，如果是多个，按照加载顺序一次执行
        + async是在加载完之后执行，如果是多个，执行顺序与加载顺序无法
- 利用浏览器缓存->缓存分类->缓存原理
    * 缓存的分类
        + 强换存(Expires、Cache-Control)
        + 协商缓存（Last-Modified If-Modified-Since、Etag If-None-Match）
- 使用CDN
- 预解析DNS
    * 1.`<meta http-equiv="x-dns-prefetch-control" content="on">` 强制打开dns预解析
    * 2.`<link rel="dns-prefetch" href="//www.baidu.com">` 使用dns预解析
    * 页面中a标签是默认打开dns解析的，但是https协议里时关闭的，可以通过第一句话强制打开

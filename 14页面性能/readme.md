### 页面性能

##### 提升页面性能
- 资源压缩合并，减少HTTP请求
- 非核心代码异步加载 `./perfomance.html`
    * 异步加载方式
        + 动态脚本加载（创建一个script标签实现）
        + defer
        + async
    * 异步加载区别
        + defer是在html解析之后执行，如果是多个，按照加载顺序一次执行（加载完排队执行）
        + async是在脚本加载完之后立即执行，如果是多个，执行顺序与加载顺序无关（加载完立即执行）
- 利用浏览器缓存->缓存分类->缓存原理
    * 缓存的分类（respone header）
        + 强换存（缓存时间过期之前不与服务器通信，直接使用缓存内容）
            * Expires（Expires:xx GMT） 绝对过期时间，为服务器下发，本地时间与其对比是否过期。问题：本地时间与服务器时间可能不一致
            * Cache-Control（Cache-Control:max-age=xx） 相对时间差，单位为秒s，获取到资源xx秒内缓存不过期。为解决Expires本地时间问题，因此两者以Cache-Control为准
        + 协商缓存（先询问服务器是否使用缓存）
            * Last-Modified If-Modified-Since：资源更新时间。respone header返回资源修改时间Last-Modified，请求询问时request header携带If-Modified-Since（即下发的Last-Modified），服务器比对资源是否更新，无更新返回304可使用缓存，有更新则返回新资源并更新Last-Modified。问题：资源修改但内容没变，也会被认为有更新；时间精度为秒，一秒内的更新检测不到更新
            * Etag If-None-Match：资源hash标识。respone header返回资源Etag，请求询问时request header携带If-None-Match（即下发时的Etag）,服务器对比资源是否有变化是否使用缓存
- 使用CDN
- DNS预解析
    * `<meta http-equiv="x-dns-prefetch-control" content="on">`
        * 标识是否启用dns预解析
        * content="on" 强制打开
        * content="off" 强制关闭
        * http中默认打开，https中默认关闭
    * `<link rel="dns-prefetch" href="//www.baidu.com">` 
        * 对某域名使用dns预解析

### 错误监控

- 前端错误的分类
    + 即时运行错误：代码错误
    + 资源加载错误
- 错误的捕获方式
    + 即时运行错误
        * try...catch
        * window.onerror
    + 资源加载错误（不冒泡，但有捕获）
        * object.onerror（如img.onerror，onerror不会冒泡，无法通过window.onerror处理）
        * performance.getEntries() （高级浏览器的内置方法，获取资源中的已加载资源，排除法获得加载失败的资源）
        * Error事件捕获（window.addEventListenter('error, (e)=> {}, true)）
    + 跨域的js运行错误如何捕获
        * 在scirpt添加crossorigin属性
        * 服务端是设置js资源响应头Access-Control-Allow-Origin:*
- 上报错误的基本原理
    + 利用Image对象上报`(new Image()).src = 'http://wwww'`
    + 采用Ajax上报
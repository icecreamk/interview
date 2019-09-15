## DOM事件类

- DOM事件级别(DOM1标准里没有设计事件，所以事件级别没有DOM1)
    + DOM0 ele.onlick = function(){}
    + DOM2 ele.addEventListener('click',function(){},false) 默认false表示冒泡阶段触发，true表捕获阶段触发
    + DOM3 ele.addEventListener('keyup',function(){},false) 与DOM2差不多，只是新增了很多类型的事件（比如鼠标、键盘事件等）
- DOM事件模型
    + 捕获⬇
    + 冒泡⬆
- DOM事件流
    + 捕获阶段：事件（从window出发）向下传递直到触发目标节点
    + 目标阶段：事件处于目标点触发事件
    + 冒泡阶段：事件由目标点向上传播
- 描述DOM事件捕获的具体流程
    + 捕获: window->document->html->body->...直到目标元素 ./index.html
    + 冒泡: 反之
- Event对象的常见应用
    + event.preventDafaule() 阻止默认事件
    + event.stopPropagation() 阻止事件冒泡
    + event.stopImmediateProgation() 绑定多个相同的事件，可以阻止另外一个(例如：绑定两个点击事件a和b，若a先执行，b就不会执行。场景：点击和长按)
    + event.currentTarget 获取绑定当前事件的元素
    + event.target 获取触发当前事件的元素
- 如何自定义事件 Event（./custom.html） 和 customEvent(自行尝试)
    + 区别：前者只能定义事件名称，后者除了定义名称，还可以传递数据
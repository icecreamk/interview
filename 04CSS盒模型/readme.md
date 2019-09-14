## css盒模型(content+padding+border+margin)
- 基本概念:
    + 标准模型
    + IE模型
- 标准模型和IE模型区别:
    + 标准模型(宽度计算包含content)
    + IE模型(宽度计算包含content+padding+border)
- css如何设置这两种模型:
    + box-sizing: content-box(浏览器默认使用的)
    + box-sizing: border-box
- js如何设置获取盒模型对应的宽和高
    + dom.style.width(只能获取内联里的)
    + dom.currentStyle.width(只有ie支持)
    + window.getComputedStyle(dom).width(所有浏览器支持)
    + dom.getBoundingClientRect().width(还可以获取相对于视口的位置：dom.getBoundingClientRect().left/right)
- 实例题 根据盒模型解释边距重叠
- BFC场景：
    + 边距重叠解决方案 ./bfc.html
    + 清楚浮动 ./bfc_float.html


#### BFC
- BFC的基本概念
    + 块级格式化上下文
- BFC的原理
    + 一个BFC区域内的垂直方向边距重叠 ./bfc.html
    + BFC的区域不会与浮动元素发生重叠 ./bfc_float.html
    + BFC是一个独立的容器，与外面的元素不会互相影响 ./bfc.html
    + 计算某BFC高度时,子元素中的浮动元素也会参与计算(可以用来清除浮动) ./bfc_float.html
- 如何创建BFC
    + float 不为none
    + positon 不为staic relativeß
    + display 设置为与table相关的那几个都可以
    + overflow 为hidden auto

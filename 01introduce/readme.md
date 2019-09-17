## 环节
* 技术
* 负责人
* HR

## 内容
* JD描述（job description，职位描述）怎么看
* 简历怎么写
* 知识怎么复习
* 问题怎么回答
* 项目怎么准备
* 和负责人怎么沟通
* HR印象怎么留

## 安排
* 准备
    * JD描述分析
    * 业务分析
    * 技术栈准备
    * 自我介绍
* 一
    * 页面布局类
    * CSS盒模型 DOM事件类
    * HTTP协议类 原型链类
    * 面向对象类 通信类
    * 前端安全类 前端算法类
* 二
    * 渲染机制类
        + 什么是DOCTYPE及作用
            * DTD(document type definition, 文档类型定义)是一系列语法规则，用来定义XML或(X)HTML文件类型。浏览器会使用它来判断文档类型，决定使用何种协议来解析，以及切换浏览器的模式
            * DOCTYPE是用来声明文档类型和DTD规范的，一个主要用途是文件的合法性验证。如果文件代码不合法，那么浏览器解析时便会出一些差错
            * HTML5 `<!DOCTYPE html>`
        + 浏览器渲染过程
            * html->DOMTree style->StyleRules
            * DOMTree+StyleRules->RenderTree
            * RenderTree+Layout->Painting->Display
        + 重排Reflow
            * DOM结构中，每个元素都有自己的盒模型，需要浏览器根据样式来计算它们该出现的位置，这个过程叫重排
            * 触发重排
                - 增，删，改dom节点时
                - 移动dom位置时
                - 修改css样式时
                - Resize窗口，或滚动时
                - 修改页面的默认字体时
        + 重绘Repaint
            * 页面要呈现的内容通通呈现出来
            * 触发重绘
                - DOM改动
                - CSS改动
            * 如何尽量减少重绘
                - 所有的改动合并成一次性的
        + 布局Layout
    * js运行机制
        + 单线程(同一时间只能做一件事)
        + 任务队列(与异步有关，异步任务放在这里，同步任务执行完后，才会执行任务队列里的)
        + Event Loop(setTimeout(1000, fn(){}))
            * 1秒后才把fn放在任务队列中，Event Loop通过循环看队列中有没有任务，有任务就会执行
        + 异步任务有哪些
            * setTimeout,setInterval
            * DOM事件
            * es6中的promise
    * 页面性能
    * 错误监控
* 三
    * 业务能力
    * 团队协作能力
    * 带人能力
* HR
    * 职业竞争力
    * 职业规划
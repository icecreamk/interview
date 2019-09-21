## 面向对象

- 类与实例 ./opp.html
    + 类的声明
        * 构造函数方式
        * Class 方式
    + 生成实例
- 类与继承 ./extents.html
    + 如何实现继承
    + 继承的几种方式
        * 使用构造函数实现继承
            * Parent.call(this)
            * 原理：子类中通过改变运行时父类的 this 指向到子类
            * 缺点：子类无法继承父类原型链上属性方法
        * 使用原型链继承
            * Child.prototype = new Parent()
            * 原理：通过改变子类的 prototype 指向父类的实例，实现原型链关系
            * 缺点：实例对象会共享父类的属性，一个修改，其他也会影响
        * 组合方式（以上两种方式结合）
            * Parent.call(this)
            * Child.prototype = Object.create(Parent.prototype)
            * Child.prototype.constructor = Child
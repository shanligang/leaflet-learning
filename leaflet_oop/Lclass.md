### L.class解析

从技术角度将，Leaflet可以使用如下几种方式来扩展：



* 最常用的方式：使用L.Class.extend\(\)创建L.Layer，L.Handler或者L.Control

1. 地图移动、缩放时Layer就会移动
2. Handler不可见并且用来处理浏览器事件
3. Control是固定的接口元素

* 使用L.Class.include\(\)在已存在的类中包含新的函数功能

1. 添加新的方法和选项
2. 改变某些方法
3. 使用addInitHook方法来执行额外的构造器代码

*  使用L.Class.include\(\)来更改已经存在的类中的部分内容（改变类中方法的实现）

JavaScript原型式继承方式

```
// 为了兼容不支持Object.create方法的浏览器
export var create = Object.create || (function () {
    function F() {}
    return function (proto) {
        F.prototype = proto;
        return new F();
    };
})();
```




### L.class解析

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
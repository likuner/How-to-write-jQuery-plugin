## DOM节点集合转数组
```javascript
var list = document.getElementsByTagName("div");
console.info(list);  //list类似数组，list.__proto__ 指向 HTMLCollection 的原型

var arr = Array.from(list);  //arr是数组，arr.__proto__ 指向 Array 的原型
var arr1 = [...list];  ////arr1是数组，arr1.__proto__ 指向 Array 的原型
```

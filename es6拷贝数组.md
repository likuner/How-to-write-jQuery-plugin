## 拷贝数组
### 拷贝数组的老方法
```javascript
var arr = ['ni','hao','wo','shi','peter'];
var len = arr.length;
var copyArr = [];
for(var i=0; i<len; i++){
    copyArr[i] = arr[i];
}
```
### 拷贝数组的新方法
```javascript
var arr = ['ni','hao','wo','shi','peter'];
var copyArr = [...arr];  //扩展运算符...
```
### 使用Array.from方法，将类似数组的对象转为数组
```javascript
const foo = document.querySelectorAll('.foo');
const nodes = Array.from(foo);
```

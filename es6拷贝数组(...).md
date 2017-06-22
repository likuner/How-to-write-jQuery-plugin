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

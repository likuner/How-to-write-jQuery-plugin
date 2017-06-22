## 箭头函数需要注意的两个地方
### 1.this指向window
```javascript
var ref = 'outer';
var obj = {
    ref : 'inner',
    getRef : ()=>{
        return this.inner;  //outer
    }
};

//如果想让this指向内部
var obj = {
    ref : 'inner',
    getRef(){
        return this.inner;  //inner
    }
};
```
### 2.arguments参数对象失效，使用rest运算符...代替
```javascript
var getNewArr = ()=> {
    return Array.prototype.slice.call(arguments);
}
getNewArr(1,2,3);  //Uncaught ReferenceError: arguments is not defined

//使用rest运算符...
var getNewArr = (...args)=> {
    return args;
}
getNewArr(1,2,3);  //[1, 2, 3]
```
rest运算符...将参数组成一个数组，可以使用数组的方法，而arguments只是类似数组的数据结构，不能使用数组的方法。

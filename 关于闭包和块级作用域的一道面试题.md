## 关于闭包和块级作用域的一道面试题
```javascript
function fn(){
    var arr = [];
    for(var i=0; i<3; i++){
        arr.push(function(){
          return i;
        });
    }
    return arr;
}

var func = fn();
console.info(func[0]());  //3
console.info(func[1]());  //3
console.info(func[2]());  //3
```
以上代码，func是一个长度为3的数组，执行数组每一项的结果均为3，如果想依次输出i的值，并且兼容IE6，可以使用闭包，如下
```javascript
function fn(){
    var arr = [];
    for(var i=0; i<3; i++){
        (function(k){
            arr.push(function(){
               return k;
            });
        })(i);
    }
    return arr;
}
var func = fn();
console.info(func[0]());  //0
console.info(func[1]());  //1
console.info(func[2]());  //2
```
如果想依次输出i的值，并且不考虑兼容IE6，可以使用let，如下
```javascript
function fn(){
    let arr = [];
    for(let i=0; i<3; i++){
        arr.push(function(){
           return i;
        });
    }
    return arr;
}
var func = fn();
console.info(func[0]());  //0
console.info(func[1]());  //1
console.info(func[2]());  //2
```




```javascript
console.log(1);
new Promise(function (resolve, reject){
    reject(true);
    window.setTimeout(function (){
        resolve(false);
    }, 0);
}).then(function(){
    console.log(2);
}, function(){
    console.log(3);
});
console.log(4);
```
可以知道，当promise调用了reject(true)方法，则传递true这个参数给'then'指定的onRejected函数，即题目中的function(){console.log(3);}。但由于.then中指定的方法调用是异步执行的，所以会先执行console.log(4);结果是：1 4 3
## 异步执行
```javascript
var runAsync = function(){
    var promise = new Promise(function(resolve,reject){
        setTimeout(function(){
            resolve('success');
        }, 3000);    //模拟异步请求服务器，请求时间为3s
    });
    return promise;
}
console.info(111);
var prom = runAsync();
prom.then(function(value){
    console.info(value);
})
console.info(222);
/*
111
222
success
*/
```
## 异步执行 async/await
```javascript

```


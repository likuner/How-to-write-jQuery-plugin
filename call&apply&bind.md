## call&apply&bind
### call和apply用法相似，作用都是`借用函数`并`改变执行的上下文`（this指向），例如：
```javascript
var obj1 = {
  n : 11,
};
var obj2 = {
  n : 12,
  getNum : function(){
    console.info(this.n);
  }
};

obj1.getNum();  //报错, obj1对象没有getNum方法
obj2.getNum.call(obj1);  //11, 本身没有getNum方法，借用obj2的getNum方法，并把this指向自己
obj2.getNum.apply(obj1);  //同上
```
call与apply有两点作用：1、改变函数执行的上下文（改变this）；2、使用call或apply，可以调用本身没有的一些方法。唯一不同的是，若需传参，call需要把参数按顺序传递进去，而apply则是把参数放在数组里。

### 使用bind方法，同样可以重新指定this，不同的是使用bind时，`并不是立即执行`，此时会返回一个新函数，调用这个新函数，此时，this的指向就是刚才bind()方法执行时，传入的参数的执行上下文，例如：
```javascript
var obj3 = {
  n : 13,
};
var obj4 = {
  n: 14,
  getNum : function(){
    console.info(this.n);
  }
}

obj3.getNum();  //报错，obj3没有getNum方法
var getNum_ = obj4.getNum.bind(obj3);  得到一个新函数getNum_，this指向obj3
getNum_();  //13
```
bind和call、apply的区别：当你希望改变上下文环境之后并非立即执行，而是回调执行的时候，使用 bind() 方法。而 apply/call 则会立即执行函数。

```javascript
var Core = {
    reg : 'core',
    say : function(){
        return this.reg;
    }
}
reg = 'window';
var fn = Core.say;

console.info(fn());  //window
console.info(fn.call(Core));  //core
console.info(fn.apply(Core));  //core
console.info(fn.bind(Core)());  //core
```

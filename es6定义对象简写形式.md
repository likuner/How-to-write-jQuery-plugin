```javascript
var name = 'peter';

//bad
var obj = {
    name : name,
    age : 26,
    sayName : function(){
        return this.name;
    }
};

//unaccepted
var obj = {
    name,
    age : 26,
    sayName : ()=>{
        return this.name;  //this指向window,没有指向obj
    }
};

//best
var obj = {
    name,
    age : 26,
    sayName(){
        return this.name;  //this指向obj
    }
};
```

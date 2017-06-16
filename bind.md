### bind()用于指定函数的执行上下文(this)，并返回一个新的具有相同功能的函数，不立即执行，例如：
```javascript
  // Create an object that contains the original function.
  var originalObject = {
      minimum: 50,
      maximum: 100,
      checkNumericRange: function (value) {
          if (typeof value !== 'number')
              return false;
          else
              return value >= this.minimum && value <= this.maximum;
      }
  }

  // Check whether 10 is in the numeric range.
  var result = originalObject.checkNumericRange(10);
  document.write(result + " ");
  // Output: false

  // The range object supplies the range for the bound function.
  var range = { minimum: 10, maximum: 20 };

  // Create a new version of the checkNumericRange function that uses range.
  var boundObjectWithRange = originalObject.checkNumericRange.bind(range);  //bind用法，多了一次执行过程
  var result = boundObjectWithRange(10);
  // var result = originalObject.checkNumericRange.call(range,10);  //call用法
  // var result = originalObject.checkNumericRange.apply(range,[10]);  //apply用法
  document.write(result);
  // Output: true
  
```

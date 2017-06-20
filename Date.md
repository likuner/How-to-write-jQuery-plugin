### Date对象获取时间戳的两种方法
#### 1970年1月1日距当前时间的毫秒数
```javascript
Date.now();
```
#### 1970年1月1日距指定时间的毫秒数,不传参数默认为当前时间
```javascript
var date = new Date('1991-03-24');
date.getTime();
```

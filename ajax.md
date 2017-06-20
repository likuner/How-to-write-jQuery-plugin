### JS原生ajax请求
#### 1.创建ajax对象
```javascript
if(window.XMLHttpRequest){
  var xhr = new XMLHttpRequest();
}else{
  var xhr = new ActiveXObject("Microsoft.XMLHTTP");  //IE6
}
```
#### 2.连接服务器
```javascript
xhr.open("get","http://192.168.1.1?name=peter&ts="+Date.now(),true);  //加上时间戳Date.now()，去除缓存
```
open()方法有三个参数：请求方式get/post，请求的地址及参数，是否异步操作
#### 3.发送请求
```javascript
xhr.send();
```
#### 4.接收服务端的返回信息
```javascript
xhr.onreadystatechange = function(){
  if(xhr.readyState==4 && xhr.status==200 || xhr.status==304){
    console.info(xhr.responseText);  //请求成功，打印返回的数据
  }else{
    console.error('error');  //请求失败
  }
};
```
客户端和服务端有交互时，会调用xhr.onreadystatechange，xhr.reafyState用来说明客户端和服务端交互到哪种程度了，
xhr.readyState有5个值：0表示未初始化，还没有调用open()方法；1表示已经调用send()方法，正在发送请求；2表示send()方法完成，已收到响应内容；
3表示正在解析响应内容；4表示响应内容解析完成，可以在客户端使用。
####　以上代码组合起来
```javascript
if(window.XMLHttpRequest){
  var xhr = new XMLHttpRequest();
}else{
  var xhr = new ActiveXObject("Microsoft.XMLHTTP");  //IE6
}

xhr.open("get","http://192.168.1.1?name=peter&ts="+Date.now(),true);

xhr.send();

xhr.onreadystatechange = function(){
  if(xhr.readyState==4 && xhr.status==200 || xhr.status==304){
    console.info(xhr.responseText);  //请求成功，打印返回的数据
  }else{
    console.error('error');  //请求失败
  }
};
```


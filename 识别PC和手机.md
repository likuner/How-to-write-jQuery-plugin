```javascript
<script type="text/javascript">
    (function(){
        var ua = window.navigator.userAgent.toLowerCase();
        if (!(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent))) {
           //window.location.href = "pc";
        }else if (ua.indexOf("iphone") > 0 || ua.indexOf("android") > 0) {
           //window.location.href = "mobile"; 
        } 
    }());
</script>
```

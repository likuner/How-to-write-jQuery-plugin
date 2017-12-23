```javascript
//返回或设置被选元素的 内容 宽高，以px计的number数值
$("selector").width();
$("selector").height();

//返回被选元素的 内容+padding 宽高，以px计的number数值
$("selector").innerWidth();
$("selector").innerHeight();

//返回被选元素的 内容+padding+border 宽高，以px计的number数值
$("selector").outerWidth();
$("selector").outerHeight();

//返回被选元素的 内容+padding+border+margin 宽高，以px计的number数值
$("selector").outerWidth(true);
$("selector").outerHeight(true);


//返回或设置被选元素相对于当前文档的偏移坐标，返回值或参数是包含top和left两个属性的对象，
//top和left的属性值是以px计的number数值
var offset = $("selector").offset();
var top = offset.top;
var left = offset.left;

//返回被选元素相对于父元素的偏移坐标，返回值是包含top和left两个属性的对象，
//top和left的属性值是以px计的number数值
var offsetParent = $("selector").position();
var topParent = offsetParent.top;
var leftParent = offsetParent.left;


//返回或设置被选元素（例如document）相对于滚动条顶部和左侧的偏移，返回值或参数是以px计的number数值
$("selector").scrollTop();
$("selector").scrollLeft();
```

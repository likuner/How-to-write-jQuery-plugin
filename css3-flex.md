/*CSS的4种布局:标准文档流布局、浮动布局、定位布局、flex布局,以下是flex布局知识:*/
```css
father
  display: flex;
  flex-direction: row/row-reverse/column/column-reverse; /*规定弹性盒子的布局方式 l-r/r-l/t-b/b-t*/
  justify-content: flex-start/flex-end/center/space-between/space-around; /*水平方向上的对齐方式*/
  align-items: flex-start/flex-end/center/stretch/baseline; /*垂直方向上的对齐方式*/
son
  flex: number; /*子容器的伸缩比例,数字或者是none*/
  align-self: flex-start/flex-end/center/stretch/baseline; /*设置子容器如何沿垂直方向排列,优先级高于父容器的align-items*/
```
/*以上为flex布局的基础知识,进阶知识...啊...有点复杂...以后补上...静待...*/


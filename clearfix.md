```html
<html>
    <head>
        <style>
            .clearfix {
                display: block;
                zoom: 1;
            }
            .clearfix:after {
                content: " ";
                display: block;
                font-size: 0;
                height: 0;
                clear: both;
                visibility: hidden;
            }
            .container{
                width: 100%;
                position: relative;
            }
            .content{
                position: absolute;
                z-index: 1;
                top: 0;
                bottom: 0;
                width: 100%;
                height: 100%;
                background: darkcyan;
            }
            .place{
                margin-bottom: 50%;  /*宽高比为2:1，可以设置任意比例*/
                float: left;
            }
        </style>
    </head>
    <body>
        <div class="container clearfix">
            <div class="content"></div>
            <div class="place"></div>
        </div>
    </body>
</html>
```

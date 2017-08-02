# holyGridLayout
圣杯布局

点击链接查看效果：https://linlif.github.io/holyGridLayout/

**html代码：**

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>圣杯布局</title>
    <link rel="stylesheet" href="app.css" type="text/css">
  </head>
  <body>
    <header id="header">header</header>

    <div id="main">
      <div class="center">圣杯布局</div>
      <div class="left">left</div>
      <div class="right">right</div>
    </div>

    <footer id="footer">footer</footer>
  </body>
</html>
```

**CSS代码：**

```css
*{
  margin: 0;
  padding: 0;
}
body{
  font-size: 30px;
  color: white;
  text-align: center;
  min-width: 650px;
}

#header,#footer{
  background-color: #303030;
  height: 80px;
  line-height: 80px;
}

#main{
  padding-left: 200px;
  padding-right: 340px;
}

#main .center{
  float: left;
  width: 100%;
  padding: 0 20px;
  background-color: #38b174;
  min-height: 600px;
}

#main .left{
  float: left;
  width: 180px;
  padding:0 10px;
  background-color: #289ad2;
  min-height: 600px;
  margin-left: -100%; /*偏移到center的左侧*/
  position: relative;
  left: -240px; /*向左偏移240像素*/
}

#main .right{
  float: left;
  background-color: #abc444;
  width: 300px;
  padding: 0 10px;
  min-height: 600px;
  margin-right: -360px; /*偏移到center的右侧*/
  position: relative; /*设置为相对定位，使其脱离文档流*/
  /*right:-360px; 注意，这里无需设置right或left了*/
}


#footer{
  clear: both;
}

* html #left { /*ie hack*/
  left：150 px; /* right宽 */
}
```



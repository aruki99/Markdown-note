# css

## 简介

- CSS 指层叠样式表 (**C**ascading **S**tyle **S**heets)
- 样式定义**如何显示** HTML 元素
- 样式通常存储在**样式表**中
- 把样式添加到 HTML 4.0 中，是为了**解决内容与表现分离的问题**
- **外部样式表**可以极大提高工作效率
- 外部样式表通常存储在 **CSS 文件**中
- 多个样式定义可**层叠**为一个

## 使用方法

### 规范

在<style>中编写css代码
    每一个声明，最好s使用分号结尾
        语法
            选择器{
                声明1;
                声明2;
                声明3;
            }

### 外部导入

```html
<link rel="stylesheet" href="css/style.css">
```

### 内部使用

写在**<style></style>>**之间的内容则为css部分

## 标签选择器

 . + class 为class选择器

**#** + id 为id选择器

```css
<style>

    /*类选择器的格式，class的名称
    好处多个标签分类，如果是同一个标签可以重复使用*/
    .yjx{
        color: #002fff;
    }
    .ceshi{
        color: #ff000f;
    }
</style>
```

## 层次选择器

```html
<body>
<p>p0</p>
<p class="cheshi">p1</p>
<p>p2</p>
<p class="cheshi">p3</p>
<ul>
    <li>
        <p>p4</p>
    </li>
    <li>
        <p>p5</p>
    </li>
    <li>
        <p>p6</p>
    </li>
</ul>
<p>p7</p>
<p>p8</p>
</body>
```

后代选择器,选择某个元素后面的所有元素.

```css
 body p{
            background: #ff000f;
        }
```

子选择器,只选择当前元素的所有下一级

```css
body>p{
    background: #a700ff;
}
```

下一个元素选择器,只选择后一个元素

.class名称+标签名{

}

```css
.cheshi + p{
    background: darkgreen;
}
```

向下所有同级元素选择器

.class名称~标签名{

}

```css
.cheshi~p{
    background: hotpink;
}
```



## 结构伪类选择器

```html
<body>
<a href="">214413</a>
<h1>拉拉拉</h1>
<p>p1</p>
<p>p2</p>
<p>p3</p>

<ul>
    <li>li1</li>
    <li>li2</li>
    <li>li3</li>

</ul>

<p>p7</p>
<p>p8</p>
</body>
```

选择 ul 的最后一个子元素

```css
ul li:last-child{
    background: #ff000f;
}
```

选择 ul 的第一个子元素

```css
ul li:first-child{
    background: #002fff;
}
```

选着当前p元素的父级元素，并选中父级元素的第一个元素，并且是当前元素才生效！

```css
p:nth-child(1){
    background: darkgreen;
}
```

选择p类型

```css
p:nth-of-type(2){
    background: yellow;
}
```



:hover 当鼠标选择并触碰此选项时的状态 

```css
a:hover{
    background: darkgreen;
}
```







## 属性选择器

```css
<style>
		/*选中拥有id的元素*/
        a[id]{
            background: #ff000f;
        }

        /*选中id=lalala*/
        a[id=lalala]{
            background: hotpink;
        }

        /*class为int的元素*/
        a[class=int]{
            background: deepskyblue;
        }

        /*class中含有int的元素*/
        a[class*=int]{
            background: deepskyblue;
        }

        /*href以h开头的元素*/
        a[href^=h]{
            background: coral;
        }

        /*$
        以ef什么结尾*/
        a[href$=ef]{
            background: #a700ff;
        }
    </style>
```





## 美化网页

```css
font-family 字体
font-size   字体大小
font-weight 字体粗细
color 字体颜色
text-align: center; 排版居中
text-indent: 2em;    文章开头空两个文字的位置
行高，块高的高度一致即可上下居中
line-height 行高
height      块高
text-decoration: underline;  下划线
text-decoration: line-through; 穿过文字的划线
text-decoration: overline;   顶端划线

 <style>
        /*水平对齐，参照物  a，b
        span参照img对齐
        */
        img,span{
            vertical-align: middle;
        }
        a{
            text-decoration: none;
        /*超链接去除下划线*/
        }
</style>
```



## 超链接伪类

```css
/*鼠标悬浮时文字状态*/
a:hover{
/*重点，多用*/
color: #ff000f;
font-size: 20px;
}
/*鼠标点击时文字状态*/
a:active{
color: #00ff07;
}
#price{
/*阴影颜色、水平位移、垂直便宜、阴影半径*/
text-shadow: red 5px 5px 1px;
}
```



## 图片背景

```css
<style>
        div{
            width: 1000px;
            height: 700px;
            /*边框粗细、边框样式、边框颜色*/
            border: 1px solid red;
            /*默认平铺*/
            background-image:url("../images/shu.jpg");
        	}
        .div1{
            /*横轴方向铺开，只有一行*/
            background-repeat: repeat-x;
        }
        .div2{
            /*竖轴方向铺开，只有一列*/
            background-repeat: repeat-y;
        }
        .div3{
            /*只显示一张*/
            background-repeat: no-repeat;
        }
        .div4{
            /*铺满整个框框*/
            background-repeat: repeat;
        }
</style>
```

## 背景渐变

```css
body{
     background-color: #ffffff;
     background-image: linear-gradient(45deg, #ffffff 0%, #2b6cff 52%, #000000 90%);
     /*https://www.grabient.com/
     渐变网站
     */
}
```



## 解决父级边框塌陷

```css
<style>
       #lala{
            /*overflow:scroll;   限制大小，若显示不完整则产生滚动条
             overflow: hidden;  限制大小，超出限制地方会无法显示
             默认会超出限制范围继续显示
             */
            width: 200px;
            height: 300px;
            border: 1px solid red ;
        }
        #lala{
            content: '';
            display: block;
            clear: both;
        }
    </style>

<div id="lala">
    <img src="../images/a.jpg" alt="" width="300" height="200">
    <p>
        你矮树答dsadasdasddddddddddddddddddddddddd复年卡买了我可没弗兰克米勒
    </p>
</div>
```

![image-20200814112410092](C:\Users\喻嘉兴\AppData\Roaming\Typora\typora-user-images\image-20200814112410092.png)

## 定位

position 属性的五个值：

- [static](https://www.runoob.com/css/css-positioning.html#position-static)(默认的，无定位)

- [relative](https://www.runoob.com/css/css-positioning.html#position-relative)(相对原来位置的定位)

- [fixed](https://www.runoob.com/css/css-positioning.html#position-fixed)(固定定位，相对浏览器边框)

- [absolute](https://www.runoob.com/css/css-positioning.html#position-absolute)(绝对定位，相对于浏览器)

- [sticky](https://www.runoob.com/css/css-positioning.html#position-sticky)

  - 基于用户的滚动位置来定位。

    粘性定位的元素是依赖于用户的滚动，在 **position:relative** 与 **position:fixed** 定位之间切换。

    它的行为就像 **position:relative;** 而当页面滚动超出目标区域时，它的表现就像 **position:fixed;**，它会固定在目标位置。



### 练习

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>练习</title>
    <style>

        #father{
            padding: 7px;
            border: 2px solid black;
            width: 300px;
            height: 300px;
            margin:250px auto;
            border-radius: 20px;
            background-color: #37ff00;
            background-image: linear-gradient(45deg, #37ff00 0%, #21cda0 46%, #fff600 100%);
        }
        a{
            border: 1px solid black;
            background-color: yellow;
            text-align: center;
            line-height: 100px;
            width: 100px;
            height: 100px;
            display: block;
            text-decoration: none;
            border-radius: 20px;
        }
        #l1{
            position: relative; /*相对定位，必须写*/
            top: -3px;
            left: -2px;
        }
        #l2,#l4{
            position: relative; /*相对定位，必须写*/
            left: 200px;
            top: -106px;
        }
        #l5{
            position: relative; /*相对定位，必须写*/
            left: 99px;
            top: -310px;
        }
        #l3{
            position: relative; /*相对定位，必须写*/
            top: -4px;
            left: -2px;
        } 	
        a:hover{
            background-color: gold;
        }
        #l1,#l2,#l3,#l4,#l5:hover{
            color: black;
        }
    </style>
</head>
<body>
<div id="father">
    <a href="https://www.baidu.com/?tn=78000241_9_hao_pg" id="l1">百度</a>
    <a href="https://www.bilibili.com/" id="l2">B站</a>
    <a href="https://www.runoob.com/" id="l3">菜鸟</a>
    <a href="hhttp://music.migu.cn/v3" id="l4">咪咕</a>
    <a href="https://www.baidu.com/?tn=78000241_9_hao_pg" id="l5">拉拉</a>
</div>
</body>
</html>
```

<img src="C:\Users\喻嘉兴\AppData\Roaming\Typora\typora-user-images\image-20200814115434263.png" alt="image-20200814115434263" style="zoom:50%;" />

## z-index 图层

```css
z-index:99;  层级第99级
```

级数越高，显示优先级越高！

## display（行与块的转化）

```css
display block;变成块元素
display inline;变成行内元素
display inline——block; 保持块元素特性，但是能写在一行
display none; 不存在，消失


float:right;	靠右侧浮动
float:left;		靠左侧浮动


clear both 左右两侧不允许浮动
clear left 左侧不允许浮动
clear right 右侧不允许浮动
```


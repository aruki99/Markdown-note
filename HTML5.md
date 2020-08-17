

# HTML5	

## 简介

超文本标记语言（英语：HyperText Markup Language，简称：HTML）是一种用于创建网页的标准标记语言。

​	您可以使用 HTML 来建立自己的 WEB 站点，HTML 运行在浏览器上，由浏览器来解析。



HTML 是用来描述网页的一种语言。

- HTML 指的是超文本标记语言: **H**yper**T**ext **M**arkup **L**anguage
- HTML 不是一种编程语言，而是一种**标记**语言
- 标记语言是一套**标记标签** (markup tag)
- HTML 使用标记标签来**描述**网页
- HTML 文档包含了HTML **标签**及**文本**内容
- HTML文档也叫做 **web 页面**



## 标签

标签由<>包裹着，并且成对出现。

第一个标签为“开始标签”（开放标签）

第二个标签为“结束标签”（闭合标签）





### 特殊字符

&nbsp 空格

&gt 大于符号

&lt 小于符号 

&copy 版权所有符号





### 基本标签

```html
<head>
<!--   meta描述性标签，用来描述我们网站的一些信息 -->
<!--    meta易班用来做SEO-->
    <meta charset="UTF-8">
    <meta name="keywords" content="喻嘉兴\java html 练习">
    <meta name="description" content="我来练习我的html">
```

- **<!DOCTYPE html>** 声明为 HTML5 文档
- **<html>** 元素是 HTML 页面的根元素
- **<head>** 元素包含了文档的元（meta）数据，如 **<meta charset="utf-8">** 定义网页编码格式为 **utf-8**。
- **<title>** 元素描述了文档的标题，网页标题
- **<body>** 元素包含了可见的页面内容，主体
- **<h1>** 元素定义一个大标题（h1,h2,h3....h6）
- **<p>** 元素定义一个段落
- **<hr/>**水平线标签
- **<br/>**换行标签
- **<strong>**粗体文字
- **<em>**斜体字体





### 图像标签

```html
<!--img学习
src 图片地址
    相对地址(推荐使用)
    ../     上级目录
    绝对地址（从根目录开始写）
-->
<img src="../resources/image/1.png" alt="图片加载失败时的代替文字（图片名称）"title="悬停在图片上方显示的文字"width="300"height="200">
<a href="4、链接标签.html#down"target="_blank">跳转到底部</a>
```

img 导入

src 地址

alt="图片加载失败时的代替文字（图片名称）

"title="悬停在图片上方显示的文字"





### 链接标签

**<a>**链接标签

在**<a>**之间插入图片，即可称为拥有链接跳转功能的图片**</a>**

```HTML
<a href="https://www.baidu.com/?tn=88093251_28_hao_pg"target="_blank">点击我跳转到百度</a> <br/>
```

href 被链接的地址

```HTML
target="_blank"
```

在新的页面打开此链接

```html
target="_self"
```

在此页面打开此链接





### 功能性链接

#### 邮件链接

```HTML
<a href="mailto:862615422@qq.com">点击联系我</a><br/>
```

#### QQ推广

```html
<a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=&site=qq&menu=yes">
    <img border="0" src="http://wpa.qq.com/pa?p=2::52" alt="你好，联系我领取福利！" title="你好，联系我领取福利！"/>
</a>
```

百度“QQ推广” 即可获得代码



#### 锚链接

1、需要一个标记锚点

2、需要在跳转出进行标记

```html
<a name="top">顶部</a><br/>
此部分为 标记顶部
<a href="#top">回到顶部</a>
点击此部分即可回到 被标记且名为“顶部”的位置
```





## 列表

#### 有序列表

<img src="C:\Users\喻嘉兴\AppData\Roaming\Typora\typora-user-images\image-20200724160401327.png" alt="image-20200724160401327" style="zoom:50%;" />

```html
<!--有序列表-->
<ol>
    <a href="https://baike.baidu.com/item/Java/85979?fr=aladdin"target="_blank"><li>java</li></a>
    <a href="https://www.python.org/"target="_blank"><li>python</li></a>
    <a href="https://tieba.baidu.com/f?kw=web&fr=ala0&tpl=5&traceid="><li>web</li></a>
    <a href="https://baike.baidu.com/item/c%E8%AF%AD%E8%A8%80/105958?fr=aladdin"><li>c</li></a>
    <a href="https://baike.baidu.com/item/C%2B%2B/99272?fromtitle=c%2B%2B%E8%AF%AD%E8%A8%80&fromid=4102088&fr=aladdin"><li>c++</li></a>
    <a href="https://baike.baidu.com/item/%E7%BD%91%E7%BB%9C%E5%AE%89%E5%85%A8"><li>网络安全</li></a>
</ol>
```



#### 无序列表

<img src="C:\Users\喻嘉兴\AppData\Roaming\Typora\typora-user-images\image-20200724160438114.png" alt="image-20200724160438114" style="zoom:50%;" />

```html
<ul>
    <a href="https://baike.baidu.com/item/Java/85979?fr=aladdin"target="_blank"><li>java</li></a>
    <a href="https://www.python.org/"target="_blank"><li>python</li></a>
    <a href="https://tieba.baidu.com/f?kw=web&fr=ala0&tpl=5&traceid="><li>web</li></a>
    <a href="https://baike.baidu.com/item/c%E8%AF%AD%E8%A8%80/105958?fr=aladdin"><li>c</li></a>
    <a href="https://baike.baidu.com/item/C%2B%2B/99272?fromtitle=c%2B%2B%E8%AF%AD%E8%A8%80&fromid=4102088&fr=aladdin"><li>c++</li></a>
    <a href="https://baike.baidu.com/item/%E7%BD%91%E7%BB%9C%E5%AE%89%E5%85%A8"><li>网络安全</li></a>
</ul>
```



#### 自定义列表

<img src="C:\Users\喻嘉兴\AppData\Roaming\Typora\typora-user-images\image-20200724160621869.png" alt="image-20200724160621869" style="zoom:50%;" />

```html
<dl>
    <dt>名称</dt>

    <dd>喻嘉兴</dd>
    <dd>庞伟怡</dd>
    <dd>什么鬼</dd>
    <dd>还好</dd>

</dl>
```

dt  标题名称
dd  标题集合



## 表格学习

```html
<table border="5">
```

边框宽度

tr 行		td	列

colspan	跨列

rowspan 	跨行

<img src="C:\Users\喻嘉兴\AppData\Roaming\Typora\typora-user-images\image-20200724161440091.png" alt="image-20200724161440091" style="zoom:50%;" />

```html
<body>
<!--表格table
    行 tr
    列 td
    border 边框 数值为宽度
-->
    
</table>

    <table border="2">
        <hr/>
    <tr>
        <td colspan="3">成绩</td>
    </tr>
    <tr>
        <td rowspan="2">喻嘉兴</td>
        <td>语文</td>
        <td>100</td>
    </tr>
    <tr>
        <td>数学</td>
        <td>99</td>
    </tr>
    <tr>
        <td rowspan="2">吴彦祖</td>
        <td>语文</td>
        <td>66</td>
    </tr>
    <tr>
        <td>数学</td>
        <td>55</td>
    </tr>

</table>
</body>
```





## 媒体元素

#### 视频

```html
<video src="../resources/video/1.mp4"controls width="750"height="500"></video>
```

src 路径

outoplay 自动播放

controls 视频控制器



#### 音乐

```html
<audio src="../resources/audio/不用去猜.mp3" autoplay></audio>
```

autoplay 自动播放音乐



## 页面结构

```html
<header>
    <h2>网页头部</h2>
</header>
```

网页头部

```html
<section>
    <h2>网页主体</h2>
</section>
```

网页主体

```html
<footer>
    <h2>网页脚部</h2>
</footer>
```

网页脚部





## 内联框架

```html
<body>
<!--跳转百度-->
<!--<iframe src="https://www.baidu.com/?tn=02003390_2_hao_pg" frameborder="0"height="500"width="750"></iframe>-->
<!--跳转B站视频-->
<!--<iframe src="//player.bilibili.com/player.html?aid=55631961&bvid=BV1x4411V75C&cid=97257967&page=11"-->
<!--        scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true">-->
<!--</iframe>-->

<iframe src=""name="喻嘉兴跳转" frameborder="0"height="500"width="750"></iframe>
<a href="1、我的第一个网页.html" target="喻嘉兴跳转">点击跳转</a>
</body>
```





## 表单学习

```html
<!--表单form
    action 表单处理位置，可以是一个网站，也可以是一个请求处理地址
    method 提交方式
        get 这种方式，在url中可以看到账号与密码，不安全，但是高效
        post 这种方式，在url中看不到账号与密码，安全，可以传输大文件
-->
<form action="1、我的第一个网页.html" method="get">
```

#### 输入账户与密码

```html
<!--文本输入框：input type=“text”-->
<!--value="喻嘉兴好困"   默认值
    maxlength="10"      最长能写几个字符串
    size="40"           文本框长度
    readonly            只读
    required            必须填写
    placeholder="文本框输入提示"
    -->
<p>名字 : <input type="text" name="username" required ></p>
<!--密码框：input type=“password”-->
<p>密码 : <input type="password"name="pwd"value="123456" hidden></p>
```

#### 单选框

```html
<!--单选框标签
    input type="radio"
    value ：单选框的值
    name ： 表示组，单项需要组名name相同，否则为多选
    disabled    禁选
    hidden      隐藏
-->
<p>
    <input type="radio"value="boy"name="sex"/>男
    <input type="radio"value="girl"name="sex"/>女
</p>
```

#### 多选框

```html
<!--多选框
    input type=“checkbox”
    checked 默认选择
-->
    <p>
        <input type="checkbox"value="sleep"name="hobby">睡觉
        <input type="checkbox"value="code"name="hobby"checked>敲代码
        <input type="checkbox"value="chat"name="hobby">聊天
        <input type="checkbox"value="game"name="hobby">游戏
        <input type="checkbox"value="eat"name="hobby">吃
    </p>
```

#### 自定义按钮

```html
<!--自定义按钮
input type="button" 普通按钮
input type="image"  图像按钮
-->
    <p>按钮
        <input type="button"name="btn1"value="点击变长"><br/>
        <input type="image"src="../resources/image/1.png"width="150"height="100">
    </p>
```

#### 下拉框，列表框

```html
<!--下拉框，列表框
    selected 默认选择
-->
    <p>国家
        <select name="列表名称">
            <option value="选择">中国</option>
            <option value="选择">美国</option>
            <option value="选择"selected>日本</option>
            <option value="选择">印度</option>
            <option value="选择">俄罗斯</option>
        </select>
    </p>
```

#### 文件域

```html
    textarea
    cols 列 rows 行
-->
    <p>反馈：
        <textarea name="textarea" cols="50" rows="10">文本内容

        </textarea>
    </p>

<!--文件域-->
    <p>上传文件
        <input type="file"name="files"><br/>
        <input type="button"value="上传文件"name="upload">
    </p>
```

#### 邮箱认证

```html
<!--邮箱验证-->
    <p>邮箱
        <input type="email"name="email" placeholder="请输入你的验证邮箱"required>
    </p>
```

#### url验证

```html
<!--url验证-->
    <p>url验证
        <input type="url"name="url"required>
    </p>
```

#### 滑块

```html
<!--滑块-->
    <p>音量
        <input type="range"name="range"max="100"min="0"step="2">
    </p>
```

#### 点击文字自动选择文本

```html
<!--增强鼠标可用性-->
    <p>
        <label for="mark">你点我试试</label>
        <input type="text" id="mark">
    </p>
```

#### 搜索框

```html
<!--搜索框
    disabled    禁用
    -->
    <p>搜索
        <input type="search"name="search"disabled>
    </p>
```

#### 自定义邮箱

```html
<!--自定义邮箱-->
    <p>自定义邮箱
        <input type="text"name="diyemail"pattern="/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
/^[a-z\d]+(\.[a-z\d]+)*@([\da-z](-[\da-z])?)+(\.{1,2}[a-z]+)+$/或\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*">
    </p>
```

#### 提交、清空表单

```html
<p>
    <input type="submit"value="提交">
    <input type="reset"value="清空表单">
</p>
```
# JavaScript

## 简介

JavaScript 是 Web 的编程语言, 是互联网上最流行的脚本语言。

所有现代的 HTML 页面都使用 JavaScript。

## JavaScript的使用

### 内部

```javascript
<script>
    'use strict'  //严格检查模式
</script>
```

JavaScript代码写在<script>之间

1、放在<body>中

2、放在<head>中

### 外部

可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。

外部 JavaScript 文件的文件扩展名是 .js。

如需使用外部文件

方法一、

请在 <script> 标签的 "src" 属性中设置该 .js 文件：

```html
<body> 

<script src="myScript.js"></script>

 </body>
```



方法二、

你可以将脚本放置于 <head> 或者 <body>中，放在 <script> 标签中的脚本与外部引用的脚本运行效果完全一致。

myScript.js 文件代码如下：



```JavaScript
function myFunction() {    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数"; }
```





## 基本语法

普通变量

```js
<script>
    'use strict';
    // 1、定义变量   
    变量类型    变量名  =   变量
    var number=10;
    var string='你好啊';
    var number2=20;

    //alert 弹窗
    //console.log（number）   在浏览器控制台打印number
    //Math.abs() 为求 绝对值
    alert(number+number2);      //数学运算
    alert(string+number2);      //字符串拼接
	alert(string.length)//          输出字符串长度
    alert(string.toLocaleUpperCase())
	//以大写形式输出
    alert(string.indexOf('a'))        
	//此字符在字符串中第几个出现
    alert(string.substring(1))          
	//截取此元素后面的所以
    alert(string.substring(3,6))         
	//截取3到5元素



</script>
```



定义数组变量

```js
<script>
var s=[2,4,5,'das','dsdd'];
    s.push('yes',34)      //在此数字最后加上额外元素

    s.pop()                 //删除尾部的一个元素

    s.unshift('a','b')            //在头部插入元素

    s.shift() 				//删除头部第一个元素

    s.sort()                    //排序数组

    s.reverse()                 //元素反转

    s.concat(123,412,'23da')      
		//并没有改本原本数组，只是返回一个新的数组

    s.join('-')             //使用特定的符号打印并拼接数组

</script>
```



## 函数

方法一

```js
<script>
    'use strict';
    const a=23;     //定义常量
    function way(x) {
        //手动抛出异常，来规避错误
        if(typeof x!= 'number'){
            throw '输入值不为数字';
        }
        console.log('x=>'+x);
        //arguments 代表传递进来的参数，是一个数组。
        for(var i = 0; i<arguments.length;i++){
            console.log(arguments[i])
        }
        if(x>=0){3
            return x;
        }else{
            return -x;
        }
    }
alert(way(0-9));
</script>
```

方法二

```js
<script>
var way =function(x){
    if(x>=0){
        return x;
    }else{
        return -x;
    }
}
alert(way(0-9));
</script>
```

### es6新特性

```js
 //rest es6引入的新特性，获取除了定义参数以外的所有参数
    function yjx(a,b,...rest) {
        console.log(a);
        console.log(b);
        console.log(rest)
    }
</script>
```



## date日期时间

```js
<script>
    'use strict';
    var now = new Date();
    now.getFullYear();      //年
    now.getMonth();         //月 0-11月
    now.getDate();          //日期
    now.getDay();           //星期几
    now.getHours();         //小时
    now.getMinutes();       //分钟
    now.getSeconds();       //秒数

    now.getTime();    //时间戳
    alert(new Date(now.getTime()))          //获取当前时间
</script>
```

## class继承

```js
<script>
    class students{
        constructor(name) {
            this.name = name;
        }
        hello(){
            alert('hello')
        }
    }
    class xiaoxueshen extends students{
        constructor(name,grade) {
            super(name);
            this.grade = grade;
        }
        mygrade(){
            alert('我是一个小学生')
        }
    }
    
    var xiaoming = new students('xiaoming');
    var xiaohong =new xiaoxueshen('xiaohong',1);
    xiaohong.hello();
</script>
```

## 操作bom对象

例子

```js
<body>

<div id="father">
    <h1>标题一</h1>
    <p id="p1">p1</p>
    <p class=p2">p2</p>
</div>


<script>
    //获取节点
    var h1 = document.getElementsByTagName('h1');
 var p1 = document.getElementById('p1');
 var p2 = document.getElementsByClassName('p2');
 var father = document.getElementById('father');

    var children = father.children; 
			//获取父节点下的所有子节点
    //father.firstChild;   父节点后的第一个节点
    //father.lastChild;    父节点后的最后一个节点

    //更新节点
    //p1.innerText='更新节点';   
	//将原先 p1的文字改成 ‘更新节点’  只有拥有 id标签的才能这样用
    // p1.innerHTML = '<strong>更新节点的底层代码</strong>';
    // p1.style.color='red' //更新文字颜色，利用css
    // p1.style.fontSize='100px'  //更新文字大小


    //删除节点
    //father.removeChild(p1)   //删除父节点中的 p1    并且都拥有id标签
    //删除是个动态的过程
    //father.removeChild(father.children[1])         //删除父节点中 序号为1 的节点
    //删除过程中，children是在变化的，下标会实时改变


    //插入节点
    //我们h获得了m某个Dom节点，假设这个dom节点是空的，我们通过innerHtml就可以增加一个元素
    // 但是若这个DOM节点已经存在元素了我们就不能这么干，因为会覆盖原先元素。




    // location.assign
    // ƒ assign() { [native code] }
    // location.reload
    // ƒ reload() { [native code] }
    // location.assign
    // ƒ assign() { [native code] }
    // location.protocol
    // "https:"
    // location.assign
    // ƒ assign() { [native code] }
    // location.href
    // "https://www.baidu.com/?tn=88093251_34_hao_pg"
    // location.host
    // "www.baidu.com"
    // document.title
    // "百度一下，你就知道"
    // document.title="你好"
    // "你好"
    // history.back()      //浏览器根据历史 后退
    // history.forward()   //浏览器根据历史 前进
</script>

</body>
```

## 追加、插入对象

```html
<p id="js">JavaScript</p>
<div id="list">
    <p id="se">javase</p>
    <p id="ee">javaee</p>
    <p id="me">javame</p>
</div>
```
```js
<script>
    'use strict';
    var js = document.getElementById('js');
    var list = document.getElementById('list');
    //list.appendChild('js')      //追加到最后面
    //通过js创建新的节点
    var newp = document.createElement('p');
    newp.id = 'newp';
    newp.innerText = 'hello,yjx';
    //再将创建的新节点追加到最后
    list.appendChild(newp);

    //创建一个新标签节点
    var myscript = document.createElement('script');
    myscript.setAttribute('type','text/javaScript')

    //可以创建一个style标签
    var mystyle = document.createElement('style');          //创建了一个空的style标签
    mystyle.setAttribute('type','text/css');
    mystyle.innerText = 'body{background-color: chartreuse;}';      //设置标签内容
    document.getElementsByTagName('head')[0].appendChild(mystyle);


    var ee = document.getElementById('ee');
    var js = document.getElementById('js');
    var list = document.getElementById('list');

    list.insertBefore(js,ee);


</script>
```

## 表单

### 操作表单

```html
<form action="post">
    <p><span>用户名</span>
        <input type="text" id="username" required>
    </p>
    <p>
        <span>性别：</span>
        <input type="radio" name="sex" value="boy" id="boy">男
        <input type="radio" name="sex" value="girl" id="girl">女
    </p>

    <input type="submit">
</form>
```

```js
<script>
    'use strict';
    var input_text = document.getElementById('username')
    //得到输入框信息
    input_text.value
    //修改输入框信息
    input_text.value='修改信息'

    //获取节点
    var boy = document.getElementById('boy');
    var girl = document.getElementById('girl');
    //判断boy是否被选中，选中为true，未选择为false
    boy.checked;
    //也可以通过 boy.checked=true 来选中 boy
</script>
```





### 提交表单

```html
<form action="post">
    <p><span>用户名</span>
        <input type="text" id="username" required>
    </p>
    <p>
        <span>密码：</span>
        <input type="password" id="password">
    </p>

<!--    绑定事件，onclick 被点击时-->
    <button type="button" onclick="tijiao()">提交</button>

<!-- 提交按钮  <input type="submit">-->


</form>
```

```js
<script>
    'use strict';
    function tijiao() {
        var username = document.getElementById('username');
        var password = document.getElementById('password');
        console.log(username.value);
        console.log(password.value);
    }
</script>
```

## jQuery

```html
<!--    插入jQuery  CDN-->
    <script src="http://libs.baidu.com/jquery/2.0.0/jquery.min.js">
</script>
```

最重要，记得插入jQuery

```html
<body>
<a href="" id="yjx" class="yjx" >点我</a>

<script>
    'use strict';
    //选择器就是css的选择器
    $('#yjx').click(function () {
        alert(32)
    })

    //普通js选择器
    document.getElementById()               //id选择器
    document.getElementsByTagName()         //标签选择器
    document.getElementsByClassName()       //class选择器
    document.getElementsByName()            //name选择器

    //jQuery选择器
    $('a').click()              //标签选择器
    $('#yjx').click()           //id选择器
    $('.yjx').click()      //class选择器


</script>
</body>
```





### jQuery事件

在一片区域内获取鼠标位置

```html
<script src="http://libs.baidu.com/jquery/2.0.0/jquery.min.js"></script>
    <style>
        #divmove{
            width: 500px;
            height: 500px;
            border: 1px solid red;
        }
    </style>
</head>
<body>


<!--要求，获取当前鼠标位置的坐标-->
mouse : <span id="move"></span>
<div id="divmove">在这里移动鼠标试试</div>


<script>
    'use strict';
    $(function () {
        $('#divmove').mousemove(function (e) {
            $('#move').text('x:' + e.pageX + 'y' + e.pageY);
        })
    })
</script>
```



### jQuery操作

操作修改网页数据

```html
   <script src="http://libs.baidu.com/jquery/2.0.0/jquery.min.js"></script>

</head>
<body>

<ul id="text">
    <li class="js">JavaScript</li>
    <li name="python">python</li>
</ul>

<script>
    'use strict';

    //获取值
    $('#text li[name=python]').text();
    //修改值
    $('#text li[name=python]').text('修改值');
    $('#text').html();
</script>
```
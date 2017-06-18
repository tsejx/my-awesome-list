# HTML/CSS基础知识 慕课手记


```
1. 文件结构：
    HTML文件的固定结构：

    <html>
        <head>...</head>
        <body>...</body>
    </html>

    html是根标签
    head定义文档头部，包含： title, script, style, link, meta
    body是网页主要内容，包含：h1,h2-h6, p, a, img

2. 认识head标签：

    <head>
        <title>...</title>         网页标题
        <meta>
        <link>
        <style>...</style>
        <script>...</script>
    </head>

3. 语义化：
    明白每个标签的用途（在什么情况下我可以使用这个标签才合理）
        比如，网页上的文章的标题就可以用标题标签，
        网页上的各个栏目的栏目名称也可以使用标题标签。
        文章中内容的段落就得放在段落标签中，在文章中有想强调的文本，就可以使用em标签表示强调等等。

4. 认识body标签：


    <p>段落文本</p>              有三段就放三个<p></p>
    <h1>标题文本</h1>            h1-h6共6个标题分级
    <em>斜体文本（强调）</em>    斜体文本内容
    <strong>粗体文本</strong>    粗体显示文本内容
    <span>单独样式文本</span>    没有语义的，它的应用就是为了 设置单独的格式用的
    <q>引用的文本</q>            引用的文本内容，会自动加上双引号
    <blockquote>大段引用</blockquote>    引用大段的文本内容，文本前后会加上缩进
    <br/>                        换行
    <hr/>                        水平横线
    &nbsp;                       空格
    <address>地址信息</address>  地址信息，通常用于公司地址显示
    <code>代码内容</code>        代码，通常是一行内
    <pre>多行代码</pre>          多行代码,你需要在网页中预显示格式时都可以使用它
    <ul>                         ul-li 列表信息，以圆点显示
      <li>信息1</li>
      <li>信息2</li>
       ......
    </ul>
    <ol>                         ol-li 列表信息，带上序号
       <li>信息</li>
       <li>信息</li>
       ......
    </ol>
    <div>排版内容<div>           排版中使用，相当于一个容器
     

确定逻辑部分：逻辑部分是页面上相互关联的一组元素，如栏目版块

    <div id="版块名称">…</div>  div 带上ID号，使之更清晰
    <table>表格内容</table>      创建表格
        <caption>标题文本</caption>         为表格添加标题文本
        <tbody>...</tbody>       若加此标签后，表格会一次性显示出来（而非网页加载一点显示一点）
        <tr>表格一行</tr>        表格中的一行
        <td>表格单元格</td>      表格中的一个单元格
        <th>表格表头</th>        表格头部的一个单元格，表格表头
    <table summary="表格摘要">...</table>    为表格添加摘要，但不会被浏览器显示出来
    <a href="目标网址" title="鼠标滑过时显示文本">链接显示文本</a>    链接标签
        target="_blank"           网页将在新窗口中打开
        mailto:                   网页中邮件地址，可带多个参数
            mailto: 邮箱地址
            cc=     抄送地址
            bcc=    密抄地址
            ;       多个邮箱地址
            subject=邮件主题
            body=   邮件内容
        完整举例: <a href="mailto:yy@sf.com ?cc=aa@sf.com &bcc=bb@sf.com &subject=主题 &body=邮件内容">发送邮件</a>
    <img scr="图片地址" alt="下载失败时替换文本" title="提示文本" />


5. 与用户交互：

    语法：
        `<form method="传送方式" action="服务器文件"></form>`
    举例：

        <form    method="post"   action="save.php">
            <label for="username">用户名:</label>
            <input type="text" name="username" />
            <label for="pass">密码:</label>
            <input type="password" name="pass" />
        </form>

    表单控件：
        文本框、文本域、按钮、单选框、复选框

    method:
        post/get

    1. 文本框（文本/密码）
        <form>
           <input type="text/password" name="名称" value="文本" />
        </form>
        type：有“text”和“password”两种类型
        name：为文本框命名，方便后台ASP和PHP使用
        value：文本框默认值，一般起提示作用

    2. 文本域（多行文本）
        <textarea rows="行数" cols="列数">默认文本内容</textarea>
        cols：多行输入域的列数
        rows：多行输入域的行数

    3. 单选框、复选框
        <input   type="radio/checkbox"   value="值"    name="名称"   checked="checked"/>
        type：radio单选，checkbox复选框
        value：提交数据到服务器的值，后台PHP处理使用
        name：为控件命名，以备后台程序ASP和PHP使用
        checked：checked="checked"时，此选项默认被选中
        注意：同一组的单选按钮，name取值一定要一致

    4. 下拉列表框
        <form action="save.php" method="post" >
            <label>爱好:</label>
            <select multiple="multiple">
              <label for="book>看书</label>        
              <option value="看书" id="book">看书</option>
              <option value="旅游">旅游</option>
              <option value="运动">运动</option>
              <option value="购物">购物</option>
            </select>
            <input   type="submit"   value="提交">
            <input   type="reset"    value="重置"  />
        </form>
        value：向服务器提交值
        selected：设置selected="selected"时，默认选中
        multiple：multiple="multiple"时，可以使用Ctrl多选，但很丑
        label：为了改进鼠标易用性，鼠标点击文本时，选择上Radio


6. 认识CSS样式：
    CSS：层叠样式表（Cascading Style Sheets），主要用于定义HTML内容在浏览器内的显示样式
    语法：
        选择符{ 属性: 值}
    举例：
        p{ color: blue}
    选择符：又称选择器，指明要应用样式规则的元素，如<html>、<body>、<h1>、<p>、<img>...
    声明：指的是冒号”:“
    多条声明：使用分号”;“隔开，最好每行都加上分号
    注释：CSS使用 /**/，HTML注释则使用<!--内容-->

7. CSS样式分类：
    1. 内联式
        <p style="color:red;font-size:12px">这里文字是红色。</p>
    2. 嵌入式
        较通用的一类，CSS样式放置在<style>标签中，而<style>通常要放置在<head>内
        <style type="text/css">
            span{
               color:blue;
               font-size:12px;
            }
        </style>
    3. 外部式
        把CSS代码写到一个单独的外部文件中，以.css扩展名结尾，在<head>内使用<link>标签引入，如：
        <link href="base.css" rel="stylesheet" type="text/css" />
        href: .css文件路径
        rel和type: rel="stylesheet" type="text/css" 是固定写法，不能改
    三种方法的优先级：
        内联式 > 嵌入式 > 外部式
        就近原则，嵌入式>外部式有一个前提：嵌入式css样式的位置一定在外部式的后面
        以上规则适用于相同权值的情况
8. CSS 类选择器
    语法：
        .类选器名称{css样式代码;}
    举例：
        <style type="text/css">
        .stress{
            color:red;
        }
        </style>
    注意：前边的小圆点是必须要有的
    使用：
        <span class="stress">胆小如鼠</span>
9. CSS ID选择器
    语法：
        #ID选择器名称{css样式代码}
    举例：
        #setGreen{color:green;}
        <span id="setGreen">胆小如鼠</span> 
    区别：
        起始于 '.' 与 '#'
        调用时 class= 与 id= 
        ID选择器只能在文档中使用一次，类选择器则可以使用多次
        一个元素可以使用多个类选择器同时设置多个样式，而ID选择器是不可以的，如 <span class="stress bigsize">三年级</span>
10.CSS 子选择器
    还有一个比较有用的选择器子选择器，即大于符号(>),用于选择指定标签元素的第一代子元素。举例：
        .food>li{border:1px solid red;}
    若大于符号换成空格( ),用于选择指定标签元素的所有后辈元素，举例：
        .first span{border:1px solid red;}

11. CSS 通用选择器
    通用选择器是功能最强大的选择器，它使用一个（*）号指定，它的作用是匹配html中所有标签元素：
        * {color: red;}
    此时，所有元素的字体都为红色

12. CSS 伪类选择符
    伪类选择符，它允许给html不存在的标签（标签的某种状态）设置样式，比如说我们给html中一个标签元素的鼠标滑过的状态来设置字体颜色
        a:hover{color:red;}
    此时，把鼠标放置到元素上边，颜色就会切换为红色

13. CSS 分组选择符
    多个标签使用逗号隔开：
        h1,span{color:red;}
    相当于：
        h1{color:red;}
        span{color:red;}

14. CSS 继承
    CSS的某些样式是具有继承性的，那么什么是继承呢？继承是一种规则，它允许样式不仅应用于某个特定html标签元素，而且应用于其后代
    如：
        p{color:red;} /*可被span继承*/
        p{border:1px solid red;} /*此时，span将不继承，边框显示红色*/

15. CSS 特殊性（权值）
    权值：
        p{color:red;} /*权值为1*/
        p span{color:green;} /*权值为1+1=2*/
        .warning{color:white;} /*权值为10*/
        p span.warning{color:purple;} /*权值为1+1+10=12*/
        #footer .note p{color:yellow;} /*权值为100+10+1=111*/
    注意：还有一个权值比较特殊--继承也有权值但很低，有的文献提出它只有0.1，所以可以理解为继承的权值最低。
    层叠：
        相同权值时，最后一个将被应用
    重要性：
        相同权值时，使用 !important 将得到最高权重，如 p{color:red!important;}
        样式优先级为：浏览器默认的样式 < 网页制作者样式 < 用户自己设置的样式，使用 !important 优先级比 用户自己设定 还高

16. CSS 文字排版
    1. 字体
        body{font-family:"宋体";}
        body{font-family:"Microsoft Yahei";}
    2. 字号，颜色
        body{font-size:12px;color:#666}
    3. 粗体
        p span{font-weight:bold;}
        a{font-weight:bold;}
    4. 斜体
        p a{font-style:italic;}
        p{font-style:italic;}
    5. 下划线
        p a{text-decoration:underline;}
    6. 删除线
        .oldPrice{text-decoration:line-through;}
    7. 缩进
        p{text-indent:2em;} /*2em 表示两倍文字大小*/
    8. 行间距
        p{line-height:1.5em;}
    9. 字间距、字母间距
        h1{letter-spacing:50px;word-spacing:50px;} /*分别是字母、单词间距*/
    19.对齐
        h1{text-align:center;} /*left、right和center*/

17. CSS 元素分类
    块状元素：
        <div>、<p>、<h1>...<h6>、<ol>、<ul>、<dl>、<table>、<address>、<blockquote> 、<form>
    内联元素：
        <a>、<span>、<br>、<i>、<em>、<strong>、<label>、<q>、<var>、<cite>、<code>
    内联块状元素：
        <img>、<input>

    1. 块状元素：
        1、每个块级元素都从新的一行开始，并且其后的元素也另起一行。（真霸道，一个块级元素独占一行）
        2、元素的高度、宽度、行高以及顶和底边距都可设置。
        3、元素宽度在不设置的情况下，是它本身父容器的100%（和父元素的宽度一致），除非设定一个宽度。
        注意：a{display:block;} /*可以把内联元素 a 转换为 块状元素*/
    2. 内联元素：
        1、和其他元素都在一行上；
        2、元素的高度、宽度、行高及顶部和底部边距不可设置；
        3、元素的宽度就是它包含的文字或图片的宽度，不可改变。
        注意：display:inline 可以转换成内联元素
    3. 内联块状元素：
        1、和其他元素都在一行上；
        2、元素的高度、宽度、行高以及顶和底边距都可设置。
        注意：display:inline-block 可以转换成内联块状

18. CSS 盒模型
    1. 边框
        div{ border:2px  solid  red;}
        相当于：
        div{
            border-width:2px;
            border-style:solid;
            border-color:red;
        }
        border-style: dashed（虚线）| dotted（点线）| solid（实线）
        border-color:#888;    //前面的井号不要忘掉。
        border-width: 有 thin | medium | thick（但不是很常用），最常还是用象素（px）
    2. 上下左右边框：
        div{border-bottom:1px solid red;} /*top、bottom、left和right*/
    3. 高度和宽度
        div{
            width:200px;    /*宽度*/
            height:30px;    /*高度*/
            padding:20px;   /*元素到边框的距离，又名为“填充”*/
            border:1px solid red;
            margin:10px;    /*两盒子距离，又名为“边界”*/
        }

19. CSS 布局模型
    元素有三种布局模型：
    1、流动模型（Flow）
        网页在默认状态下的 HTML 网页元素都是根据流动模型来分布网页内容的
        第一点，块状元素都会在所处的包含元素内自上而下按顺序垂直延伸分布，因为在默认状态下，块状元素的宽度都为100%
        第二点，在流动模型下，内联元素都会在所处的包含元素内从左到右水平分布显示
    2、浮动模型 (Float)
        现在我们想让两个块状元素并排显示
        任何元素在默认情况下是不能浮动的，但可以用CSS定义为浮动，如div、p、table、img等元素都可以被定义为浮动
        举例：
            #div1{float:left;}
            #div2{float:right;}
    3、层模型（Layer）
        就像是图像软件PhotoShop中非常流行的图层编辑功能一样，每个图层能够精确定位操作，但在网页设计领域，由于网页大小的活动性，层布局没能受到热捧
        层模型有三种形式：
            1、绝对定位(position: absolute)
                需要设置position:absolute(表示绝对定位)，这条语句的作用将元素从文档流中拖出来
                然后使用left、right、top、bottom属性相对于其最接近的一个具有定位属性的父包含块进行绝对定位
                如果不存在这样的包含块，则相对于body元素，即相对于浏览器窗口
                举例：
                    div{
                        xxxx:yyyy;
                        position:absolute;
                        right:100px;
                        top:20px;
                    }
            2、相对定位(position: relative)
                position:relative（表示相对定位），它通过left、right、top、bottom属性确定元素在正常文档流中的偏移位置
                相对定位完成的过程是首先按static(float)方式生成一个元素(并且元素像层一样浮动了起来)，
                然后相对于以前的位置移动，移动的方向和幅度由left、right、top、bottom属性确定，偏移前的位置保留不动
                举例：
                    #div1{
                        width:200px;
                        height:200px;
                        border:2px red solid;
                        position:relative;
                        left:100px;
                        top:50px;
                    }                    
                    <div id="div1"></div>
            3、固定定位(position: fixed) 如弹窗广告
                fixed：表示固定定位，与absolute定位类型类似，但它的相对移动的坐标是视图（屏幕内的网页窗口）本身
                它不会随浏览器窗口的滚动条滚动而变化，除非你在屏幕中移动浏览器窗口的屏幕位置，或改变浏览器窗口的显示大小，
                因此固定定位的元素会始终位于浏览器窗口内视图的某个位置，不会受文档流动影响
                举例：
                    #div1{
                        width:200px;
                        height:200px;
                        border:2px red solid;
                        position:fixed;
                        left:100px;
                        top:50px;
                    }
            Relative与Absolute组合使用：
                1、参照定位的元素必须是相对定位元素的前辈元素
                <div id="box1"><!--参照定位的元素（前辈）-->
                    <div id="box2">相对参照元素进行定位</div><!--相对定位元素-->
                </div>
                2、参照定位的元素必须加入position:relative;
                #box1{
                    width:200px;
                    height:200px;
                    position:relative;        
                }
                3、定位元素加入position:absolute，便可以使用top、bottom、left、right来进行偏移定位了
                #box2{
                    position:absolute;
                    top:20px;
                    left:30px;         
                }

20. 代码简写：
    1. 盒模型：    
        margin:10px; 相当于 margin:10px 10px 10px 10px; （上右下左顺序）
        margin:10px 40px; 相当于 margin:10px 40px 10px 40px; （上右 下左顺序）
        padding, border和 margin是一致的；
    2. 颜色值：
        p{color:#000000;} 相当于 p{color: #000;}
        p{color: #336699;} 相当于 p{color: #369;}
    3. 字体：
        body{
            font-style:italic;
            font-variant:small-caps; 
            font-weight:bold; 
            font-size:12px; 
            line-height:1.5em; 
            font-family:"宋体",sans-serif;
        }
        编写为：
            body{font:italic  small-caps  bold  12px/1.5em  "宋体",sans-serif;}
        注意：
            1、使用这一简写方式你至少要指定 font-size 和 font-family 属性，其他的属性未指定将自动使用默认值。
            2、在缩写时 font-size 与 line-height 中间要加入“/”斜扛。

21. 长度值
    1. 像素
        像素为什么是相对单位呢？因为像素指的是显示器上的小点（CSS规范中假设“90像素=1英寸”）
    2. em
        假定 font-size设定 14px，那么 1em=14px
    3. 百分比
        p{font-size:12px;line-height:130%}
```




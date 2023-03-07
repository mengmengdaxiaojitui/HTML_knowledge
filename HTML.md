1. link : <a>定义一个超级链接
    <a href="https://www.runoob.com/" target="_blank" rel="noopener noreferrer">访问菜鸟教程!</a>       
    1. target: 定义被链接的文档会在何处显示（_blank,在新页面）

    2. id: 创建一个HTML文档书签，但是在HTML页面不显示。   
    <a id="tips">有用的提示部分</a>   
    <a href="#tips">访问有用的提示部分</a>    

    3. 需要将正斜杠添加到子文件夹   

    4. 图片链接<p>创建图片链接:<a href="http://www.runoob.com/html/html-tutorial.html">   <img  border="10" src="smiley.gif" alt="HTML 教程" width="32" height="32"></a></p>   
      
    <p>无边框的图片链接:
    <a href="http://www.runoob.com/html/html-tutorial.html">   
    <img border="0" src="smiley.gif" alt="HTML 教程" width="32" height="32"></a></p>   

    5. 跳到当前页面 
        <p><a href="#C4">查看章节 4</a></p>   
        <h2><a id="C4">章节 4</a></h2><p>这边显示该章节的内容……</p>

    6. 创建电子邮件链接：<a href="mailto:someone@example.com?Subject=Hello%20again" target="_top">发送邮件</a>



------------------------
2. head:（CSS, title, style, meta, link, script, noscript, base)   
    1. title: 必需的。定义了工具栏的标题，收藏过后显示在收藏夹中的标题。

    2. base:描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接：<head><base href="http://www.runoob.com/images/" target="_blank"></head> 

    3. link: 定义了文档与外部资源之间的关系，常用于样式表<link rel="stylesheet" type="text/css" href="mystyle.css">   

    4. style: 定义了HTML文档的样式引用地址，也可以直接添加样式来渲染文档。<style type="text/css">body {
    background-color:black;}
    p {color:white}</style>   

    5. meta: meta标签描述了一些基本的元数据.标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。（网页的描述，关键词，文件的最后修改时间，作者，或者其他Web服务。）
        1. 为搜索引擎定义关键词 :
        <meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">

        2. 为网页定义描述内容: 
        <meta name="description" content="免费 Web & 编程 教程">
         
        3. 定义网页作者:<meta name="author" content="abby">

        4. 每30秒钟刷新当前页面: <meta http-equiv="refresh" content="30 seconds">

        

        

---------------------
3. CCS: style（内联样式，内部样式表，和外部引用）
    1. 内联：在html中使用style属性
    <a href="http://www.runoob.com/" style="text-decoration:none;">访问 runoob.com!</a>

    2. 内部：head区域使用style
    <style type="text/css">
    h1 {color:white;}
    p {color:white;}</style>

    3. 外部：在head使用外部CSS文件再引入（最好的方式）<link rel="stylesheet" type="text/css" href="styles.css">


-----------------
4. img:是空标签，只包含属性，没有闭合标签（src是源属性，alt是替代文本）
<img src="url" alt="some_text">

    1. 从不同的位置插入图片：
    <img src="/images/chrome.gif" alt="Google Chrome" width="33" height="32"><p>一个来自菜鸟教程的图像:</p>   
    <img src="http://www.runoob.com/images/logo.png" alt="runoob.com" width="336" height="69">    

    2. 可设置图片高度，宽度，位置（height, width, align="middle/top"。

    3. 图片链接:
    <a href="http://www.runoob.com/html/html-tutorial.html">   <img  border="10" src="smiley.gif" alt="HTML 教程" width="32" height="32"></a></p>   

    4. 图片影射： 创建带有可供点击区域的图像地图，其中的每个区域都是一个超级链接
        1. map:定义图像地图
        2. area： 定义图像中的可点击区域
    <img src="planets.gif" width="145" height="126" alt="Planets" usemap="#planetmap">
    <map name="planetmap">
    <area shape="rect" coords="0,0,82,126" alt="Sun" href="sun.htm">
    <area shape="circle" coords="90,58,3" alt="Mercury" href="mercur.htm">
     <area shape="circle" coords="124,58,8" alt="Venus" href="venus.htm">
    </map>

        3. shape:点击区域形状（rect矩形,  circle圆形, poly多边形)
        4. coords: 连接区域在图片上的坐标，以像素为单位

-----------------
5. table: 
    1. tr(table row): 行
    2. td(table data cell): 列
    3. th(table header cell): 表头
    4. 两行三列:(border边框属性，th是表头属性:会自动加粗居中, caption是表格标题，)
    <table border="1">
        <caption>Monthly saving</caption>
        <tr>
            <th>head1</th>
            <th>head2</th>
            <th>head3</th>
        </tr>
        <tr>
            <td>100</td>
            <td>200</td>
            <td>300</td>
        </tr>
        <tr>
            <td>400</td>
            <td>500</td>
            <td>600</td>
        </tr>
    </table>

    5. 跨行表格:(th rowspan="2" 跨两列/ th colspan="2"跨两行)

    6. 可以table里面包含table,list,和其他元素

    7. 单元格边/格间距：(cellpadding, cellspacing)
    <table border="1" cellpadding="10">
    <table border="1" cellspacing="10">

-------------------
6. list:（有序列表，无序列表，自定义列表）
    1. 无序列表：小黑圆圈(ul-unordered list)
        1. list-style-type: 
            1. disc:圆点
            2. circle: 圆圈
            3. square: 正方形
        <ul style="list-style-type:disc"><li>Coffee</li><li>Milk</li></ul>

    2. 有序列表：数字（ol-ordered list)
        1. type:
            1. A/a: 大写字母/小写字母
            2. I/i: 罗马数字/小罗马数字
        <ol type="I"><li>coffee</li><li>milk</li></ol>

    3. 自定义列表： 项目及注释的组合（dl-definition list)
        1. dl: 自定义列表
        2. dt: 自定义列表项(difinition term)
        3. dd: 自定义列表项的定义(difinition description)
        <dl><dt>Coffee</dt>
        <dd>- black hot drink</dd>
        <dt>Milk</dt>
        <dd>- white cold drink</dd></dl>

    4. 嵌套列表：ul里面放ul
       
------------------------
7. div和span：HTML可通过这两个将元素组合起来
    1. HTML元素被定义为：块级元素/内联元素
        1. 块级元素(blcok-level)： 通常以新行来开始和结束（div,h1,p,ul,table）

        2. 内联元素(inline)： 不会以新行开始 （span, b, td, a, img)
            1. b（bring attention to): 粗体元素，用于吸引读者的注意到该元素的内容上

        3. div: 
            1. 块级元素，没有特定含义，用于组合其他HTML元素的容器，游览器会在其前后方显示折行。
            2. 与CSS一同使用，可用于对大的内容块设置样式属性。

        4. spn: 
            1. 内联元素， 可作为作文本的容器.
            2. 与CSS使用，只可用于部分文本设置样式属性


-----------
8. 布局：使用div/table(不建议用table进行布局)
    <body>
    <div id="container" style="width:500px"><!--整个图形大小为500px-->
    <div id="header" style="background-color:#FFA500;">
    <h1 style="margin-bottom:0;">主要的网页标题</h1></div>
    <div id="menu" style="background-color:#FFD700;height:200px;width:100px;float:left;">
    <b>菜单</b><br>
    HTML<br>
    CSS<br>
    JavaScript</div>
    <div id="content" style="background-color:#EEEEEE;height:200px;width:400px;float:left;">
    内容在这里</div>
    <div id="footer" style="background-color:#FFA500;clear:both;text-align:center;">
    版权 © runoob.com</div>
    </div>
    </body>

![alt 布局图片](/Users/zhenghuanhuan/Desktop/HTML/布局.png/)
<img src="/Users/zhenghuanhuan/Desktop/HTML/布局.png" alt="布局照片">


------------------
9. 表单和输入：
    1. 表单: from action=""
        1. 手机用户输入信息，表示文档中的一个区域，此区域包含交互空间，将用户收到的信息送到Web服务器

        2. 表单本身不可见，一般一个文本字段默认官渡为二十个字符   

        3. input type="...":
            1. text:输入字母和数字等内容(带边框的表单：fieldset)
                <from action="">
                <fieldset>
                <legend>Personal information:</legend>
                Name: <input type="text" size="30"><br>

            2. password:输入密码，密码字段字符为星号或者圆圈
                Password: <input type="password" name="password"></form>  

            3. dadio: 单选按钮
                <input type="radio" name="sex" value="male">男<br>

            4. checkbox: 复选框(再次点击可取消)
                <input type="checkbox" name="person" value="abby">我喜欢abby<br>
            
           
            5. submit:提交按钮(当用户单击确认按钮时，表单的内容会被传送到服务器。表单的动作属性 action 定义了服务端的文件名。action 属性会对接收到的用户输入数据进行相关的处理)
               <form name="input" action="html_form_action.php" method="get">
               Username: <input type="text" name="user">
               <input type="submit" value="Submit"></form> 

               1. method：用于定义表单数据的提交方式
                    1. post:   
                    指的是 HTTP POST 方法，表单数据会包含在表单体内然后发送给服务器，用于提交敏感数据，如用户名与密码等。
                    2. get:    
                    默认值，指的是 HTTP GET 方法，表单数据会附加在 action 属性的 URL 中，并以 ?作为分隔符，一般用于不敏感信息，如分页等。例如：https://www.runoob.com/?page=1，这里的 page=1 就是 get 方法提交的数据。

            6. select：下拉列表（可以有预选值：selected)
            <form action="">
            <select name"person" >
            <option value="abby" selected>abby</option></form>

            7. 从表单发送邮件:
            <form action="MAILTO:someone@example.com" method="post" enctype="text/plain">
            Name:<br><input type="text" name="name" value="your name"><br>
            E-mail:<br>
            <input type="text" name="mail" value="your email"><br>
            Comment:<br>
            <input type="text" name="comment" value="your comment" size="50"><br><br>
            <input type="submit" value="发送">
            <input type="reset" value="重置"></form>


----------------
10. iframe: 框架
    1. 可以在同一个游览器窗口显示不止一个页面,有的游览器不支持这个   
    2. 语法： <iframe src="URL"></iframe>url指向不同的网站

    3. 设置高度和宽度：width, height
    4. 移除边框： frameborder="0"
    5. 使用iframe来显示目标连接页面，目标链接会在iframe里面显示：target
    <iframe src="demo_iframe.htm" name="iframe_a"></iframe>
    <p><a href="https://www.runoob.com" target="iframe_a">RUNOOB.COM</a></p>

---------------
11. RGB:（红，绿，蓝，Alpha透明度）
    1. 每种颜色最小值为0：十六进制 #00
    2. 最大值为255： 十六进制 #FF
    3. Alpha： 0-1   
    div{background:rgba(255,0,0,0.5);}

---------------
12. script:
    1. script标签：
    <body><script>document.write("Hello World!")</script></body> 

    2. noscript标签：针对不支持脚本或禁用脚本的游览器，如果不支持的话游览器会呈现noscript的文版本内容
    <script>document.write("Hello World!")</script>
    <noscript>抱歉，你的浏览器不支持 JavaScript!</noscript>
     
--------------------
13. 字符实体：character entities
    1. html不能使用小于或者大于符号,所以需要使用实体名(&lt, &#60, &#060)，但是有的游览器不支持所有的实体名称。
    2. 实体名格式： 
        1. &entity_name;（小于&lt，大于&gt, 和号&amp）
        2. &#entity_number;（小于&#60，大于&#62, 和号&#38）

    3. 不间断空格: &nbsp
    4. 结合音符表：上网查


--------------
14. Uniform resource locators统一资源定位器： URL
    1. 由字母组成：abby.com
    
    2. 由互联网协议（IP）地址组成： 192.68.20.50

    3. 格式：   
    scheme://host.domain:port/path/filename
    http://www.runoob.com/html/html-tutorial.html

        1. scheme: 定义因特网服务的类型。最常见的类型是(http：超文本传输协议, https：安全超文本传输协议,ftp：文件传输协议, file)
        2. host: 定义域主机（http 的默认主机是 www)
        3. domain - 定义因特网域名，比如 runoob.com
        4. :port - 定义主机上的端口号（http 的默认端口号是 80)
        5. path - 定义服务器上的路径（如果省略，则文档必须位于网站的根目录中）。
        6. filename - 定义文档/资源的名称


------------
15. HTML5
    1. 首先在HTML文档第一行必须声明<!DOCTYPE html>
    2. 对于中文网页需要使用<meta charset="utf-8>
    3. 改进：
        1. 新元素：有的也被移除（dir, font, dig, center, frame, frameset, noframes, strike, center, basefont, applet, acronym)

        2. 新属性

        3. 完全支持CSS3：（新选择器，新属性，动画，2d,3d转换，圆角，阴影效果，可下载字体） 
        
        4. Video, Audio：   
            * HTML5<video>
            * HTML5<audio>   
            <video width="320" height="240" controls>
            <source src="movie.mp4" type="video/mp4">
            </video>

        5. 2D, 3D制图:
            * <canvas>元素
            * 使用内联SVG
            * 使用CSS3 2D/3d转换

        6. 本地储存，本地SQL数据
        7. web应用

    4. 八个新的HTML语义（semantic)元素，所有都是块级元素
        1. 为了让旧版本的游览器显示这些新的元素可以设置CSS的display属性值为：block   
        header, section, footer, aside, nav, main, article, figure 
        {display: block; }

        2. 添加新元素：
            1. 添加元素myHero并且定义样式。但是Internet explorer 8及其更早的不支持这个方法，需要用shiv来解决。
        <head>
        <script>document.createElement("myHero")</script>
        <style>
            myHero {
            display: block;
            background-color: #ddd;
            padding: 50px;
            font-size: 30px;}</style></head> 
        <body><myHero>我的第一个新元素</myHero></body>   
        

    5. 新元素：
        1. canvas：(JavaScript)   
            * 一个画布在网页中是一个矩形框，二维网格，左上角的坐标为（0,0）通过 canvas 元素来绘制.
            * 先定义画布标签，然后加入脚本。
            * 标签只是图形容器，您必须使用脚本来绘制图形。
                <!--画矩形-->
                1. fillStyle: CSS颜色，渐变或图案，默认黑色   
                2. fillRect(x,y,width,height):定义了矩形当前的填充方式。
                <!-- 画线条 -->
                3. moveTo(x,y):定义线条开始坐标
                4. lineTo(x,y):定义线条结束坐标
                5. stroke()：绘制线条
                <!-- 画圆 -->
                6. arc(x,y,start,stop):画圆
                7. stroke()/fill():绘制圆形
                <!-- 画文字 -->
                8. font = "大小 字体样式“ :定义字体   
                9. fillText(text,x,y):绘制实心的文本
                10. strokeText(text,x,y):绘制空心的文本
                <!-- 渐变，必须使用两种或以上的停止颜色 -->
                11. createLinearGradient(x,y,x1,y1): 创建线条渐变   
                12. createRadialGradient(x,y,r,x1,y1,r1):  创建一个径向/圆渐变
                13. addColorStop(坐标，”颜色“)：指定颜色停止，参数使用坐标来描述，可以是0至1.
                14. fillStyle: 填充渐变
                15. fillRect(x,y,width,height):填充
                <!-- 图像放到画布上 -->
                16. drawImage(image,x,y)

            <body><canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>   

            <script>
            <!--找到canvas元素-->
            var c=document.getElementById("myCanvas");
            <!-- 然后，创建 context 对象：-- >
            var ctx=c.getContext("2d");

            <!--下面的两行代码绘制一个红色的矩形 -->
            ctx.fillStyle="#FF0000";
            <!-- 在画布上绘制150x75的矩形，从左上角的（0,0）开始 -->
            ctx.fillRect(0,0,150,75);
            <!-- 画线条 -->
            ctx.moveTo(0,0);
            ctx.lineTo(200,100)
            ctx.stroke();
            <!-- 画圆 -->
            ctx.beginPath();
            ctx.arc(95,50,40,0,2*Math.PI);
            ctx.stroke();
            <!-- 画文本 -->
            ctx.font=”30px Arial";
            ctx.fillText("Hello World", 10, 50);
            <!-- 渐变 -->
            var grd=ctx.createRadialGradient(75,50,5,90,60,100);
            grd.addColorStop(0,"red");
            grd.addColorStop(1,"white");
            ctx.fillStyle=grd;
            ctx.fillRect(10,10,150,80);
            <!-- 图像放到画布上 -->
            var img=document.getElementById("scream");
            ctx.drawImage(img,10,10);
            </script></body>

        2. SVG:(XML)   
            * 可缩放矢量图形 (Scalable Vector Graphics)
            * HTML5支持内联SVG，使用 XML 格式定义图形
            * SVG 图像在放大或改变尺寸的情况下其图形质量不会有损失
            * SVG 是万维网联盟的标准
            * 与其他图像格式相比（比如 JPEG 和 GIF），使用 SVG 的优势在于：可伸缩，可通过文本编辑器来创建和修改，可以被搜索，索引，校本化或压缩。可在任何分辨率下呗高质量的打印，可在图像质量不下降的情况下呗放大。
            * SVG 基于 XML，这意味着 SVG DOM 中的每个元素都是可用的。您可以为某个元素附加 JavaScript 事件处理器。

            * svg：图形的容器，可以绘制路径，框，圆，文本，图形图像
            
            <svg xmlns="http://www.w3.org/2000/svg" version="1.1">
            <!-- 画圆 -->
            <circle cx="100" cy="50" r="40" stroke="black" stroke-width="2" fill="red" /></svg>
            <!-- 五角星 -->
            <polygon points="100,10 40,180 190,60 10,60 160,180" style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;"></svg>
            


        3. 新多媒体元素：
            * audio:   
            定义音频内容

            * video:   
            定义视频（video 或者 movie）

            * source:   
            定义多媒体资源 video 和 audio

            * embed:   
            定义嵌入的内容，比如插件。

            * track:   
            为诸如 video和 audio 元素之类的媒介规定外部文本轨道。  

        4. 新表单元素：
            * datalist:    
            定义选项列表。请与 input 元素配合使用该元素，来定义 input 可能的值。

            * keygen:   
            规定用于表单的密钥对生成器字段。

            * output:   
            定义不同类型的输出，比如脚本的输出。 

        5. 新的语义和结构元素：很多，可以查      


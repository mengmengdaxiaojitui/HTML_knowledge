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

5. table: 
    1. tr: 行
    2. td(table data): 列
    3. 两行三列:(border边框属性，th是表头属性:会自动加粗居中, caption是表格标题，)
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

    4. 跨行表格:(th rowspan="2" 跨两列/ th colspan="2"跨两行)

    5. 可以table里面包含table,list,和其他元素

    6. 单元格边/格间距：(cellpadding, cellspacing)
    <table border="1" cellpadding="10">
    <table border="1" cellspacing="10">



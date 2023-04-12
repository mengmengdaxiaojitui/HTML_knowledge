1. Javascript的基本作用范围：
    1. 直接写入HTML输出流：      
        * document.wrire("text"); 但是只能在HTML中输出使用，如果文档加载后再使用，会覆盖整个文档。
    2. 对事件的反应：在某个时间发生时执行代码，例如用户点击按钮   
    3. 改变HTML的内容，图像，样式，验证输入   

2. JavaScript用法：
    * 如果需要在HTML中使用javaScript，需要在《script》中写。
    * javascript通常在《head》或者《body》最下面。
    * 也可以将javascript保存在外部。使用外部文件，需要再《script》标签的src属性中设置此外部文件。外部脚本不能包含《script》标签，直接写javascript代码。
    <script src="myScript.js"></script>
    * 语句之间用分号；隔开
-----------
3. 输出：
    * 没有任何的答应或者输出的函数。
    * 使用不同方式输出数据：
        1. window.alert(): 弹出警告框   
        2. document.write(): 将内容写到HTML文档中
        3. innerHTML: 写入到HTML元素
        4. console.log(): 写入到游览器的控制台
    * 操作HTML元素：
        1. 获取某个HTML元素： document.getElementById("id");
        2. 获取并插入元素内容： 
        document.getElementById("id").innerHTML=“段落修改”;

4. 语法：
    变量是一个名称，字面量是一个值
    1. (字面量)
        * Number: 3.14 / 1001/ 123e5
        * String: "abby" / 'abby'
        * 表达式: 5+6 / 5*10
        * Array: [40, 100, 2, 3]
        * Object: {firstName: "abby" , lastName: "Zheng"}
        * Function: 
            function myFunction(a, b){return a*b ;} 
    2. (变量)
        大小写敏感，通常以字母开头，也可以以$, _开头，但是不提倡
        * var： 定义变量，用=来为变量赋值，逗号隔开声明
            var x, y;
            x = 3; y = 5;    
    3. （操作符）
        * 运用赋值算数符给变量赋值：=， +， -， *，/,
        * 条件，比较及逻辑运算符：  ==, !=, > , <
    4. （注释）
        * 单行注释： // Abby
        * 多行注释： /* Abby */
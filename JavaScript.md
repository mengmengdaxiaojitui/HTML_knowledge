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
        * String: "He is called \"abby\"";或者使用不同引号
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

5. 数据类型：
    1. 基本类型：    
        * String: var x="abby";
        * Number:  var x=123e-5;
        * Boolean:  var x=true;
        * Null:  var x=null;清空变量
        * Undefined:
        * Symbol（独一无二的值）:
    2. 对象类型：    
        * Object: var x={firstName:"abby", lastName:"zheng"};
            1. 查询数据： name=x.firstName; 或者 x["firstName"];
        * Array: var x=new Array("abby","2"); / var x=new Array(); x[0]="abby";
        * Function： 
        * (特殊对象： RegExp正则, Date)
    3. 查询数据类型：   
        typeof
    4. 声明新变量：   
        使用new

6. Object: 值键
    1. 对象可以包含多个值，每个值以name:value对呈现：var car = {name:"abby",...};
    2. 对象方法：（调用函数）
        methodName: function(){ // 代码 }
    3. 访问对象方法： 
        objectName.methodName();如果不加（）会返回函数的定义

7. Function: 
    1. 函数是由事件驱动的或者被调用时执行的可重复使用的代码块
    2. 带参数的函数：   
        function MyFunction(name, job){
            alert("Welcome" + name +", the" + job);
        }
    3. 带返回值的函数：
        function myFunction(){
            var x=5;
            return x;
        }
    4. 调用函数:<button onclick="MyFunction('abby', 'it')>点击这样</button>

8. 作用域：
    1. 作用域是可访问变量的集合，对象和函数同样是变量，
    2. 局部变量：   
        在函数里声明的，具有局部作用域，局部变量只能在函数内部访问。在函数执行完毕后销毁。
    3. 全局变量：   
        变量在函数外定义。变量在函数内没有使用var等关键字，则变量为全局变量。在页面关闭后销毁。在HTML中，全局变量是window对象。

9. 事件：
    1. HTML事件发生在HTML元素上的事情。
        <some-HTML-element some-event="JavaScript 代码">
        <button onclick="getElementById('demo').innerHTML=Date()">现在的时间是?</button>
    2. 常见HTML事件：
        * onchange: HTML元素改变
        * onclick: 用户点击HTML元素
        * onmouseover: 鼠标指针移动到指定的元素上时发生
        * onmouseout: 鼠标从一个HTML元素移开鼠标时发生
        * onkeydow: 用户按下键盘按键
        * onload： 游览器已完成页面的加载

10. 字符串：
    1. "He is called \"abby\"";或者使用不同引号，字符串可以是对象（不要创建）
    2. 字符串长度： length
    3. 创建字符串属性的函数：constructor
    4. 转义字符： \
        * \': 单引号
        * \": 双引号
        * \\： 反斜杠
        * \n： 换行
        * \r： 回车
        * \t： tab制表符
        * \b： 退格符
        * \f: 换页符
    5. 字符串方法：
        * charAt()： 返回指定索引位置的字符
        * charCodeAt(): 返回指定索引位置字符的 Unicode 值
        * fromCharCode(): 将 Unicode 转换为字符串
        * concat(): 连接两个或多个字符串，返回连接后的字符串
        * indexOf(): 返回字符串中检索指定字符第一次出现的位置
        * lastIndexOf(): 返回字符串中检索指定字符最后一次出现的位置
        * match(): 找到一个或多个表达式的匹配
        * replace(): 替换与表达式匹配的子串
        * search(): 检索与表达式相匹配的值
        * slice()： 提取字符串的片段，并在新的字符串中返回被提取的部分
        * split()： 把字符串分割为子字符串数组
        * toLowerCase()： 把字符串转换为小写
        * toUpperCase()： 把字符串转换为大写
        * toString(): 返回字符串对象值
        * valueOf(): 返回某个字符串对象的原始值
        * trim(): 移除字符串首尾空白

11. 算术运算符：
    1. +，-，*，/：
    2. %： 取模，余数， 剩余的数是多少(x=y%2)
    3. ++： 自增加一（x=++y)
    4. --： 自减加一 (x=--y)

12. 比较运算符：
    1. ==：等于
    2. !=： 不等于
    3. ===： 绝对等于
    4. !==： 绝对不等于
    5. &&： and
    6. ||: or
    7. !: not
    8. 对变量进行赋值的条件运算符：
        variablename=(condition)?value1:value2;
        voteable=(age<18)?"年龄太小”：“年龄已达到”；

13. 条件语句：
    1. if:
        * 只有当指定条件为true时使用该语句执行代码
        * if(condition){
            当条件为true执行的代码
        }

    2. if...else:
        * true执行代码，false执行别的代码
    3. if...else if...else:
        * 选择多个代码块之一来执行
    4. switch:
        * 穿着多个代码块之一来执行
        * switch(n){
            case 1:
                执行代码块 1
                break;
            case 2:
                执行代码块 2
                break;
            default:
                与 case 1 和 case 2 不同时执行的代码
        } 

14. for循环：
    1. for: 有一定的次数
        * for (语句 1; 语句 2; 语句 3)
          { 被执行的代码块 }
        * 语句1： 开始前执行，可任意值或多个值（ var i=0; )
        * 语句2： 运行循环的条件( i<5; )
        * 语句3： 在循环代码块执行后执行( i++; )  

    2. for/in: 循环遍历对象的属性
        * var person={fname:"Bill",lname:"Gates",age:56}; 
            for (x in person)  // x 为属性名
            { txt=txt + person[x]; }

    3. while: 当指定条件为true时循环指定的代码块
        * while (条件)
        { x=x + "The numver is " + i;
          i++  }

    4. do/while: 当指定的条件为trur时循环指定的代码块,该循环至少执行一次
        * do{ 需要执行的代码 }
          while (条件);

15. break / continue
    1. break: 跳出循环
    2. continue: 跳出当前循环的迭代，显示下一个
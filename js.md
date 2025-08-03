### 入门

#### 编写位置

1.可以将js编写到网页内部的script标签

```
<script >
 	alert('哈哈')
</script>
```

2.可以将js编写到外部的js文件，然后通过script标签引入

```
<script src="./入门/script/script.js"></script>
```

 3.可以将js代码编写到指定属性中

```
<button onclick="alert('你点我干嘛')">点我一下</button>
<hr>
<a href="javascript:alert('哈哈哈')">超链接</a>
<hr>
<a href="javascript:;">超链接</a>
```

#### 基本语法

1.多行注释 /**/

2.单行注释 //

3.js严格区分大小写

4.在js中多个空格和换行会被忽略

- 可以利用这个特点对代码进行格式化，让代码更美观一点

5.js每条语句都应该以分号结尾

- js中具有自动添加分号的机制，所以如果不写分号解释器会自动添加

#### helloworld

```
js代码需要编写到script标签中
<script>        
    alert("hello,world")//弹出警告框
    console.log('你猜我在哪？')//控制台呈现
	document.write('你猜我在哪？')//文档就是网页，所以是在文档中呈现
</script>        
```

#### 变量和常量

变量中并不存储任何值，而是存储值的内存地址

在js中使用const声明常量，常量只能赋值一次，重复赋值会报错

​     在js中除了常规的常量外，有一些对象类型的数据我们也会声明为常量

#### 字面量和变量

字面量

​        \- 字面量其实就是一个值，他所代表的含义就是他字面的意思

​        \- 比如，1,2,3,4,5,"hello"，true，null……

​        \- 在js中所有的字面量都可以直接使用，但是直接使用字面量并不方便

```
	   let x
       x=80
       x=81
       console.log(x)
```

​      变量

​        \- 变量可以“存储”字面量

​        \- 并且变量中存储的字面量可以随意修改

​        \- 通过变量可以对字面量进行描述，并且变量比较方便修改

```
	   let age
       age=80
       console.log(age)
```

多行注释快捷键：shift+alt+a

​      变量的使用

​        声明变量--> let 变量名 / var 变量名  

​        变量赋值--> 变量名=xx

​        声明和赋值同时进行--> let 变量=值

```
	  let a
      let b,c,d

      var e

      a=1
      a="hello"
      a=true
      console.log(a)

      let q=100
      console.log(q)
```

#### 标识符

在js中，所有可以由我们自己命名的内容，都可以认为是一个标识符

​        像变量名、函数名、类名……

​      使用标识符时需呀遵循如下的命名规范：

​        1.标识符只能含有字母、数字、下划线、$,且不能以数字开头

​        2.标识符不能是js中的关键字和保留字，也不建议使用内置的函数和类名

​        3.命名规范：

​          \- 通常会使用驼峰命名法

​            \- 首字母小写，每个单词开头大写

​            \- maxlength---maxLength

​          \- 类名会使用大驼峰命名法

​            \- 首字母大写，每个单词开头大写

​            \- maxlength---MaxLength

​          \- 常量的字母会全部大写

​            \- MAX_LENGTH

### 数据类型

#### 数值

数值（Number）

​        \- 在js中所有的整数和浮点数都是Number类型

​        \- js中的数值并不是无限大的，当数值超过一定范围后会显示近似值

​        \- Infinity是一个特殊的数值，表示无穷

​        \- NaN (Not a Number)也是一个特殊的数值，表示非法的数值

​        \- 所以在js中进行一些精度比较高的运算时要十分注意



​      大整数（BigInt）

​        \- 大整数用来表示一些比较大的整数

​        \- 使用n结尾，表示的数字范围以内存为依据，内存装得下就可以无限大

​      其他进制的数字：

​        二进制 0b

​        八进制 0o

​        十六进制 0x

​      创建的时候可以创建其他进制的值，但显示出来还是十进制



```
	  let a = 10
       a=10.5
       a=999999999999999999999999999999999999999999
       a= 99999** 99999
       a=0.00000000000000000000000000000000000000000000000001
       a=0.1+0.2
       a= 1-'a'
       a=999999999999999999999999999999999999999999999999999999999n

       a=0b1010
       a=0o10
       a=0xff
       console.log(a)
```

#### 类型检查

```
	    let a=10
        let b=10n
        console.log(a)
        console.log(b)
         a+b
        //大整数不能和其他类型的值进行运算
        console.log(typeof a)
        console.log(typeof b)
```

 typeof 运算符

​        \- 用来检查不同的值的类型

​        \- 他会根据不同的值返回不同的类型

#### 数据类型

​	字符串(String)

​        \- 在js中使用单引号或双引号来表示字符串

​        \- 转义字符 \

​          \''-----''

​          \\-----\

​          \\\\----\\

​          \"----"

​          \t--制表符(tab)

​          \n--换行

​        \- 模板字符串

​          \- 使用反单引号`来表示模板字符串

​          \- 模板字符串可以嵌入变量

​          \- 使用typeof检查一个字符串时会返回"string"

```
	  let a= 'hello'
       a="hello1"
       a="这是一个\\\字符串"
       console.log(a)

       let name="孙悟空"
       let str=`你好，${name}`
       console.log(str)
       let b=10
       console.log(`b=${b}`)

       let c="hhh"
       console.log(typeof c)
```

​	布尔值（Boolean）

​        \- 主要用来进行逻辑判断

​        \- 布尔值只有true和false

​        \- 使用typeof检查一个布尔值时会返回"boolean"

​      空值（Null）

​        -空值用来表示空对象

​        \- 空值只有一个null

​        \- 使用typeof检查一个空值会返回"object"

​        \- 所以使用typeof无法检查空值

​      未定义（Undefined）

​        \- 当声明一个变量而没有赋值时，他的值就是"Undefined"

​        \- Undefined的类型只有一个值就是Undefined

​      符号（Symbol）

​        \- 用来创建一个唯一的标识

​        \- 使用typeof检查符号时会返回"symbol"



​      js中原始值一共有七种

​        1.数字 Number

​        2.大整数（BigInt）

​        3.字符串（String）

​        4.布尔值（Boolean）

​        5.空值（Null）

​        6.未定义（Undefined）

​        7.符号（Symbol）

​      这七种原始值是构成各种数据的基石

​        原始值在js中是不可变类型，一旦创建就不能修改

```
 	   let bool=true//真
       bool=false//假
       console.log(bool) //false

       let a=null
       console.log(typeof a);//object

       let b
       console.log(b);//undefined

       let c=Symbol()//调用Symbol()创建了一个符号
       console.log( typeof c);//symbol
```

#### 类型转换—布尔值

使用Boolean()函数来将其他类型转换为布尔值  

​        转换的情况：

​          数字：

​            \- 0和NaN转换为false

​            \- 其余都是true

​          字符串：

​            \- 空串转换为false

​            \- 其余都是true

​          null和Undefined都转换为false



​          对象：对象通常都会转换为true



​        总结：所有表示空性的没有的错误的值都会转换为false

​          例如0、NaN、空串、null、Undefined、false

```
		let a=12//true
        a=-1//true
        a=0//false
        a=NaN//false
        a=Infinity//true

        a='abc'//true
        a='false'//true
        a=''//false
        a=' '//true

        a=null //false
        a=undefined //false
        console.log(typeof a,a);
        a=Boolean(a)
        console.log(typeof a,a);
```

#### 类型转换—数字

将其他的数据类型转换为数值

​        \- 1.使用Number()函数来将其他类型转换为数值

​        转换的情况：

​          \- 字符串：

​            \- 如果字符串是一个合法的数字，则会自动转换为对应的类型

​            \- 如果字符串不是合法数字，则转换为NaN

​            \- 如果字符串是空串或者纯空格的字符串，则转换为0

​          \- 布尔值：

​            \- true转换为1，false转换为0

​          \- null 转换为0

​          \- Undefined 转换为NaN



​        专门用来将字符串转换为数值的两个方法

​          \- parseInt() 将一个字符串转换为一个整数

​            \- 解析时会自左向右读取一个字符串，直到读取到字符串中所有的有效整数

​            \- 也可以使用parseInt()来对一个数字进行取整

​          \- parseFloat() 将一个字符串转换为一个浮点数

​            \- 解析时会自左向右读取一个字符串，直到读取到字符串中所有的有效小数

```
	  let a='123'//123
       a='abc'//NoN
       a='11px'//NoN
       a=''//0
       a=' '//0
       a=true//1
       a=false//0
       a=null//0
       a=undefined//NaN
       //console.log(typeof a,a)
       a=Number(a)
       //console.log(typeof a,a)

       let b='123px'
       b='123.45'
       b=456
       console.log(typeof b,b);
       b=parseInt(b)
       console.log(typeof b,b);
```

#### 类型转换—字符串

类型转换是指将一种数据类型转换为其他类型

​        主要是将类型转换为字符串、数值、布尔值

​      

​      转化为字符串：

​        1.调用toString()方法将其他类型转换为字符串

​          \- 调用xxx的yyy方法

​             ----xxx.yyy()

​          \- 由于null和Undefined中没有toString()

​            所以这两个东西调用toString()时会报错

​        2.调用String()函数将其他类型转换为字符串

​          \- 调用xxx函数

​            ----xxx()

​          原理：对于拥有toString()方法的值调用String()函数时，

​            实际上就是在调用toString()方法

​            对于null，则直接转换为"null"

​            对于Undefined，则之际转换为"undefined"

```
	  let a=10 //"10"
       a=true //"true"
       a=11n//"11"
       a=null
       /* console.log(typeof a,a);
       a=a.toString(a)
       console.log(typeof a,a); */

       let b=1//"1"
       b=null//"null"
       b=undefined//"undefined"
       console.log(typeof b,b)
       b=String(b)
       console.log(typeof b,b)
```

### 运算符

#### 算术运算符

运算符（操作符）

​        \- 运算符可以用来对一个或多个操作数(值)进行运算

​        \- 算术运算符

​          \+ 加法运算符

​          \- 减法运算符

​          \* 乘法运算符

​          / 除法运算符

​          ** 幂运算

​          % 模运算，两个数相除取余数

  \- 注意：

​          \- 算术运算时，除了字符串的加法，其他运算的操作数是非数值时，都会自动转换为数值进行运算

```
	  let a=1 + 1
       a=1 - 2
       a=2 * 2
       a=5 / 2
       a=10 / 3 //不是整除，是多少就显示多少
       a=10 / 0 //Infinity
       a=10 ** 2
       a=9 ** .5 //.5表示平方根
       a=10 % 2 //0
```

```
js是一门弱类型语言，当进行运算时会通过自动的类型转换来完成运算
       a=10 - '5'//10-5
       a=10 + true//10+1
       a=10 + null //10+0
       a=5 - undefined //5-NaN=NaN
```

当任意一个值和字符串做加法运算时，他会先将其他值转换为字符串，然后再做拼串的操作

​    可以利用这一特点来完成类型转换

​      可以通过为任意类型 + 一个空串的形式来将其转换为字符串，其原理和String()函数相同，但使用起来更加简洁

```
	   a="hello" + "world"
       a= '1' + 2 //'1' + '2' = 12
       
       a=true
       a=a + ''
       console.log(typeof a,a);
```

#### 赋值运算符

赋值运算符用来将一个值赋值给一个变量

​        = 

​          \- 将符号右侧的值赋值给左侧的变量

​        ??= 

​          \- 空赋值，只有当变量的值为null或Undefined时才会对变量进行赋值

​        +=

​          \- a += n 等价于 a = a + n

​        -=

​          \- a -= n 等价于 a = a - n

​        *=

​          \- a *= n 等价于 a = a * n

​        /=

​          \- a /= n 等价于 a = a / n

​        %=

​          \- a %= n 等价于 a = a % n

​        **=

​          \- a **= n 等价于 a = a ** n

```
	  let a = 10
       a = 5 //将右边的值赋值给左边的变量
       let b = a //一个变量只有在=左边才是变量，在=右边是值
       
       a = 66
       a = a + 11 //大部分的运算符都不会改变变量的值，赋值运算符除外

       a = 5
       a = a + 5//10
       a += 5//在a原来值的基础上加5

       a=null
       a=undefined
       a ??= 101
       console.log(a)
```

#### 一元的正负

一元的正负

​        \+ 正号

​          \- 不会改变数值的符号

​        \- 负号

​          \- 可以对数值进行符号位取反

​        当我们对非数值类型进行正负运算时，会先将其转换为数值然后再运算

```
	  let a = -10
       a = -a
       let b='123'
       b=+b //等价于b=Number(b),结果是123
        console.log(typeof a,a);
        console.log(typeof b,b);
```

#### 自增和自减

++ 自增运算符

​        \- 使用会使得原来的变量立刻增加1

​        \- 自增分为前自增(++a)和后自增(a++)

​        \- 无论是a++还是++a都会使原变量立刻增加1

​        \- 不同的是++a和a++所返回的值不同

​          a++是自增前的值，旧值

​          ++a是自增后的值，新值

```
		let a = 10
       
    //    let b = a++
    //    console.log("a++ = ",b);
       
       let b = ++a
    //    console.log("++a = ",b);
    //    console.log(a);

       let n = 5
       //             5     7   7
       let  result = n++ + ++n + n
       console.log(result);	
```

-- 自减运算符

​        \- 使用会使得原来的变量立刻减少1

​        \- 自减分为前自减(--a)和后自减(a--)

​        \- 无论是a--还是--a都会使原变量立刻减少1

​        \- 不同的是--a和a--所返回的值不同

​          a-- 是自减前的值，旧值

​          --a 是自减后的值，新值

```
	a = 5
      console.log('--a =',--a);//4
      //console.log('a-- =',a--);
      
      console.log(a);
```

#### 逻辑非

! 逻辑非

​        \- 可以对一个值进行非运算

​        \- 他可以对一个布尔值进行取反操作

​          true --- false

​          false --- true

​        \- 如果对一个非布尔值进行取反，他会先将其转换为布尔值然后再取反

​          可以利用这个特点将其他类型转换为布尔值



​        类型转换

​          转换为字符串

​            显式转换：String()

​            隐式转换: +　＂＂

​          转换为数值

​            显式转换：Number()

​            隐式转换: +

​          转换为布尔值

​            显式转换：Boolean()

​            隐式转换: !!

```
	let a = 1
       a=!a
       //console.log(a);

       a = 123
       a=!!a
       console.log(typeof a,a);
```

#### 逻辑与、逻辑或

&& 逻辑与

​        \- 可以对两个值进行与运算

​        \- 当&&左右都为true时，则返回true，否则返回false

​        \- 与运算是短路的与，如果第一个值是false，则不看第二个值

​        \- 与运算是找false，如果找到false则直接返回，没有false才会返还true

​        \- 对于非布尔值进行与运算，他会转换为布尔值然后运算，但是最终会返回原值

​        \- 如果第一个值为false，则直接返回第一个值

​          如果第一个值为true，则返回第二个值

```
	let a = true && true //true
       a = false && true //false
        a = true && false //false
        a = false && false //false

        //true && alert(123) //第一个值为true，alert会执行
        false && alert(123) //第一个值为false，alert不会执行

        //  true && true --> true
        a = 1 && 2//2
        // true && false -->false
        a = 1 && 0//0
        // false && false -->false
        a = 0 && NaN//0
```

|| 逻辑或

​        \- 可以对两个值进行或运算

​        \- 当||左右有true时，则返回true，否则返回false

​        \- 或运算也是短路的或，如果第一个值是true，则不看第二个值

​        \- 或运算是找true，如果找到true则直接返回，没有true才会返还false

​        \- 对于非布尔值进行或运算，他会转换为布尔值然后运算，但是最终会返回原值

​        \- 如果第一个值为true，则直接返回第一个值

​          如果第一个值为false，则返回第二个值

```
	 a = true || true //true
        a = true || false //true
        a = false || true //true
        a = false || false //false

        //false || alert(123) //第一个值为false，alert会执行
        true || alert(123) //第一个值为true，alert不会执行

        a = 1 || 2 //1
        a = "hello" || NaN //"hello"
        a = NaN || 1 //1


       console.log(a);
```

#### 关系运算符

关系运算符用来检查两个值之间的关系是否成立

​        成立返回true，不成立返回false



​        \> 检查左值是否大于右值

​        \>= 检查左值是否大于或等于右值

​        < 检查左值是否小于右值

​        <= 检查左值是否小于或等于右值

​    注意： 当对非数值进行关系运算时，他会转换为数值再进行比较

​      当关系运算符的两端是两个字符串，他不会将字符串转换为数值，而是逐位比较字符的Unicode编码

​        利用这个特点可以对字符串按照字母排序

​      注意比较两个字符串格式的数字时一定要进行类型转换

```
	let a = 10 > 5//true
       a = 5 > 5 //false
       a = 5 >= 5//true

       a = 5 < '10' //true
       a = '1' > false //true

       a = 'a' < 'b' //97<98,true
       a = '12' < '2' //字符串逐位比较，1<2,true

       //检查num是否在5和10之间
       let num = 6
       //a = 5 < num < 10 错误的写法
       a = num > 5 && num < 10

       console.log(a);
```

#### 相等运算符

==

​        \- 相等运算符，用来比较两个值是否相等，相等返回true，不等返回false

​        \- 使用相等运算符比较两个不同类型的值时，

​          他会将其转换为相同的类型（通常转换为数值）然后再比较，

​          类型转换后值相同也会返回true

​          null == undefined 会返回true

​          NaN不和任何值相等，包括他自己

```
	let a = 1 == 1 //true
        a = 1 == 2 //false
        a = 1 == '1' //true
        a = true == '1' //true
        
        a = null == undefined //true
        a = NaN == NaN //false
```

​      ===

​        \- 全等运算符，用来比较两个值是否全等

​        \- 他不会进行自动的类型转换，如果两个值的类型不同直接返回false

​        \- null === undefined 会返回false

```
	a = 1 ==='1' //false
        a = null === undefined //false
```

​      !=

​        \- 不相等，用来检查两个值是否不相等，不相等返回true，相等返回false

​        \- 会自动进行类型转换

```
	a = 1 != 1 //false
```

​      !==

​        \- 不全等，用来检查两个值是否不全等，不全等返回true，全等返回false

​        \- 不会自动进行类型转换

```
	a = 1 !== '1' //true
        a = 1 !== 2 //true
```

#### 条件运算符

条件运算符

​        条件表达式 ? 表达式1 ：表达式2

​      执行顺序：条件运算符在执行时，会先对条件表达式进行求值判断，

​        如果结果为true，则执行表达式1

​        如果结果为false，则执行表达式2

```
//false ? alert(1):alert(2)
        let a = 10
        let b = 20
        c=a<b ? true:false
        console.log(c);
```

#### 运算符优先级

和数学一样，js中的运算符也有优先级，比如先乘除后加减

​      因为()拥有最高的优先级，如果遇到拿不准的，可以直接通过()来改变优先级

```
	let a = 1 + 3 * 3//10
        a = (1 && 2) || 3
        console.log(a);
```

### 流程控制

#### 代码块

使用{}来创建代码块，代码块可以用来对代码进行分组,

​        同一个代码块中的代码就是同一组代码，一个代码块中的代码要么都执行要么都不执行

​      

​      let 和 var 

​        \- 在js中，使用let声明的变量具有块作用域

​          在代码块中声明的变量无法在代码块的外部访问

​        \- 使用var声明的变量不具有块作用域

```
		{
            var a = 10
            alert(123)


        }
        console.log(a);
        {
            console.log("hello");
            document.write("hello")

        }
```

#### if语句

流程控制语句可以用来改变程序执行的顺序

​        1.条件判断语句

​        2.条件分支语句

​        3.循环语句



​      if语句

​        语法：

​          if(条件表达式)

​          {

​            语句

​          }

​            

​        执行流程：

​          if语句在执行会先对if后的条件表达式进行求值判断，

​            如果结果为true，则执行if后的语句

​            如果为false，则不执行

​        if语句只会控制紧随其后的那一行代码，如果希望可以控制多行代码，可以用{}括起来

​        最佳实践：即使if后只有一行代码，我们也应该编写代码块，这样结构会更清晰

​        

​      如果if后的条件表达式不是布尔值，会转换为布尔值再运算

```
	let a = 20
        if (a > 10) {
            alert("a比10大")
        }
        if (100) {
            alert("你猜我执行吗")
        }
```

#### if-else语句

if-else语句

​        \- 语法

​          if(条件表达式){

​            语句...

​          }else{

​            语句...

​          }

​      执行流程：

​        \- if-else执行时，先对条件表达式进行求值判断

​          如果结果为true，则执行if后的语句

​          如果为false，则执行else后的语句



​      if-else if-else语句

​        \- 语法

​          if(条件表达式){

​            语句...

​          }else if(条件表达式){

​            语句...

​          }else if(条件表达式){

​            语句...

​          }else if(条件表达式){

​            语句...

​          }else if(条件表达式){

​            语句...

​          }else{

​            语句...

​          }

​        执行流程：

​          if-else if-else语句，会自上向下依次对if后的条件表达式进行求值判断

​          如果条件表达式结果为true，则执行当前if后的语句，执行完毕语句结束

​          如果条件表达式结果为false，则继续向下判断，直到找到true为止

​          如果所有的条件表达式都是false，则执行else后的语句

​        注意：

​          if-else if-else语句中只会有一个代码块被执行，

​            一旦有执行的代码块，下边的条件都不会再继续判断了

​            所以一定要注意条件编写的顺序

```
let age = 60
        //    if(age >=60){
        //     alert("你已经退休了")
        //    }else{
        //     alert("你还没有退休")
        //    }
        if (age >= 100) {
            alert("你是一个长寿的人")
        } else if(age > 80){
            alert("你比楼上那位还年轻不少")
        }else if(age >=60){
            alert("你已经退休了")
        }
        else if(age >=40){
            alert("你已经中年了")
        }
        else if(age >=18){
            alert("你已经成年了")
        }else{
            alert("你还未成年")
        }
        
       //prompt()可以用来获取用户输入的内容，他会将用户输入的内容以字符串的形式返回，可以通过变量来接收
        let num = +prompt("请输入内容：")
        alert(typeof num)
```

#### 练习1判断奇偶

```
/* 
            练习1：编写一个程序，获取用户输入的一个整数，然后通过程序来显示这个数是奇数还是偶数
        */
        let num = +prompt("请输入一个整数：")
        //let num = parseInt(prompt("请输入一个整数："))
        /* 
        验证一下用户输入的是否合法，只有是有效数字时，我们才检查他是否是奇偶
            我们不能使用== 和=== 来检查一个值是否是NaN
            可以使用isNaN()函数来检查一个值是否是NaN
            num % 1 !== 0 判断一个数是否是小数

        */
        if (isNaN(num) || num % 1 !== 0) {
            alert("你的输入有问题，请输入整数！")
        } else {
            if (num % 2 === 0) {
                alert(`${num}是偶数`)
            } else {
                alert(`${num}是奇数`)
            }
        }
```

#### 练习2期末成绩

```
/* 
            练习2：
                    从键盘输入小明的期末成绩:
                        当成绩为100时，'奖励一辆BMW'
                        当成绩为[80-99]时，'奖励一台iphone'
                        当成绩为[60-79]时，'奖励一本参考书'
                        其他时，什么奖励也没有
        */
        let score = +prompt("请输入成绩：")
        //检查score是否合法
        if (isNaN(score) || score < 0 || score > 100) {
            alert("请输入一个合法的分数")
        } else if (score === 100) {
            alert("奖励一辆BMW")
        } else if (score >= 80) {
            alert("奖励一台iphone")
        } else if (score >= 60) {
            alert("奖励一本参考书")
        } else {
            alert("什么奖励也没有")
        }
```

#### 练习3择偶条件

```
/* 
            - 练习3：
            大家都知道，男大当婚，女大当嫁。那么女方家长要嫁女儿，当然要提出一定的条件：
                高：180cm以上; 富:1000万以上; 帅:500以上;
                如果这三个条件同时满足，则:'我一定要嫁给他'
                如果三个条件有为真的情况，则:'嫁吧，比上不足，比下有余。'
                如果三个条件都不满足，则:'不嫁！'
        */
        //获取男士的数据（高、富、帅）
        let height = prompt("请输入身高(厘米)")
        let wealth = prompt("请输入财富（万）")
        let handsome = prompt("请输入颜值（像素）")
        if (height > 180 && wealth > 1000 && handsome > 500) {
            alert("我一定要嫁给他")
        } else if (height > 180 || wealth > 1000 || handsome > 500) {
            alert("嫁吧，比上不足，比下有余。")
        } else {
            alert("不嫁！")
        }
```

#### switch语句

 题目：根据用户输入的数字显示中文

​        switch语句

​          \- 语法：

​            switch(表达式){

​              case 表达式：

​                代码...

​                break

​              case 表达式：

​                代码...

​                break

​              case 表达式：

​                代码...

​                break

​              default：

​                代码...

​                break

​              ...

​            

​            }

​          \- 执行流程：

​            switch语句在执行时，会依次将switch后的表达式和case后的表达式进行全等比较

​              如果比较结果为true，则自当前case处开始执行代码

​              如果比较结果为false，则继续比较其他case后的表达式，直到找到true为止

​              如果所有的比较结果都为false，则执行default后的语句

​          \- 注意：

​            当比较结果为true时，会从当前case处开始执行代码，也就是说case是代码执行的起始位置

​              这就意味着只要是当前case后的代码都会执行，可以使用break来避免执行其他的case

​          \- 总结：

​            switch语句和if语句的功能是重复的，switch语句能做的事if语句也能做，反之亦然

​              最大的不同在于switch在多个全等判断时结构比较清晰

```
	let num = +prompt("请输入一个数字")
        switch (num) {
            case 1:
                alert("壹")
                break //break可以用来结束switch语句
            case 2:
                alert("贰")
                break
            case 3:
                alert("叁")
                break
            default:
                alert("我是default")
                break
        }
```

#### while语句

循环语句

​        \- 通过循环语句可以使指定的代码反复执行

​        \- js中一共有三种循环语句

​          while

​          do-while

​          for

​        \- while语句

​          语法：

​            while(条件表达式){

​              循环体

​            }

​        执行流程：

​          while语句在执行时，会先对条件表达式进行判断，

​            如果结果为true，则执行循环体，执行完毕，继续判断

​            如果为true，则再次执行循环体，执行完毕，继续判断，如此反复

​            直到条件表达式的结果为false时，循环结束

```
当一个循环的条件表达式恒为true时，这个循环就是一个死循环，会一直执行（慎用）
        while (true) {
        alert('哈哈')
        }
        
        
       通常编写一个循环，要有三个条件
                1.初始化表达式
                2.条件表达式
                3.更新表达式
            
        //初始化表达式
        let a = 0
        //条件表达式
        while(a < 3){
            console.log(a);
            //更新表达式
            a++   
        } 
       
       let i = 0
        while (1) {
            console.log(i);
            i++
            if (i >= 5) {
                break
            }
             
```

```
/* 
                练习：假设银行存款的年利率为5%，问1000块存多少年可以变成5000块
        
        */
        //创建一个变量表示钱数
        let money = 1000
        let year=0
        //1000存一年是多少？money = 1000*0.05+money
        while (money < 5000) {

            money = money * 0.05 + money//执行一次就是存一年的钱
            //money*=1.05
            year++

        }
        console.log(`需要存${year}年,`,`最终的钱数为${money}元`);
```

#### do-while语句

 do-while循环

​        语法：

​          do{

​            语句...

​          }while(条件表达式)

​        执行顺序：

​          do-while语句在执行时，会先执行do后的循环体，

​            执行完毕后，会对while后的条件表达式进行判断

​            如果为false，则循环终止

​            如果为true，则继续执行循环体，以此类推

​          

​          \- 和while的区别：

​            while语句是先判断再执行

​            do-while语句是先执行再判断

​            

​            实质的区别：do-while至少要执行一次

```
 	let i = 0
        /* while (i < 5) {
            console.log(i);
            i++

        } */
        do {
            console.log(i);
            i++
        } while (i < 5)
```

#### for循环

for循环

​        -for循环和while循环没有本质区别，都是用来反复执行代码，

​          不同点就是语法结构，for循环更加清晰

​        \- 语法：

​          for(①初始化表达式;②条件表达式;④更新表达式){

​              ③语句...

​          }

​        \- 执行流程：

​          1.先执行初始化表达式，初始化变量

​          2.执行条件表达式，判断循环是否执行(true执行，false终止)

​          3.判断结果为true，则执行循环体

​          4.执行更新表达式，对初始化变量进行修改

​          5.重复2，直到判断为false为止

​        \- 初始化表达式在循环的整个生命周期中只会执行一次

​        \- for循环中的三个表达式都可以省略

​        \- 使用let在for循环的()中声明的变量是局部变量，只能在for循环的内部访问

​        \- 创建死循环的方式:

​          while(1){}

​          for(;;){}

```
	/* let i = 0
        while(i<5){
        console.log(i);
        i++
       }  */
      for(let i=0;i<5;i++){
        console.log(i);
        
      }
       console.log(i);
      //死循环
      /* for(;;){
        alert(1)
      } */
```

#### 100以内3的倍数

```
<script>
        /* 
            练习:求100以内3的倍数（求有多少个和总和）

        */
       //方法一
        /*let count = 0
        sum = 0
         for (num = 1; num < 100; num++) {
            if (num % 3 === 0) {
                //console.log(num);
                count++
                sum += num
            }  
        }
         console.log(`100以内3的倍数有${count}个，`,`它们的总和是${sum}`); */
        //方法二
        let count = 0
        sum = 0
         for(num=3;num<100;num+=3){
            count++
            sum+=num
         }
         console.log(`100以内3的倍数有${count}个，`,`它们的总和是${sum}`);

    </script>
```

#### 水仙花数

```
<script>
        /* 
            练习：求1000以内的水仙花数
                    - 水仙花数
                        - 一个n位数(n>=3)，如果他各个位上数字的n次幂之和还等于这个数，那么这个数就是一个水仙花数
                        例如：153  1^3 + 5^3+ 3^3 = 153
        */
		方法一：
        /* for(let i=100;i<1000;i++){
            let bai=parseInt(i/100)
            let shi=parseInt((i-bai*100)/10)
            let ge=parseInt(i%10)
            if(bai**3+shi**3+ge**3===i)
            console.log(i);   
        } */
		方法二：
        for (let i = 100; i < 1000; i++) {
            let strI = i + ''//转换为字符串
            if (strI[0] ** 3 + strI[1] ** 3 + strI[2] ** 3 === i)
                console.log(i);

        }
    </script>
```

#### 质数

```
<script>
        /* 
            练习：获取用户输入的大于1的整数，然后检查这个数是否是质数，并打印结果
                质数：一个数如果只能被1和它本身整除，那么这个数就是质数
                    1既不是质数也不是合数
        
        */
        //以9为例
        /* let flag=true
        for(let i=2;i<9;i++){
            if(9%i===0){
                //如果执行了就说明他有其他因数，就不是质数
                flag=false
            }
        }
        if(flag){
            alert("9是质数")
        }else{
            alert("9不是质数")
        } */

        let num = +prompt("请输入一个数字")
        //用来记录num的状态，默认为true，num是质数
        let flag = true
        for (let i = 2; i < num; i++) {
            if (num % i === 0) {
                //如果if执行了就说明他有其他因数，就不是质数
                flag = false
            }
        }
        if (flag) {
            alert(`${num}是质数`)
        } else {
            alert(`${num}不是质数`)
        }
    </script>
```

#### 循环嵌套

```
在循环中也可以嵌套其他的循环

            希望在网页中打印出如下图形
                *****
                *****
                *****
                *****
                *****

                *       j<1  i=0
                **      j<2  i=1
                ***     j<3  i=2
                ****    j<4  i=3
                *****   j<5  i=4

                *****   j<5  i=0
                ****    j<4  i=1
                ***     j<3  i=2
                **      j<2  i=3
                *       j<1  i=4
            当循环发生嵌套时，外层循环每执行一次，内层循环都会执行一个完整的周期
```

```
//外层循环控制图形的高度
        for (let i = 0; i < 5; i++) {
            //内层循环控制图形的宽度
            for (let j = 0; j < 5; j++){
                document.write("*&nbsp;")
            }
             document.write("<br>")    
        }
        document.write("<hr>")
        
        //外层循环控制图形的高度
        for (let i = 0; i < 5; i++) {
            //内层循环控制图形的宽度
            for (let j = 0; j < i+1; j++){
                document.write("*&nbsp;")
            }
             document.write("</br>")    
        }
        document.write("<hr>")
        
        //外层循环控制图形的高度
        for (let i = 0; i < 5; i++) {
            //内层循环控制图形的宽度
            for (let j = 0; j < 5-i; j++){
                document.write("*&nbsp;")
            }
             document.write("</br>")    
        }
```

#### 九九乘法表

```
	<style>
        span{
            display: inline-block;
            width: 100px; 
        }
    </style>
    <script>
        /* 
            打印九九乘法表
        */
        for (i = 1; i <= 9; i++) {
            for (j = 1; j < i + 1; j++) {
                document.write(`<span>${j} * ${i} = ${i*j}</span>`)
            }
            document.write("<br>")
        }
    </script>
```

#### 100以内质数

```
	<script>
        /* 
            求100以内所有质数
        
        */
       //外层循环用来取数，内层循环用来取因数
        for (i = 2; i < 100; i++) {
            let flag = true
            for (j = 2; j < i; j++) {
                if (i % j === 0) {
                    flag = false
                }
            }
            if (flag) {
                console.log(i)
            }

        }
    </script>
```

#### break和continue

​	break

​        \- break用来终止switch和循环语句

​        \- break执行后当前的switch和循环语句会立即停止

​        \- break会终止离他最近的循环

​      continue

​        \- continue用来跳过当次循环

```
	for (let i = 0; i < 5; i++) {
            console.log(i);
            for (let j = 0; j < 5; j++) {
                if (j === 1) continue
                console.log(`内层循环-->`, j);

            }
        }

        for (let i = 0; i < 5; i++) {
            if (i === 3) {
                continue
            }
            console.log(i);
        }

        /*  for (let i = 0; i < 5; i++) {
             if(i===3){
                 break
             }
             console.log(i);
 
         } */
```

#### 质数优化

```
	<script>
        /* 
            优化前
                1.10000 100ms
                2.100000 9244ms
            第一次优化（加break）
                1.10000 9ms
                2.100000 630ms
            第二次优化（平方根）
                1.10000 1ms
                2.100000 7ms
                3.1000000 120ms
        */
       console.time("质数练习")
       for (i = 2; i < 1000000; i++) {
            let flag = true
                            //平方根
            for (j = 2; j <= i**.5; j++) {
                if (i % j === 0) {
                    flag = false
                    //进入判断说明i一定不是质数，后续的检查没有执行的必要
                    break
                }
            }
            if (flag) {
                //console.log(i)
            }

        }
        console.timeEnd("质数练习")
    </script>
```

### 对象

#### 对象

数据类型

​        原始值

​          1.数值（Number）

​          2.大整数（BigInt）

​          3.字符串（String）

​          4.布尔值（Boolean）

​          5.空值（Null）

​          6.未定义（Undefined）

​          7.符号（Symbol）



​        原始值只能表示一些简单的数据，但不能表示复杂数据

​        比如：现在需要在程序中表示一个人的信息



​        对象：对象是js中的一种复合数据类型，他相当于一个容器在对象中可以存储各种不同类型数据

```
	//创建对象
        let obj = new Object()
        /* 
            对象中可以存储多个各种类型的数据
                对象中存储的数据，我们称为属性
            
            向对象中添加属性：
                对象.属性名=属性值
            读取对象中的属性
                对象.属性名
                如果读取的是一个对象中没有的属性，不会报错而是显示Undefined

        
        */
       obj.name="孙悟空"
       obj.age=500
       obj.gender="男"
       //修改属性
       obj.name="Tom Sun"
       //删除属性
       delete obj.name
       console.log(obj.name);
       
```

#### 对象的属性

 属性名

​        \- 通常属性名就是一个字符串，所以属性名可以是任何值，没有什么特殊要求

​          如果属性名太特殊了，不能直接使用，需要使用[]来设置

​          虽然如此，但还是建议属性名也按照标识符的规范命名

​        \- 也可以使用符号(Symbol)作为属性名来添加属性

​          获取这些属性时也必须使用symbol

​          使用symbol添加的属性，通常是那些不希望被外界访问的属性

​        \- 使用[]去操作属性时，可以使用变量

​      属性值

​        \- 对象的属性值可以是任意的数据类型，也可以是一个对象

​      使用typeof检查一个对象时，返回的是object

```
	let obj = new Object()
        obj.name = "孙悟空"
        /* obj.if="hah"//不建议
        obj.let="djj"//不建议
        obj["13233#@*（）qwd"]="呵呵"//不建议 */

        /* let mySymbol=Symbol()
        obj[mySymbol]="通过mySymbol添加的属性"
        console.log(obj[mySymbol]); */

        obj.gender = "男"
        obj["age"] = 18
        let str = "address"
        obj[str] = "花果山"//等价于obj["address"="花果山"]
        obj.str = "nihao"//使用.的形式添加属性时，不能使用变量
        /* console.log(obj.gender);
        console.log(obj["age"]); */

        obj.a = 1
        obj.b = true
        obj.c = 'hello'
        obj.d = 123n
        obj.e = Object()
        obj.e.name = "猪八戒"
        obj.e.age = 300

        console.log(obj.e.name);
        console.log(typeof obj);
          /* in运算符
            -用来检查对象中是否含有某个属性
                语法：属性名 in 对象
                如果有返回true，没有返回false */
        console.log("name" in obj);
```

#### 对象字面量

对象字面量

​        \- 可以直接使用{}创建对象

​        \- 使用{}创建的对象可以直接向对象中添加属性

​        \- 语法：

​          {

​            属性名 :属性值,

​            [属性名]：属性值

​        

​          }

```
	let obj=Object()
       let mySymbol=Symbol()
       obj2={
        name:"孙悟空",
        age:500,
        ["gender"]:"男",
        [mySymbol]:"特殊的属性",
        hello:{
            a:1
        }


       }
       //obj2.name="孙悟空"
       console.log(obj);
       console.log(obj2);
       
```

#### 枚举对象中的属性

枚举属性：指将对象中所有的属性全部获取

​        for-in语句

​          \- 语法：

​            for(let propName in 对象){

​            语句...

​            }

​          \- for-in的循环体会执行多次，有几个属性就会执行几次

​            每次执行时，都会将一个属性名赋值给我们所定义的变量

​          \- 注意：并不是所有的属性都可以枚举，比如：使用符号添加的属性

```
 /* let obj=Object()
       obj.name="孙悟空"
       obj.age=500 */
       let obj={
        name:"孙悟空",
        age:500,
        gender:"男",
        address:"花果山",
        [Symbol()]:"测试"//符号添加的属性是不能枚举的
       }
       for(let propName in obj){
        //console.log(1);
        console.log(propName,obj[propName]);
        
        
       }
       console.log(obj);
```

#### 可变类型

​	\- 原始值属于不可变类型，一旦创建就无法修改

​      \- 在内存中不会创建重复的原始值

```
	let a = 10
        let b = 10
        a = 12//当我们为一个变量重新赋值时，绝对不会影响其他的变量
        console.log("a=", a);
        console.log("b=", b);
```

\	- 对象属于可变类型

​        \- 对象创建完成后，可以任意的添加删除修改对象中的属性

​        \- 注意：

​          \- 当对两个对象进行相等或全等比较时，比较的是两个对象的内存地址

​        \- 如果有两个变量同时指向一个对象，通过一个变量修改对象时，对另一个变量也会产生影响

```
	let obj = Object()
        obj.name = "孙悟空"
        obj.age = 200

        let obj2 = Object()
        let obj3 = Object()
        console.log(obj2 === obj3);//false

        let obj4=obj
        obj4.name="猪八戒"//当修改一个对象时，所有指向该对象的变量都会受到影响
        console.log("obj",obj);
        console.log("obj4",obj4);
        console.log(obj===obj4);
```

#### 变量和对象

修改对象

​        \- 修改对象时，如果有其他变量指向该对象，

​          则所有指向该对象的变量都会受到影响

​      修改变量

​        \- 修改变量时，只会影响当前的变量

​      在使用变量存储对象时，很容易因为改变变量指向的对象，提供代码的复杂度

​        所以通常情况下，声明存储对象的变量时会使用const

​      注意：const只是禁止变量被重新赋值，不会对对象的修改产生影响

```
	const obj = {
            name: "孙悟空"
        }
        const obj2 = obj
        //obj2={}
        obj2.name="猪八戒"//修改对象
        //obj2 = null//修改变量
        /* console.log(obj);
        console.log(obj2); */
        const obj3={
            name:"猪八戒"
        }
        obj3.name="沙和尚"
        console.log(obj3);
```

#### 方法

方法（method）

​        \- 当一个对象的属性指向一个函数

​          那么我们就称这个函数是该对象的方法

​          调用函数就称为调用对象的方法

```
	let obj = {}
        obj.name = "孙悟空"
        obj.age = 500
        //函数也可以成为一个对象的属性
        obj.sayHello = function () {
            console.log("hello");

        }
        // console.log(obj);
        obj.sayHello()
```



### 函数

#### 函数

函数(Function)

​        \- 函数也是一个对象

​        \- 它具有其他对象所有的功能

​        \- 函数中可以存储代码，且可以在需要的时候调用这些代码

​      语法：

​        function 函数名(){

​          语句...

​        }

​      调用函数

​        -调用函数就是执行函数中存储的代码

​        \- 语法：函数对象()

​      使用typeof检查函数对象时会返回function

```
//创建一个函数对象
       function fn(){
            console.log("你好");
            
       }
       console.log(typeof fn);
       fn()
```

#### 函数的创建方式

函数的定义方式：

​        1.函数声明

​          function 函数名(){

​            语句...

​          }

​        2.函数表达式

​          const 变量 = function(){

​            语句...

​          }

​        3.箭头函数

​          () = >{

​            语句... 

​          }

```
	//1.函数声明
        function fn() {
            console.log("函数声明");

        }
        //2.函数表达式
        const fn2 = function () {
            console.log("函数表达式");

        }
        //3.箭头函数,只有一条语句的时候可以不用大括号
        const fn3 = () => {
            console.log("箭头函数");

        }
        const fn4 = () => console.log("箭头函数2");

        console.log(typeof fn);
        console.log(typeof fn2);
        console.log(typeof fn3);
        console.log(typeof fn4);
```

#### 参数

```
/* 
                定义一个可以求任意两个数和的函数
        */

        /* function sum() {
            console.log(1 + 1);

        }
        const sum2 = function () {
            console.log(1 + 1);
        }
        const sum3 = () => console.log(1 + 1);
        sum3() */
```

​	形式参数

​        \- 在定义函数时，可以在函数中指定数量不等的形式参数（形参）

​        \- 在函数中定义参数就相当于在函数内部声明对应的变量但是没有赋值

​      实际参数

​        \- 在调用函数时，可以在函数的（）中传递数量不等的实参

​        \- 实参会赋值给其对应的形参

​        \- 参数：

​          \- 1.如果实参和形参数量相同，则对应的实参赋值给对应的形参

​          \- 2.如果实参多余形参，则多余的实参不会使用

​          \- 3.如果形参多余实参，则多余的形参为Undefined

​      1.函数声明       []表示可选

​          function 函数名([参数]){

​            语句...

​          }

​      2.函数表达式

​          const 变量 = function([参数]){

​            语句...

​          }

​      3.箭头函数

​          ([参数]) = >{

​            语句... 

​          }

```
function fn(a, b) {
            console.log("a=", a,a.name);
            console.log("b=", b);

        }
        //fn(1, 2)
        //fn(true,"hello")
        //fn(null,11n)
        //fn({name:"孙悟空"},"hello")

        function sum(a, b) {
            console.log("a+b=", a + b);

        }
        //sum(1, 2)
        //sum(1) //1+undefined=NaN
        sum("hello","world")
```

#### 箭头函数的参数

```
<script>

        const fn = (a, b) => {
            console.log("a=", a);
            console.log("b=", b);

        }
        fn(123, 456)
        //当箭头函数中只有一个参数时，括号可以省略不写
        const fn2 = a => {
            console.log("a=", a);
        }
        fn2(1)
        //定义参数时，可以为参数指定默认值，默认值会在没有对应的实参时生效
        const fn3=(a=10,b=20,c=30)=>{
            console.log("a=",a);
            console.log("b=",b);
            console.log("c=",c);
            
        }
        fn3(1,2)
 </script>
```

#### 使用对象作为参数

```
<script>
        
        function fn(a) {
            console.log("a=", a);
            //console.log(a.name);

            a = {}//修改变量时，只会影响当前的变量
            a.name = "猪八戒"//修改对象时，如果有其他变量指向该对象,则所有指向该对象的变量都会受到影响
            console.log(a);



        }
        //对象可以作为参数传递
        let obj = { name: "孙悟空" }
        //传递实参时，传递的并不是变量本身，而是变量中存储的值
        fn(obj)
        console.log(obj);

            let obj2={ name: "唐僧" }
        //函数每次调用，都会重新创建默认值
       // function fn2(a = { name: "唐僧" }) {
        function fn2(a =obj2 ) {
            console.log("a=", a);
            a.name = "沙和尚"
            console.log("a=", a);
            /* 
                默认值如果在里面写的那么他每次调用都是创建新的
                如果是在外面写的传进来，那就是每次访问的都是同一个对象
            */

        }
        fn2()
        fn2()
 </script>
```

#### 函数作为参数

在js中，函数也是一个对象（一等函数）

​        别的对象能做的事函数也可以

```
	function fn(a) {
            console.log("a=", a);
            a()

        }
        let obj = { name: "孙悟空" }
        function fn2() {
            console.log("我是fn2");

        }
        fn(fn2)
        fn(function () {
            console.log("我是匿名函数");

        })
        fn(() => console.log("我是箭头函数"))
```

#### 函数的返回值

```
<script>
        function sum(a, b) {
            //console.log(a+b);
            return a + b
        }
        sum(1, 2)
        //计算完成后，将计算的结果返回而不是直接打印
        function fn() {
            /* 在函数中，可以通过return关键字来指定函数的返回值
                返回值就是函数的执行结果,函数调用完毕返回值便会作为结果返回

            任何值都可以作为返回值使用，包括对象和函数之类
                如果return后不跟任何值，则相当于返回undefined
                如果不写return，那么函数的返回值依然是undefined

            return一执行函数立即结束
                
            */
            //return "hello"
            //return {name:"孙悟空"}
            //return ()=>alert(123)
            alert(123)
            return
            alert(456)

        }
        let result = fn()
        //result = sum(1,2)
        //console.log(fn());
        console.log("result=",result);

    </script>
```

#### 箭头函数的返回值

箭头函数的返回值可以直接写在箭头后

​        如果直接在箭头后设置对象字面量为返回值时，对象字面量必须使用（）括起来

```
	const sum = (a, b) => a + b
        const fn=()=>({name:"孙悟空"})
        let result = sum(1,2)
        result=fn()
        console.log(result);
```

#### 作用域

作用域（scope）

​        \- 作用域指的是一个变量的可见区域

​        \- 作用域有两种：

​          全局作用域

​            \- 全局作用域在网页运行时创建，在网页关闭时消耗

​            \- 所有直接编写到script标签中的代码都位于全局作用域中

​            \- 全局作用域中的变量是全局变量，可以在任意位置访问

​          局部作用域

​            \- 块作用域

​              \- 块作用域是一种局部作用域

​              \- 块作用域在代码块执行时创建，代码块执行完毕他就销毁

​              \- 在块作用域中声明的变量是局部变量，只能在块内部访问，外部无法访问

```
	let a = "变量a"
        {
            let b = "变量b"
            {
                console.log(b);

            }
        }
        console.log(b);
```

#### 函数作用域

函数作用域

​        \- 函数作用域也是一种局部作用域

​        \- 函数作用域在函数调用时产生，调用结束后销毁

​        \- 函数每次调用都会产生一个新的函数作用域

​        \- 在函数中定义的变量是局部变量，只能在函数内部访问，外部无法访问

```
	function fn() {
            let a = "fn中的变量a"
            //console.log(a);

        }
        fn()
        console.log(a);
```

#### 作用域链

作用域链(就近原则)

​        \- 当我们使用一个变量时，js解释器会优先在当前作用域中寻找变量，

​          如果找到了则直接使用

​          如果没找到，则去上一层作用域中寻找

​          如果还没找到，则继续去上一层寻找,以此类推

​          如果一直到全局作用域都没找到，则报错 xxx is not defined

```
	//let a = 10
        {
            //let a = "第一代码块中的a"
            {
               // let a = "第二代码块中的a"
                console.log(a);
            }

        }
```

#### window对象

```
<script>
        /* 
            Window对象
                - 在浏览器中，浏览器为我们提供了一个Window对象，可以直接访问
                - Window对象代表的是浏览器窗口，通过该对象可以对浏览器窗口进行各种操作
                    除此之外Window对象还负责存储js中的内置对象和浏览器的宿主对象
                - Window对象的属性可以通过Window对象访问，也可以直接访问
                - 函数可以认为是Window对象的方法
        */
        /* 
                 宿主对象：alert() document.write() console.log()……
                 内置对象：String() Number()……
        */
        //   window.alert(123)
        //   window.console.log(111)
        window.a = 10//向window对象中添加的属性会自动成为全局变量
        //console.log(a);


        /* 
            var 用来声明变量，作用和let相同，但是var不具有块作用域
                - 在全局中使用var声明的变量，都会作为window对象的属性保存
                - 使用function声明的函数，都会作为window的方法保存
                - 使用let声明的变量不会存储在window对象中，而存在一个秘密的小地方(无法访问)
        
        */
        var b = 20//等价于window.b=20
        function fn() {
            alert("我是fn")
        }
        /* console.log(window.b);
        window.fn()
        let c = 21
        window.c=22
        console.log(c); */
        function fn2(){
            //var d=10//虽然var没有块作用域，但有函数作用域（局部作用域）
            window.d=10//在局部作用域中，如果没有使用var或let声明变量，则变量会自动成为window对象的属性，也就是全局变量,（不建议这样写）
        }
        fn2()
        console.log(d);
    </script>
```



#### 提升

​	变量的提升

​        \- 使用var声明的变量，他会在所有代码执行前被声明

​          所以我们可以在变量声明前就访问变量

​      函数的提升

​        \- 使用函数声明创建的函数，会在其他代码执行前被创建

​          所以我们可以在函数声明前调用函数

​      let声明的变量实际也会提升，但是在赋值之前解释器禁止访问该变量



​      目的：提升性能，预留它们的空间

```
	console.log(a);
        var a = 10//只是var a往前提，值没有
        //a = 10//window.a=10

        console.log(b);
        let b=10
        
        

        /* fn()
        function fn(){
            alert("我是fn函数")
        } */
        
        fn2()//函数整体往前提
        var fn2=function(){

        }
```



#### 练习

```
<script>
        /* var a = 1
        function fn() {
            a = 2//在局部作用域中，如果没有使用var或let声明变量，则变量会自动成为window对象的属性，也就是全局变量
                // 但是上面已经用var声明了，所以局部的a是改变量的
            console.log(a);//2
        }
        fn()
        console.log(a);//2 */


        //定义形参就相当于在函数中声明了对应的变量，但是没有赋值
        /* var a = 1
        function fn(a) {
            console.log(a);//undefined
            var a = 2
            console.log(a);//2
        }
        fn()
        console.log(a);//1 */

        /*  var a = 1
         function fn(a) {
             console.log(a);//10
             var a = 2
             console.log(a);//2
         }
         fn(10)
         console.log(a);//1 */

        /* var a = 1
        function fn(a) {
            console.log(a);//1
            var a = 2
            console.log(a);//2
        }
        fn(a)
        console.log(a);//1 */
        

        console.log(a);//2
        var a = 1
        console.log(a);//1
        function a() {
            alert(2)
        }
        console.log(a);//1
        var a = 3
        console.log(a);//3
        var a = function () {
            alert(4)
        }
        console.log(a);//4
        var a
        console.log(a);//4
    </script>
```



#### debug

```
<script>
        // debugger//在代码中打一个断点
        console.log(a);//2
        var a = 1
        console.log(a);//1
        function a() {
            alert(2)
        }
        console.log(a);//1
        var a = 3
        console.log(a);//3
        var a = function () {
            alert(4)
        }
        console.log(a);//4
        var a
        console.log(a);//4
    </script>
```



#### 立即执行函数

在开发中应该尽量减少直接在全局作用域中编写代码

​        所以我们的代码要尽量编写到局部作用域

​      如果使用let声明的变量，可以使用{}来创建块作用域

​      如果使用var声明的变量，可以使用function

```
{
            let a = 10
        }
        {
            let a = 20
        }

       /*  function fn() {
            var a = 20
        }
        fn()
        function fn2() {
            var a = 30
        }
        fn2() */
        //希望可以创建一个只执行一次的匿名函数

        /* 立即执行函数（IIFE）
            - 立即执行函数是一个匿名的函数，他只会调用一次
            - 可以利用IIFE创建一个一次性的函数作用域，避免变量冲突的问题 */

        (function(){
            let a=10
            console.log(a);
            
        }());

        (function(){
            let a=10
            console.log(a);
            
        }())
```



#### 函数中的this

 this

​        \- 函数在执行时，js解析器每次都会传递进一个隐含的参数，这个参数就叫做this

​        \- this会指向一个对象

​          \- this所指向的对象会根据函数调用方式的不同而不同

​            1.以函数形式调用时，this指向的是window

​        \- 通过this可以在方法中引用调用方法的对象

```
function fn() {
            // console.log(this === window);
            console.log(this);
            
        }
        const obj={name:"孙悟空"}
        obj.test=fn
        const obj2={name:"猪八戒",test:fn}
        //fn()
        obj.test()//{name:"孙悟空"}
        obj2.test()//{name:"猪八戒",test:fn}

        const obj3={
            name:"沙和尚",
            sayHello:function(){
                console.log(this.name);
                
            }
        }
        const obj4={
            name:"唐僧",
            sayHello:function(){
                console.log(this.name);
                
            }
        }
        obj3.sayHello()
        obj4.sayHello()
```



#### 箭头函数中的this

箭头函数

​        ([参数]) => 返回值



​      例子：

​        无参箭头函数：() => 返回值

​        一个参数的：a => 返回值

​        多个参数的：(a,b) => 返回值

​      

​        只有一个语句的函数：() => 返回值

​        只返回一个对象的函数: () => ({...})

​        有多行语句的函数：() => {

​            ...

​            return 返回值

​        }



​        箭头函数没有自己的this，他的this由外层作用域决定!!!

​          箭头函数的this和他的调用方式无关

```
function fn() {
            console.log("fn--->", this);

        }
        const fn2 = () => {
            console.log("fn2-->", this);//总是window

        }
        /* fn()//window
        fn2() //window
        */

        const obj = {
            name: "孙悟空",
            //属性名和属性值一样可以省略属性值
            fn,//fn:fn
            fn2,//fn2:fn2
            sayHello(){//sayHello:function()
                console.log(this.name);
                /* function t(){
                    console.log("t-->",this);//window
                }
                t() */
                const t2 = ()=>{
                    console.log("t2-->",this);
                }
                t2()//sayHello
                
            }
        }
        /* obj.fn()//obj
        obj.fn2()//window */
        obj.sayHello()
```



#### 严格模式

js运行代码的模式有两种：

​        \- 正常模式：

​          \- 默认情况下，代码都运行在正常模式中，

​            在正常模式下语法检查并不严格

​            他的原则是能不报错就不报错

​          \- 这种处理方式导致代码的运行性能较差

​        \- 严格模式：

​          \- 在严格模式下语法检查变得严格

​            1.禁止一些语法

​            2.更容易报错

​            3.提升性能

​        

​        \- 在开发中，应该尽量使用严格模式

​          这样可以将一些隐藏的问题消灭在萌芽阶段

​            同时也能提升代码的运行性能

```
	"use strict"// 全局的严格模式
        let a = 10
        console.log(a);
        function fn(){
            "use strict"// 函数的严格模式
        }
```



### 面向对象

#### 面向对象简介

面向对象编程（OOP）

​        1.程序是干嘛的？

​          \- 程序就是对现实世界的抽象

​        2.对象是干嘛的？

​          \- 一个事物抽象到程序中后就变成了对象

​          \- 在程序世界中，一切皆对象



​        一个事物通常有两部分组成：数据和功能

​        一个对象通常有两部分组成：属性和方法

​        事物的数据到了对象中体现为属性

​        事物的功能到了对象中体现为方法



​        3.面向对象的编程

​          \- 面向对象的编程指，程序中的所有操作都是通过对象来完成

​          \- 做任何事情之前都要先找到它的对象

```
const jennie = {
            //添加属性
            name: "jennie",
            age: 29,
            height: 163,
            weight: 45,

            //添加方法
            dancing() {
                console.log(this.name + "ACE");

            },
            singing() {
                console.log(this.name + "天籁");

            }
        }
```



#### 类的简介

使用object创建对象的问题：

​        1.无法区分出不同类型的对象

​        2.不方便批量创建对象

​      在js中可以通过类（class）来解决这个问题

​        1.类是创建对象的模版，可以将对象中的属性和方法直接定义在类中

​          定义后，就可以直接通过类来创建对象

​        2.通过同一个类创建的对象，我们称为同类对象

​        可以使用instanceof来检查一个对象是否是由某个类创建

​        如果某个对象是由某个类所创建，则我们称该对象是这个类的实例

​        

​        语法：

​          class 类名 {}//类名要使用大驼峰命名

​          const 类名 = class{}

```
//person类专门用来创建人的对象
        class Person{

        }
        //animal类专门用来创建动物的对象
        class Animal{
            
        }
        const p1=new Person()//调用构造函数创建对象
        const p2=new Person()

        const a1=new Animal()
        const a2=new Animal()
        //console.log(Person);
        console.log(p1 instanceof Person);//true
        console.log(a1 instanceof Person);//false
        
        
        const jennie = {
            //添加属性
            name: "jennie",
            age: 29,
            height: 163,
            weight: 45,

            //添加方法
            dancing() {
                console.log(this.name + "ACE");

            },
            singing() {
                console.log(this.name + "天籁");

            }
        }
        const jisoo = {
            //添加属性
            name: "jisoo",
            age: 30,
            height: 162,
            weight: 45,

            //添加方法
            dancing() {
                console.log(this.name + "大姐");

            },
            singing() {
                console.log(this.name + "天籁");

            }
        }
        /* console.log(jennie);
        console.log(jisoo); */
```



#### 属性

```
<script>
        /* 
            类是创建对象的模板，要创建第一件事就是定义类
        */
        class Person {
            /*  类的代码块，默认就是严格模式
                    类的代码块是用来设置对象的属性的，不是什么代码都能写 
            */
            name="孙悟空"//Person的实例属性name,实例属性只能通过实例访问
            age=500

            //使用static声明的属性是静态属性（类属性），静态属性只能通过类访问
            static test="test静态属性"
            
        }
        const p1 = new Person()
       /*  p1.name="孙悟空"
        p1.age=500 */

        const p2 = new Person()
        /* p2.name="猪八戒"
        p2.age=300 */

        console.log(Person.test);
        console.log(p2);
        
        
    </script>
```



#### 方法

```
<script>
        
        class Person {
            name = "孙悟空"
            /* sayHello=function(){
                    //添加方法的一种方式
            } */

            sayHello() {
                console.log("大家好，我是"+this.name);//谁调方法谁就是当前实例，所以当前实例是p1
                
                //添加方法(实例方法),实例方法中this就是当前实例
            }
            static test(){
                //静态方法（类方法） 通过类来调用 静态方法中this指向的是当前类
                console.log("我是静态方法");
                
            }
        }
        const p1 = new Person()
        console.log(p1);
        p1.sayHello()
        Person.test()

    </script>
```



#### 构造函数

```
<script>
        /* 
        
        */
        /* class Person {
            //当我们在类中直接指定实例属性的值时，意味着我们创建的所有对象的属性都是这个值
            name = "孙悟空" 
            age = 500
            gender = "男"

            sayHello() {
                console.log(this.name);

            }
        }
        //创建一个Person的实例
        const p1=new Person("孙悟空","18","男")
        const p2=new Person("猪八戒","18","男")
        const p3=new Person("沙和尚","18","男")
        console.log(p1);
        console.log(p2);
        console.log(p3);
         */
        class Person {
            /* 在类中可以添加一个特殊的方法constructor
                该方法我们称为构造函数（构造方法）
                该方法会在调用类创建对象的时候执行
             */
            constructor(name, age, gender) {
                //console.log("构造函数执行", name, age, gender);
                //可以在构造函数中为实例属性进行赋值
                //在构造函数中，this表示当前所创建的对象
                this.name = name
                this.age = age
                this.gender = gender


            }
        }
        const p1 = new Person("孙悟空", "18", "男")
        const p2 = new Person("猪八戒", "18", "男")
        const p3 = new Person("沙和尚", "18", "男")
        console.log(p1);
        console.log(p2);
        console.log(p3);


    </script>
```



#### 封装

面向对象的三大特点：封装、多态、继承

​        

​      1.封装

​        \- 对象就是一个用来存储不同属性的容器

​        \- 对象不仅存储属性，还要负责数据的安全

​        \- 直接添加到对象中的属性并不安全，因为它们可以被任意的修改

​        \- 如何确保数据安全？

​          1.私有化数据

​            \- 将需要保护的数据设置为私有，只能在类内部使用

​          2.提供setter和getter方法来开放对数据的操作

​            \- 属性设置私有，通过getter和setter方法操作属性带来的好处

​              1.可以控制属性的读写权限

​              2.可以在方法中对属性的值进行验证

​     总结：

​      \- 封装主要用来保证数据的安全

​      \- 实现封装的方式：

​        1.属性私有化，加#

​        2.通过getter和setter方法来操作属性

​          get 属性名(){

​            return this.#属性

​          }

​          set 属性名(参数){

​            this.#属性=参数

​          }

```
class Person {
            //#address="花果山"//实例属性使用#开头就变成了私有属性，私有属性只能在类内部访问
            #name
            #age
            #gender
            constructor(name, age, gender) {
                this.#name = name
                this.#age = age
                this.#gender = gender
            }
            sayHello() {
                console.log(this.#name);

            }
            //getter方法，用来读取属性
            getName() {
                return this.#name
            }
            setName(name) {
                this.#name = name
            }
            getAge() {
                return this.#age
            }
            //setter方法，用来设置属性
            setAge(age) {
                if (age >= 0) {
                    this.#age = age
                }

            }
            get gender(){
                console.log("get执行了");
                
                return this.#gender
            }
            set gender(gender){
                this.#gender=gender
            }
        }
        const p1 = new Person("孙悟空", "18", "男")
        // p1.age=-11
        //p1.#age = 11
        p1.setAge(11)
        p1.gender="女"
        console.log(p1.gender);
```


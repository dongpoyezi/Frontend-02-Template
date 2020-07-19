学习笔记

week 3

运算符 和表达式

语法书 运算符 优先级关系
类型转换  引用类型

Member
   a.b
   a[b]
   Foo`string`
   Super.b
   super[‘b’]
   New.target
   New Foo()

New
     New Foo

例子   new a() ()  第一个括号是和左边new结合的
          new new a()   a() 是和后一个new 结合的


reference 引用类型  里面有 object 和key


Call 
   foo()
   super()
   foo()[‘b’]  
   foo().b
   foo()`abc`



左右手运算

a.b =c 可以
a+b = c 不行


update 自增 自减

单目运算符

delete a.b
Void foo()
Typeof a
+a
-a
~a
!a
Await a


**  乘方 右结合

expression



类型转换


 a+b 
“false” == false
a[0] =1





拆箱转换  把 Object转换成普通类型

ToPremitive   

比如object参与加法会调用ToPremitive

三个方法影响ToPremitive
 toString  valueOf
Symbol.toPrimitive



var o = {
     toString() { return “2” }
     valueOf() {return 1},
     [Symbol.toPrimitive]() {return 3}
}



console.log(“x”+o)
先调用Symbol.toPrimitive ，没有，掉用valueOf ,没有，调用toString()


装箱转换






运行时相关

语句

简单语句，组合语句，声明

简单语句
expressionStatement
Empty
Debugger
Throw
Continue
break
return



复合语句

block
If
Switch
Iteration
With
Labelled
Try

声明
function
Generator
Asyncfunction
asyncGenerator
variableStatement
Class
Lexical


Function    function *  async function  async function * var
Class const let


执行粒度

宏任务
微任务（promise）
函数调用
语句 声明
表达式
直接量 变量 this
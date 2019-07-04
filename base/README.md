# Javascript
Javascript 是交互性语言，是轻量级语言，`弱类型语言`，直译语言，它不需要编译便可以直接运行在浏览器中。
直译语言灵活性比较弱，如果一条执行不了，下面的语言就无法运行了。
<br>
<br>


<strong>为什么说是 '弱类型语言'</strong>
>**弱类型语言：Javascaript 它可以很简单的给变量赋值各种数据类型，所以是弱类型语言。** <br>
强类型语言： 不可以很简单的让变量转换成各种数据类型，称为强类型语言。比如 Java , c++ , Python

<br>

<strong>比如说：</strong>
```copy
console.log(a)                      //抛出错误异常 'a is not defined' 中断执行。
console.log(b)                      //不执行
console.log(c)                      //不执行
console.log('hello world')          //不执行
```

在没有声明变量 'a,b,c' 的情况下，直接运行代码会报错 `a is not defined` ，并且中断执行。

<br>

<strong>解决方法：</strong>

面对上面这种情况我们可以使用异常捕获方法 `try{} catch{}`。

```copy
try{
    console.log(a);                 //检测到异常 'a is not defined' 但是不抛出错误，位于它后面的代码不执行，直接运行 'catch' 里面的代码块
    console.log(b);                 //不执行
    console.log(c);                 //不执行
}catch(e){
    console.log('hello world');     //'hello world'
}
```
当 `try` 模块里面代码检测有异常的时候，不抛出异常，代码块内位于后面的代码不执行，执行 `catch` 代码块内的代码。

<br>


#### 总结
* `脚本语言`：Javascript 是一种解释型脚本语言，Javascript 在运行的过程当中逐行解释。而 C/C++ 需要编译之后才能解析<br>
* `基于对象`：Javascript 是一种基于对象的脚本语言，不仅可以创造对象，也可以使用现有的对象。<br>
* `弱类型语言`：Javascript 是一种弱类型脚本语言，它可以随时改变变量的数据类型。<br>
* `动态性`：Javascript 是一种动态类型脚本语言，它可以对用户的操作及时的作出响应。<br>
* `跨平台性`：Javascript 不以来任何操作系统，只要有浏览器就能运行。<br>

<br>

#### Tips
`Javascript` 中，控制台大致把报错信息分为两大类：
* `语法错误`（关于 `SyntaxError` 的这类错误导致浏览器不能正常预解析，使得这个 `js` 文件无法执行 ）；
* `抛出异常`（这类错误程序会执行到问题代码后停止继续往下执行）；

<br>
<br>

###### 常见的错误提示

<strong>SyntaxError-语法解析错误</strong>

`变量命名不规范的语法错误导致不能正常预解析，整段 js 无法运行`
```copy
console.log('1');
console.log('2');

var 1a = 'hello world'         //Uncaught SyntaxError: Invalid or unexpected token
                               //【无效的或者意外的标记】`1a` 变量命名不规范，导致整段 `js` 无法运行；

var 1 = 'hello world'          //Uncaught SyntaxError: Unexpected number
                               //【意外的数字】`1` 变量命名不规范，导致整段 `js` 无法运行；
```
<br>


`参数的不规范导致不能正常预解析，整段 js 无法运行`
```copy
console.log('1');
Math.max(2,4,-);               //Uncaught SyntaxError: Unexpected token )
                               //【意外的标记】括号里最后一个参数不符合规范；
```

<br>

<strong>Uncaught ReferenceError-引用错误</strong>

引用到没有定义的变量或者函数 `抛出异常`；
```copy
console.log('1')
console.log('2')
fun();                          //引用没有定义的 `fun`;
```


<br>

<strong>RangeError-范围错误</strong>

`抛出异常` - 超出范围值：有可能是长度范围超出了，有可能是参数的范围超出了；
```copy
[].length = -1;                 //长度的值 '-1' 超出了长度的有效范围值
6.666.toFixed(-1);              //参数中 '-1' 超出了有效范围值      
```

<br>

<strong>TypeError-类型错误</strong>

`抛出异常` - 变量或者参数不是预期的类型的时候，比如 `new` 一个字符串或者调用对象不存在。
```copy
var text = new 'hello world';       //"hello world" is not a constructor
var text = new  123123;             //"hello world" is not a constructor
var text = new  helloWorld;         //"hello world" is not a constructor

var target = {};
target.change();                    //target.change is not a function

```


<br>

<strong>URIError-类型错误</strong>
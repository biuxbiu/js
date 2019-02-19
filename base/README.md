# Javascript
Javascaript 是交互性语言，是轻量级语言，`弱类型语言`。
>**弱类型语言：Javascaript 它可以很简单的给变量赋值各种数据类型，所以是弱类型语言。** <br>
强类型语言： 不可以很简单的让变量转换成各种数据类型，称为强类型语言。比如 Java , c++ , Python

## 变量
变量是用于存储信息的“容器”，变量的值可以在整个程序中被修改。
```复制
var student = 'peter'
```
在上面的例子，student 被赋值为 'peter'。
>注意：Javascript 中区分大小写。<Br>
Peter 和 peter 是两个不同的变量。


## 数据类型
五种简单的数据类型：`数字 number`,`字符串 string`,`布尔 boolean`,`空 null`,`未定义 undefined`，<Br>一种复杂的数据类型：`对象 object`。


#### 数字 number
数据类型，可以带小数点，也可以不带。
```
var x = 34.00;      //有小数点
var x = 34;         //没有小数点
```
极大极小都可以通过科学技术方体现。
```
var y = 123e5;      //123*10的五次方 12300000
var y = 123e-5;     //123除以10的五次方 0.00123
```

#### 字符串 string
字符串是存储字符的变量，字符串是引号中的任意文本。
可以使用`单引号`或者`双引号`
```
var name = 'peter';     //使用单引号
var name = "peter";     //使用双引号
```
单引号里面可以有双引号，双引号里面可以有单引号。
```
var name = 'He is "peter"'      //He is "peter"
var name = "He is 'peter'"      //He is 'peter'
```
单（双）引号里面有单（双）引号需要转义。
```
var name = 'He is \'peter\''        //He is 'peter'
```

其它的转义情况

| 代码 | 输出 |
|:---:|:---:|
|\'|单引号|
|\"|双引号|
|\\|斜杠|
|\n|换行|
|\r|回车|
|\t|tab（制表符）|
|\b|推格符|
|\b|换页符|

#### 布尔 boolean
布尔类型只能有两个值，`true` 和 `false`。
```
var x = true;
var y = false;
```
>0,null,undefined,空字符串的时候，布尔值为 `false`。任何有值的字符串都为 `true`。<Br>
`空字符串`也表示有值，为 `true`。


## 算数运算符
算数运算符对数字或者文字或者变量执行算术运算。

| 交易所 | 货币类型 | 货币类型 |
| -------- | -------- | -------- |
| + | 加法 | y = x + 2 |
| - | 减法 | y = x - 2 |
| * | 乘法 | y = x * 2 |
| / | 乘法 | y = x / 2 |
| % | 取余 | y = x % 2 |
| ++ | 自增 | y = x++ |
| -- | 自减 | y = x-- |


#### 数字与其他类型中的运算
* 数字类型中，加法表示两个数的和。
```
var num = 2 + 3;        //5    =>  算术运算
```
* 数字与`变量`相加，为算数运算。
```
var x = 10;     //变量
var num = x + 2 + 3;        //15    =>  算术运算
```
* 数字与`字符串`相加为`拼接`效果，输出`字符串`。
```
var num = 1 + '10' ;     //'110'     =>  字符串拼接
```
* 数字与`字符串`相减为算数运算，输出数字。
```
var x = '10';        //字符串
var num = 1 - x;     //-9   =>  算术运算
```
* 数字与`undefined`相加输出 `NaN`。
```
var num = 1 + undefined;     //NaN  =>  算术运算
```
* 数字与`字符串的undefined`相加为`拼接`。
```
var num = 10 + 'undefined'       //'10undefined'    =>  字符串拼接
```
* 数字与`null`相加减为算数运算。
```
var num = 10 + null;       //10 null => 0（数字运算）
var num = 10 - null;       //10 null => 0（数字运算）
```

#### 字符串与其他数据类型之间的运算
* 字符串与`undefined`相加减，要注意`+`和`-`的输出结果不一样。
```
var num  = '123' + undefined;       //'123undefined'    =>  字符串拼接
var num  = '123' - undefined;       //NaN   =>  数字运算
```
* 字符串与`null`相加减
```
var num = '123' + null;     //'123null' =>  字符串拼接
var num = '123' - null;     //123   =>  算术运算
```
* 字符串与`boolean`相加减
```
var num = '123' + false;     //'123false' =>  字符串拼接
var num = '123' - false;     //123   =>  算术运算
var num = '123' + true;     //'123true' =>  字符串拼接
var num = '123' - true;     //122   =>  算术运算
```


#### null与其他数据类型之间的运算
* null与`undefined`相加减。
```
var num = null + undefined;       //NaN   =>  算术运算
var num = null - undefined;       //NaN   =>  算术运算
```
* null与`boolean`相加减。
```
var num = null + false;       //0  =>  算术运算
var num = null - false;       //0   =>  算术运算
var num = null + true;       //1    =>  算术运算
var num = null - true;       //-1   =>  算术运算
```

#### undefined与其他数据类型之间的运算
* undefined与`boolean`相加减。
```
var num = undefined + false;        //NaN   =>  算术运算
var num = undefined - false;        //NaN   =>  算术运算
var num = undefined + true;        //NaN   =>  算术运算
var num = undefined - true;        //NaN   =>  算术运算
```

#### 自增与自减
`x++` 自加一。
```
var num = 0;
for(var i=0;i<10;i++>){
}
```


## 比较运算符
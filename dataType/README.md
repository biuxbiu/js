## 数据类型

Javascript 中的数据类型大致分为以下几种：

* 原始数据类型：`string`/`number`/`boolean`
* 复合数据类型：`object`/`array`
* 特殊数据类型： `null`/`undefined`

#### 数值型-Number
* 整数
* 浮点数

###### 十进制
>我们日常中用的都是十进制

```copy
1.2         //整数
-2          //整数
-1.2        //浮点数
.222e30     //0.222乘以10的30次方
```
<br>

###### 十六进制
>（以 '0x' 开头）

```copy
0x0         //0
0xabcdef    //11259375
0xfff       //4095
```
<br>

###### 八进制
>八进制需要注意到一下几个地方：<br>
'0' 开头，至少有三位数，任何一位数不能超过 '7'，若有一位数超过 '7' 就不能以八进制看待;


```copy
01          //1
010         //8
011         //9
021         //17
01234       //668

0128        //128（第四位数超过 '7' 了，不能以八进制看待了）
```

* 八进制转十进制计算过程

```copy
01234       //4+3*8+2*8²1*8³ = 668
020         //0+2*8 = 16
021         //1+2*8 = 17
```

<br>

###### 特殊值
* 无穷大 Infinity

```copy
无穷大
    无穷大 Infinity
    1.79e309             //1.79 乘以 10 的 309 次方

    Infinity 负无穷大
    1.79e-309            //1.79 乘以 10 的 -309 次方
```

* NaN

```copy
NaN（not a number）
    NaN                  //是唯一一个不能与自身比较的值
    isNaN()              //检测值是否为 'NaN'
```

>NaN 是唯一一个不能与自身比较的值<br>
NaN === NaN   //false<br>

<br>

!>什么情况下会得出值 `NaN` ?

```copy
0/0                     //NaN（ 0 除以 0 的值为 'NaN'）
0/'hello world'         //NaN（ 0 除以 字符串 的值为 'NaN'）
'hello world'/0         //NaN（ 字符串 除以 0 的值为 'NaN'）

====================

/*要注意的是 '0' 与数字之间的运算*/
0/1                     //0
1/0                     //infinite
```

<br>

如何判断一个值是不是 `NaN` ?  
* `isNaN()` 用于判断括号里面的参数是否为 `NaN`;
* `isNaN()` 如果参数里的值不是数值，会强制将这个参数转换成数值（即使用 `Number()` ）再进行判断。;
* `null`（转换成 `0`） 和 `布尔值`（换成 `0` 或者 `1`） 都会被转换成数值，`0` 和 `1` 都是数值，所以 `isNaN()` 会返回 `false`;

各种情况如下：

|函数|结果|原因|
|:---|:---:|:---|
|isNaN(NaN)|true|is not a number|
|isNaN(undefined)|true|undefined(is not a number)|
|isNaN({})|true|object(is not a number)|
|isNaN(null)|false|null -> 0(is a number)|
|isNaN(false)|false|false -> 0(is a number)|
|isNaN(true)|false|true -> 1(is a number)|
|isNaN(37)|false|37(is a number)|
|isNaN('37')|false|Number('37') -> 37(is a number)|
|isNaN('37.37')|false|Number('37.37') -> 37.37(is a number)|
|isNaN('37,5')|true|Number('37,5') -> NaN(is not a number)|
|isNaN(37,5)|false|Number(37,5) -> 37(is a number)|
|isNaN('123asd')|true|Number('123asd') -> NaN(is not a number)|
|isNaN('')|false|Number('') -> 0(is a number)|
|isNaN(' ')|false|Number(' ') -> 0(is a number)|



#### 字符串-string
字符串是存储字符的变量，字符串是引号中的任意文本。
可以使用`单引号`或者`双引号`

```copy
var name = 'peter';     //使用单引号
var name = "peter";     //使用双引号
```

单引号里面可以有双引号，双引号里面可以有单引号。
```copy
var name = 'He is "peter"'      //He is "peter"
var name = "He is 'peter'"      //He is 'peter'
```

单（双）引号里面有单（双）引号需要转义。
```copy
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
```copy
var x = true;
var y = false;
```
>0,null,undefined,空字符串的时候，布尔值为 `false`。任何有值的字符串都为 `true`。<Br>
`空字符串`也表示有值，为 `true`。


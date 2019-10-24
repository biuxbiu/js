
## 运算符

运算符看似简单，但是实质上要完全理解运算符是一门很大的学问。

## 算数运算符
算数运算符对数字或者文字或者变量执行算术运算。

| 符号 | 描述 | 例子 |
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
```copy
var num = 2 + 3;        //5    =>  算术运算
```

<br>


* 数字与`变量`相加，为算数运算。
```copy
var x = 10;     //变量
var num = x + 2 + 3;        //15    =>  算术运算
```
<br>


* 数字与`字符串`相加为`拼接`效果，输出`字符串`。
```copy
var num = 1 + '10' ;     //'110'     =>  字符串拼接
```

<br>


* 数字与`字符串`相减为算数运算，输出数字。
```copy
var x = '10';        //字符串
var num = 1 - x;     //-9   =>  算术运算
```

<br>


* 数字与`undefined`相加输出 `NaN`。
```copy
var num = 1 + undefined;     //NaN  =>  算术运算
```

<br>


* 数字与`字符串的 undefined`相加为`拼接`。
```copy
var num = 10 + 'undefined'       //'10undefined'    =>  字符串拼接
```

<br>


* 数字与`null`相加减为算数运算。
```copy
var num = 10 + null;       //10 null => 0（数字运算）
var num = 10 - null;       //10 null => 0（数字运算）
```

<br>
<br>


#### 字符串与其他数据类型之间的运算
* 字符串与`undefined`相加减，要注意`+`和`-`的输出结果不一样。
```copy
var num  = '123' + undefined;       //'123undefined'    =>  字符串拼接
var num  = '123' - undefined;       //NaN   =>  数字运算
```
* 字符串与`null`相加减
```copy
var num = '123' + null;     //'123null' =>  字符串拼接
var num = '123' - null;     //123   =>  算术运算
```
* 字符串与`boolean`相加减
```copy
var num = '123' + false;     //'123false' =>  字符串拼接
var num = '123' - false;     //123   =>  算术运算
var num = '123' + true;     //'123true' =>  字符串拼接
var num = '123' - true;     //122   =>  算术运算
```


#### null与其他数据类型之间的运算
* null与`undefined`相加减。
```copy
var num = null + undefined;       //NaN   =>  算术运算
var num = null - undefined;       //NaN   =>  算术运算
```
* null与`boolean`相加减。
```copy
var num = null + false;       //0  =>  算术运算
var num = null - false;       //0   =>  算术运算
var num = null + true;       //1    =>  算术运算
var num = null - true;       //-1   =>  算术运算
```

#### undefined与其他数据类型之间的运算
* undefined与`boolean`相加减。
```copy
var num = undefined + false;        //NaN   =>  算术运算
var num = undefined - false;        //NaN   =>  算术运算
var num = undefined + true;        //NaN   =>  算术运算
var num = undefined - true;        //NaN   =>  算术运算
```

#### 自增与自减

|方法|说明|代码|解析|
|:---:|:---:|:---:|:---:|
|++|自增一|x=y++|会先输出 y 再自增|
|++|自增一|x=++y|先自增在输出 y|
|--|自减一|x=y--|会先输出 y 再自减|
|--|自减一|x=--y|先自减在输出 y|


## 比较运算符
在逻辑语句中使用比较运算符来比较两个`变量`或两个`值`之间的大小，结果返回 `true` 和 `false`。

假如 `var x = 0`;

|运算符|描述|比较|返回值|
|:---:|:---:|:---:|:---:|
|==|等于|x=='0'|true|
|==|等于|x==1|false|
|===|全等于|x===0|true|
|===|全等于|x==='0'|false|
|!=|不等于|x!=1|true|
|!=|不等于|x!=0|false|
|!==|不全等于|x!=='0'|true|
|!==|不全等于|x!==0|false|
|<|小于|x<0|true|
|>|大于|x>0|false|
|>=|大于等于|x>=0|true|
|>=|大于等于|x>='0'|true|
|<=|小于等于|x<=0|true|
|<=|小于等于|x<='0'|true|

>`==` 、 `!=` 比较的是两个 `值` 是否相等。<br>
`===` 、 `!==` 比较的是两个 `值和数据类型` 是否相等。

## 逻辑运算符
逻辑运算符，也称为`布尔运算符`，因为它比较后会输出`true`或者`false`。

假如`var x = 5`,`var y = 10`

|运算符|描述|比较|返回值|
|:---:|:---:|:---:|:---:|
|&&|并且|x>5&&y>=10|true|
|\|\||或者|x>5||y>=10|true|
|!|或者|取反||!(x>y)|true|

#### 三元运算

```copy
condition ? functionOne() : functionTwo();
```
`condition` 判断条件是否成立，成立返回`true`,不成立返回`false`<Br>
`true`执行`functionOne()`<Br>
`false`执行`functionTwo()`

引用逻辑运算符的例子我们可以写出三元运算如下
```copy
x>y ? console.log('true') : console.log('false');
```
如果 x>y 条件成立(condition)，返回`true`执行`console.log('true')`<Br>
如果 x>y 条件不成立(condition)，返回`false`执行`console.log('false')`


## 字符串运算符
实则为两个字符串拼接。

```copy
var firstName = 'biu'; 
var lastName = 'chan'; 
var student = firstName + lastName;     //两个字符串相加为拼接
```

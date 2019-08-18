## 变量
变量是用于存储信息的 `容器`，变量的值可以在整个程序中被修改。


<br>
<br>

#### 声明变量
```copy
var                                 //通过 `var` 关键字来申明一个变量；
var fruits;                         
    fruits = 'banner'               //可以先声明后赋值； 
var fruites , color , price;        //也可以通过 `逗号` 隔开同时声明多个变量；
var fruits  = 'Banana';             //声明变量的同时可以给变量赋值;
var fruits = 'Banana',              
    color = 'yellow' , 
    price = '12';                   //可以一次性给多个变量赋值;
var fruits = 12;                    //可以改变数据类型
var fruits = ‘hell world’;          //可以改变数据类型
var fruits = null;                  //可以改变数据类型
var fruits = 'Apple';               //变量重名会产生覆盖;
```

<br>
<br>


!>声明变量需要注意以下几种情况


```copy
var fruits;                     //声明变量但是没有赋值的时候输出 `undefined`；
var fruits , Fruits;            //变量区分大小写， `fruits` 和 `Fruits` 是两个变量；
var fruits , _Fruits;           //变量命名需要语义化，以 `字母或者下划线` 开始；
var FruitsColor , 
    fruitsColor , 
    fruits_color;               //变量命名最好遵循大小驼峰写法或者下划线写发；

=================
var 12b = 'text';               //杜绝数字开头的变量（Invalid or unexpected token）
var a = b = c = d = 0;          //`a` 是局部变量，`b` `c` `d` 是全局变量；
```

>我们可以通过删除变量来判断是全局变量还是局部变量。

<br>
<br>


#### 删除变量
用 `delete` 方法可以删除变量。
变量可以声明，也可以删除。<br>
删除变量要遵循以下几点：
* 所有 `var` 声明的变量都不可以删除（哪怕 `var` 的是全局变量）。
* 没有 `var` 声明的变量都可以删除。


<br>
<br>


<strong> 举个例子：</strong><br>

```copy
var x = 10;          //作用域使得 `x` 是个全局变量；
y = 20;              //定义来全局变量；

window.x = 10;
window.y = 20;          

delete window.x;        //false
delete window.y;        //true
```

<br>
<br>


**为什么 `var` 的变量不能删除？**

因为每个变量都有一个隐形的 `configurable` 属性。<br>
当 `configurable` 的属性为 `false` 的时候，就不能被删除。


<br>
<br>

`var` 的变量不可删除

```copy
var a = 10;
Object.getOwnPropertyDescriptor(window,'a');

//打印信息如下
{
    value: 10, 
    writable: true, 
    enumerable: true, 
    configurable: false                 //这个值为 `false` 因此不能删除
}
```

<br>
<br>

没有 `var` 的变量可删除

* configurable: true -- 可以修改

```copy
b = 10;
Object.getOwnPropertyDescriptor(window,'b');

//打印信息如下
{
    value: 10, 
    writable: true, 
    enumerable: true, 
    configurable: true                 //这个值为 `true` 因此可以删除
}
```

<br>
<br>


##  总结
了解变量声明方式和规则，变量的覆盖。


通过 `var` 关键字来声明一个变量，可以通过逗号隔开同时声明多个变量，声明变量的同时可以给变量赋值，可以一次性给多个变量赋值，变量重名会产生覆盖


# 函数
函数是用来执行特定任务的代码块。

>函数的好处是，只要定义一次，就可以多次调用。<br>
在函数中使用不同的参数就会产生不同的结果。


## 定义一个函数
函数定义有三个部分，`函数名`，`参数列表`，`函数体`。
```
function functionName(parameters){
    //执行的代码
}

function 函数名(参数列表){
    //函数体
}
```

定义一个名叫 print 的函数：
```
function print(){
    console.log('1');
}
```
## 函数参数
函数的参数列表中有分 `实参` 和 `形参` 。

举个例子：
```
function print(x){      //`x` 为变量，作为 `形参` 角色。
    console.log(x);
}

print(1);       //把 `1` 作为 `实参` 传入到函数当中去。
print(2);       //把 `2` 作为 `实参` 传入到函数当中去。
```

## 多参数
函数的参数列表中可以有多个参数 。
```
function sum(x,y){
    console.log(x+y)   
}

sum(1,2)        //`3`
```

`实参` 与 `形参` 对应的顺序需要一致。
```
function name(x,y){
    console.log('他的名字是' + x);
}

name('ken','peter');        //'他的名字是 ken'
name('peter','ken');        //'他的名字是 peter'

```
上面的例子，实参传入的值改变之后，输出的结果也跟着改变了。


## return-语句
一个函数内可以有一个 `return` 语句，`return` 语句用于返回函数的值，并终止函数往下执行。
>函数内有多个 `return` 语句的话，会从一个 `return` 语句开始终止函数，不往下执行。

```
function sum(x,y){
    return x;       //此处终止函数执行，并输出 `x` 的结果
    return y;
    return x+y;
}

sum(1,2);       //1;
```

>为什么有 `return` 的出现呢？因为你有时候需要进行计算并接收结果，所以你会需要用到 `return` 。

## alert-prompt-confirm
# HTML-DOM
通过 HTML DOM，可访问 JavaScript HTML 文档的所有元素。

## 什么是-DOM
`HTML DOM` (文档对象模型)，当页面在加载的时候，浏览器会创建页面的 `文档对象模型` ，`文档对象模型` 被构造为对象的树。

`Javascript` 可以改变页面中任何 `html` 元素<br>
`Javascript` 可以改变页面中任何 `html` 属性<br>
`Javascript` 可以改变页面中任何 `css` 样式<br>
`Javascript` 可以改变页面中任何所有时间做出反应。

`文档对象` 是网页中所有对象的所有者，或者说是根。

>所以要访问页面中的对象的话，始终要访问 `document` 对象。

实例：
```copy
document.body.innerHTML = 'hello world';
```

>由于 `body` 是 `dom` 节点，所以我们可以访问 `document` 来修改 `body` 的属性 `innerHTML`

## 选择元素

通过 `id` 找元素：
```copy
document.getElementById(id);
```

通过 `class` 找元素：
```copy
document.getElementByClassName(name);
```

通过 `tag` 找元素：
```copy
document.getElementByTagName(tag);
```

实例：
```copy
document.getElementById('demo');

document.getElementByClass('demo');

document.getElementByTagName('div')
```

## 改变属性
!>回顾一下，只有对象才有方法和属性。
## 第一章 原生AJAX
###  AJAX简介
**AJAX** 就是异步的js 和XML
通过在AJAX可以在浏览器中发送异步请求，最大的优势：**无刷新获取数据**
AJAX 不是新的编程语言 而是一种将现有的标准组合在一起使用的新方法。

###  XML简介
- XML可扩展标记语言
- XML被设计用来传输和存储数据
- XML和HTML 类似，不同的是HTML中的预定义标签，而XML中没有预定义标签，全都是自定义标签，用来表示一些数据

 ```js
//比如一个学生的数据
name = "孙悟空";age = 18;gender="男";
 ```
**用XML表示**
```
<student>
    <name>孙悟空</name>
    <age>18</age>
    <gender>男</gender>
</student>
```
现在被json取代
```
{"name": "孙悟空"，"age":18，"gender":"男"}
```

### AJAX的特点
#### AJAX的优点
1. 可以无需刷新页面与服务器端进行通信
2. 允许你根据用户事实来更新部分页面内容

#### AJAX的缺点
1. 没有浏览历史，不能回退
2. 存在跨域（同源）
3. SEO不友好

### AJAX的使用


## 第二章 jQuery中的AJAX

### get 请求
```js
$.get(url, [data], [callback], [type])
    url:请求的URL地址
    data:请求携带的参数
    callback:载入成功时回调函数
    type:设置返回内容格式，xml html script json text _default
```
### post请求
```js
$.post(url, [data], [callback], [type])
    url:请求的URL地址
    data:请求携带的参数
    callback:载入成功时回调函数
    type:设置返回内容格式，xml html script json text _default
```

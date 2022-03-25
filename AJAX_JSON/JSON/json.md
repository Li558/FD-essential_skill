# JSON教程

## JSON简介

- **JSON: JavaScript Object Notation（JavaScript 对象标记法）。**

- **JSON 是一种存储和交换数据的语法。**

- **JSON 是通过 JavaScript 对象标记法书写的文本。**

#### 什么是 JSON？

- JSON 指的是 JavaScript 对象标记法（*J*ava*S*cript *O*bject *N*otation）
- JSON 是一种轻量级的数据交换格式
- JSON 具有自我描述性且易于理解
- JSON 独立于语言

JSON 使用 JavaScript 语法，但是 JSON 格式是纯文本的。文本可被任何编程语言作为数据来读取和使用。

#### 为什么使用 JSON？

因为 JSON 格式仅仅是文本，它能够轻松地在服务器浏览器之间传输，并用作任何编程语言的数据格式。

JavaScript 提供內建函数把以 JSON 格式写的字符串转换为原生 JavaScript 对象：

```js'
JSON.parse()
```





#### 交换数据

当数据在浏览器与服务器之间进行交换时，这些数据只能是文本。

JSON 属于文本，并且我们能够把任何 JavaScript 对象转换为 JSON，然后将 JSON 发送到服务器。

我们也能把从服务器接收到的任何 JSON 转换为 JavaScript 对象。

以这样的方式，我们能够把数据作为 JavaScript 对象来处理，无需复杂的解析和转译。

#### 发送数据

如果您的数据存储在 JavaScript 对象中，您可以把该对象转换为 JSON，然后将其发送到服务器。

```js
var myObj = { name:"Bill Gates",  age:62, city:"Seattle" };
var myJSON =  JSON.stringify(myObj);
window.location = "demo_json.php?x=" + myJSON;
```

#### 接收数据

如果您以 JSON 格式接收到数据，您能够将其转换为 JavaScript 对象：

```js
var myJSON = '{ "name":"Bill Gates",  "age":62, "city":"Seattle" }';
var myObj =  JSON.parse(myJSON);
document.getElementById("demo").innerHTML = myObj.name;
```



#### 存储数据

把数据存储在本地存储中

```js
//存储数据：
myObj = { name:"Bill Gates",  age:62, city:"Seattle" };
myJSON =  JSON.stringify(myObj);
localStorage.setItem("testJSON", myJSON);

//接收数据：
text = localStorage.getItem("testJSON");
obj =  JSON.parse(text);
document.getElementById("demo").innerHTML = obj.name;
```

------------------------------------------

-------------------------------

------







-------------------

------------------------

-------

## Json语法

**JSON 语法是 JavaScript 语法的子集。**











#### JSON 语法规则

JSON 语法衍生于 JavaScript 对象标记法语法：

- 数据在名称/值对中
- 数据由逗号分隔
- 花括号容纳对象
- 方括号容纳数组

#### JSON 数据- 名称和值

JSON 数据写为名称/值对。

名称/值由字段名称构成，后跟冒号和值：

```js
"name":"Bill Gates"
```

JSON 名称需要双引号。而 JavaScript 名称不需要。

JSON – 求值为 JavaScript 对象

JSON 格式几乎等同于 JavaScript 对象。

在 JSON 中，键必须是字符串，由双引号包围：



#### JSON JavaScript

```js
//JSON
{ "name":"Bill Gates" }
//JAVASCRIPT
{ name:"Bill Gates" }
```

#### JSON 值

- 字符串
- 数字
- 对象（JSON 对象）
- 数组
- 布尔
- null

在 JavaScript 中，以上所列均可为值，外加其他有效的 JavaScript 表达式，包括：

- 函数
- 日期
- undefined

**在JSON中  字符串值必须用双引号编写**

**在 JavaScript 中，您可以书写使用双引号或单引号的字符串值：**

```json
//json
{ "name":"Bill Gates" }
//js
{ name:'Bill Gates' }
```

#### JSON 使用 JavaScript 语法

因为 JSON 语法由 JavaScript 对象标记法衍生而来,通过 JavaScript，您能够创建对象并向其分配数据.

```js
var person =  { name : "Bill Gates", age : 62, city : "Seattle" };

//返回Bill Gates 下面两种皆可以
person.name;
person["name"];

//修改数据
person.name = "Steve Jobs";
person["name"] = "Steve Jobs";


```

#### JavaScript 数组用作 JSON

与将 JavaScript 对象用作 JSON 相同，JavaScript 数组也可以用作 JSON。

#### JSON 文件

- JSON 文件的文件类型是 ".json"
- JSON 文本的 MIME 类型是 "application/json"

--------------

----------

------









---------------

-------------

--------

## JSON vs XML

**JSON 和 XML 均可用于从 web 服务器接收数据。**







#### JSON 实例

```js
{"employees":[
    { "firstName":"Bill", "lastName":"Gates" },
    { "firstName":"Steve", "lastName":"Jobs" },
    { "firstName":"Elon", "lastName":"Musk" }
]}
```

#### XML 实例

```xml
<employees>
    <employee>
         <firstName>Bill</firstName>
         <lastName>Gates</lastName>
     </employee>
     <employee>
         <firstName>Steve</firstName>
         <lastName>Jobs</lastName>
     </employee>
     <employee>
         <firstName>Elon</firstName>
         <lastName>Musk</lastName>
     </employee>
</employees>
```

#### JSON 类似 XML

- JSON 和 XML 都是“自描述的”（人类可读的）
- JSON 和 XML 都是分级的（值中有值）
- JSON 和 XML 都能被大量编程语言解析和使用
- JSON 和 XML 都能被 XMLHttpRequest 读取

#### JSON 与 XML 的差异

- JSON 不使用标签
- JSON 更短
- JSON 的读写速度更快
- JSON 可使用数组

最大的不同在于

**XML 必须使用 XML 解析器进行解析。而 JSON 可通过标准的 JavaScript 函数进行解析。**

#### JSON 比 XML 更好

- XML 比 JSON 更难解析。
- JSON 被解析为可供使用的 JavaScript 对象。

**对于AJAX应用程序，JSON 比XML更快更易用**

使用XML:

- 读取 XML 文档
- 使用 XML DOM 遍历文档
- 提取变量中存储的值

使用JSON：

- 读取 JSON 字符串
- JSON.Parse JSON 字符串

---------------------------

----------------------

-----------







------------

-------

-----------

## JSON 数据类型









#### 有效的数据类型

**在 JSON 中，值必须是以下数据类型之一：**

- 字符串
- 数字
- 对象（JSON 对象）
- 数组
- 布尔
- Null

**JSON 的值*不可以*是以下数据类型之一：**

- 函数
- 日期
- undefined

#### JSON 字符串

```js
{ "name":"John" }
```

#### JSON 数字

JSON 中的数字必须是整数或浮点数。

```js
{ "age":30 }
```

#### JSON 对象

JSON 中的值可以是对象。

```js
{
"employee":{ "name":"Bill Gates", "age":62, "city":"Seattle" }
}
```

JSON 中作为值的对象必须遵守与 JSON 对象相同的规则。

#### JSON 数组

JSON 中的值可以是数组。

```js
{
"employees":[ "Bill", "Steve", "David" ]
}
```

#### JSON 布尔

JSON 中的值可以是 true/false。

```js
{ "sale":true }
```

#### JSON null

JSON 中的值可以是 null。

```js
{ "middlename":null }
```

-------

------

---







----

-----

-----

## JSON.parse()

**JSON 的常规用途是同 web 服务器进行数据传输。**

**在从 web 服务器接收数据时，数据永远是字符串。**

**通过 JSON.parse() 解析数据，这些数据会成为 JavaScript 对象。**











#### 实例 – 解析 JSON

**接受文本**

```
'{ "name":"Bill Gates", "age":62, "city":"Seattle"}'
```

**JavaScript 函数 JSON.parse() 把文本转换为 JavaScript 对象**

```
var obj = JSON.parse('{ "name":"Bill Gates", "age":62, "city":"Seattle"}');
```

**书写**

```js
<p id="demo"></p> 

<script>
 document.getElementById("demo").innerHTML = obj.name + ", " + obj.age; 
</script>
```

#### 来自服务器的 JSON

通过使用 AJAX 请求从服务器请求 JSON。

只要服务器的响应是用 JSON 格式编写的，你可以将字符串解析成 JavaScript 对象。

```js
var xmlhttp = new XMLHttpRequest();
xmlhttp.onreadystatechange = function()  {
    if (this.readyState == 4 && this.status == 200) {
        myObj =  JSON.parse(this.responseText);
        document.getElementById("demo").innerHTML  = myObj.name;
    }
};
xmlhttp.open("GET", "json_demo.txt", true);
xmlhttp.send();

//文件内容
{
    "name":"Bill Gates",
    "age":62,
    "Cars":[
        { "car":"porsche", "model":"911" },
        { "car":"BMW", "model":"M5" },
        { "car":"Volvo", "model":"XC90" }
    ]
}
//结果是
Bill Gates
```

#### 作为 JSON 的数组

在对衍生自数组的 JSON 使用 JSON.parse() 后，此方法将返回 JavaScript 数组，而不是 JavaScript 对象

```js
var xmlhttp = new XMLHttpRequest();
xmlhttp.onreadystatechange = function()  {
    if (this.readyState == 4 && this.status == 200) {
        myArr =  JSON.parse(this.responseText);
        document.getElementById("demo").innerHTML  = myArr[0];
    }
};
xmlhttp.open("GET", "json_demo_array.txt", true);
xmlhttp.send();

//文件
[ "porsche", "BMW", "Volvo", "Audi" ]
```

#### 例外

**解析日期**

把字符串转换为日期

```js
var text =  '{ "name":"Bill Gates", "birth":"1955-10-28", "city":"Seattle"}';
var obj = JSON.parse(text);
obj.birth = new Date(obj.birth);
 
document.getElementById("demo").innerHTML = obj.name + ", " + obj.birth;
```

**第二个参数**

将字符串转换为日期

```js
var text =  '{ "name":"Bill Gates", "birth":"1955-10-28", "city":"Seattle"}';
var obj = JSON.parse(text, function (key, value) {
    if  (key == "birth") {
        return new Date(value);
    } else {
         return value;
   }});
 
document.getElementById("demo").innerHTML = obj.name + ", " + obj.birth;
```

**解析函数**

JSON 中不允许函数。

如果您需要包含函数，请把它写作字符串。

稍后您可以把它转换回函数：

```js
var text =  '{ "name":"Bill Gates", "age":"function () {return 62;}", "city":"Seattle"}';
var obj = JSON.parse(text);
obj.age = eval("(" + obj.age + ")");
 
document.getElementById("demo").innerHTML = obj.name + ", " +  obj.age();
//
Bill Gates,62
```

**您应该避免在 JSON 中使用函数，函数会丢失它们的作用域，而且您还需要使用 eval() 把它们转换回函数。**

----

----

---











----

----

----

## JSON.stringify()

**通过 JSON.stringify() 把 JavaScript 对象转换为字符串。**









#### 对 JS对象进行字符串化

**JS对象**

```js
var obj = { name:"Bill Gates", age:62, city:"Seattle"};
```

JSON.stringify() 将它转换为字符串

```js
var myJSON = JSON.stringify(obj);
```

结果将是遵守 JSON 标记法的一段字符串。myJSON 目前是一段字符串，并准备好送往服务器

```js
var obj = { name:"Bill Gates", age:62, city:"Seattle"};
var myJSON =  JSON.stringify(obj);
document.getElementById("demo").innerHTML = myJSON;
//结果
{"name":"Bill","age":62,"city":"Seatle"}
```

#### Stringify JavaScript 数组

```js
var arr = [ "Bill Gates", "Steve Jobs", "Elon Musk" ];
var myJSON =  JSON.stringify(arr);
document.getElementById("demo").innerHTML = myJSON;
//结果
["Bill Gates","Steve Jobs","Elon Musk"]
```

#### 例外

**日期字符串化**

```js
var obj =  { "name":"Bill Gates", "today":new Date(), "city":"Seattle"};
var myJSON = JSON.stringify(obj);
document.getElementById("demo").innerHTML = myJSON;

//结果
{"name":"Bill Gates","today":"2021-12-08T07:32:52.213Z","city":"Seattle"}
```

#### 函数字符串化

在 JSON 中，不允许函数作为对象值。

JSON.stringify() 函数将从 JavaScript 对象删除任何函数，包括键和值：

```js
var obj =  { "name":"Bill Gates", "age":function () {return 62;}, "city":"Seattle"};
var myJSON = JSON.stringify(obj);
document.getElementById("demo").innerHTML = myJSON;
//结果
{"name":"Bill Gates","city":"Seattle"}
```

如果您在运行 JSON.stringify() 函数前已将函数转换为字符串，这个环节可以省略。

```js
var obj =  { "name":"Bill Gates", "age":function () {return 62;}, "city":"Seattle"};
obj.age = obj.age.toString();
var myJSON = JSON.stringify(obj);
document.getElementById("demo").innerHTML = myJSON;
//结果
{"name":"Bill Gates","age":"function () {return 62;}","city":"Seattle"}
```

**避免在 JSON 中使用函数**

---

---

---











---

---

---

## JSON 对象









#### 对象语法

```js
{ "name":"Bill Gates", "age":62, "car":null }
```

- JSON 对象被花括号 {} 包围。

- JSON 对象以键/值对书写。

- 键必须是字符串，值必须是有效的 JSON 数据类型（字符串、数字、对象、数组、布尔或 null）。

- 键和值由冒号分隔。

- 每个键/值对由逗号分隔。

#### 访问对象值

**可以通过使用点号（.）来访问对象值**

```js
myObj =  { "name":"Bill Gates", "age":62, "car":null };
x = myObj.name;
```

**也可以使用方括号（[]）来访问对象值**

```js
myObj =  { "name":"Bill Gates", "age":62, "car":null };
x = myObj["name"];
```

#### 遍历对象

```js
myObj =  { "name":"Bill Gates", "age":62, "car":null };
for (x in myObj) {
   document.getElementById("demo").innerHTML  += x;
}
//结果
name
age
car
```

括号标记法

```js
myObj =  { "name":"Bill Gates", "age":62, "car":null };
for (x in myObj) {
   document.getElementById("demo").innerHTML  += myObj[x];
}
//结果
Bill Gates
62
null
```

#### 嵌套的 JSON 对象

```js
myObj =  {
   "name":"Bill Gates",
   "age":62,
   "cars": {
	  "car1":"Porsche",
	  "car2":"BMW",
	  "car3":"Volvo"
   }
}
```

通过使用点号和括号访问嵌套的 JSON 对象

```js
x = myObj.cars.car2;
BMW
//或者：

x = myObj.cars["car2"];
```

#### 修改值

使用点号来修改 JSON 对象中的任何值

```JS
myObj.cars.car3 = "Mercedes Benz";
```

也可以使用括号来修改 JSON 对象中的值

```JS
myObj.cars["car3"] = "Mercedes Benz";
```

#### 删除对象属性

delete 关键词来删除 JSON 对象的属性

```JS
delete myObj.cars.car1;
```

---

---

----













---

----

----

## JSON 数组

#### 作为 JSON 对象的数组









```js
[  "Porsche", "BMW", "Volvo" ]
```

JSON 中的数组几乎与 JavaScript 中的数组相同。

在 JSON 中，数组值的类型必须属于字符串、数字、对象、数组、布尔或 null。

在 JavaScript 中，数组值可以是以上所有类型，外加任何其他有效的 JavaScript 表达式，包括函数、日期和 undefined。

#### JSON 对象中的数组

数组可以是对象属性的值

```js
{
"name":"Bill Gates",
"age":62,
"cars":[ "Porsche", "BMW", "Volvo" ]
}
```

#### 访问数组值

通过使用索引号来访问数组值

```js
x = myObj.cars[0];
```



#### 遍历数组

通过使用 for-in 循环来访问数组值

```js
for (i in myObj.cars) {
     x  += myObj.cars[i];
}
//结果
Porsche
BMW
Volvo
```

可以使用 for 循环

```
for (i  = 0; i < myObj.cars.length; i++) {
    x  += myObj.cars[i];
}
//结果
Porsche
BMW
Volvo
```

#### JSON 对象中的嵌套数组

数组中的值也可以另一个数组，或者甚至另一个 JSON 对象

```js
myObj =  {
   "name":"Bill Gates",
   "age":62,
   "cars": [
	  { "name":"Porsche",  "models":[ "911", "Taycan" ] },
	  { "name":"BMW", "models":[ "M5", "M3", "X5" ] },
	  { "name":"Volvo", "models":[ "XC60", "V60" ] }
   ]
}
```

如需访问数组内部的数组，请对每个数组使用 for-in 循环

```js
for (i in myObj.cars) {
    x += "<h1>" + myObj.cars[i].name  + "</h1>";
    for (j in myObj.cars[i].models) {
         x += myObj.cars[i].models[j];
    }
}
//结果
Porsche
911
Taycan

BMW
M5
M3
X5

Volvo
XC90
V60
```

#### 修改数组值

使用索引号来修改数组

```js
myObj.cars[1] = "Mercedes Benz";
//结果
Porsche
BMW
Mercedes Benz
```



#### 删除数组项目

 delete 关键词来删除数组中的项目

```
delete myObj.cars[1];
//结果
Porsche
BMW
```

----

-----

----

















---

----

----

## JSON 服务器

**JSON 的一个常见用途是与 Web 服务器交换数据。**

**从 Web 服务器接收数据时，数据始终是字符串。**

**用 JSON.parse() 解析数据，数据会成为 JavaScript 对象。**







#### 发送 Data

如果您将数据存储在 JavaScript 对象中，则可以将对象转换为 JSON，并将其发送到服务器

```js
const myObj = {name: "Bill", age: 31, city: "New York"};
const myJSON = JSON.stringify(myObj);
window.location = "demo_json.php?x=" + myJSON;
```

#### 接收 Data

如果您接收 JSON 格式的数据，则可以轻松地将其转换为 JavaScript 对象

```js
const myJSON = '{"name":"Bill", "age":31, "city":"New York"}';
const myObj = JSON.parse(myJSON);
document.getElementById("demo").innerHTML = myObj.name;
```

#### 来自服务器的 JSON

您可以使用 AJAX 请求从服务器请求 JSON.只要来自服务器的响应以 JSON 格式编写，您就可以将字符串解析为 JavaScript 对象

**使用 XMLHttpRequest 从服务器获取数据**

```js
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myObj.name;
};
xmlhttp.open("GET", "json.txt");
xmlhttp.send();
```

#### 数组形式的 JSON

在从数组派生的 JSON 上使用 JSON.parse() 时，该方法会返回 JavaScript 数组，而不是 JavaScript 对象

**从服务器以数组返回的 JSON**

```js
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myArr = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myArr[0];
  }
}
xmlhttp.open("GET", "json_array.txt", true);
xmlhttp.send();
```

----

---

----

















-----

------

---

## JSON PHP

**JSON 的常规用途是从 web 服务器读取数据，然后在网页中显示这些数据。**

**本章向您讲解如何在客户端与 PHP 服务器之间交换 JSON 数据**







#### PHP 文件

PHP 提供处理 JSON 的内建函数

通过使用 PHP 函数 json_encode()，PHP 中的对象可转换为 JSON

```php
<?php
$myObj->name = "Bill Gates";
$myObj->age = 62;
$myObj->city = "Seattle";

$myJSON = json_encode($myObj);

echo $myJSON;
?>
 //结果
    {"name":"Bill Gates","age":62,"city":"Seattle"}
```



#### 客户端 JavaScript

这是客户端上的 JavaScript，使用 AJAX 调用来请求上例的 PHP 文件

使用 JSON.parse() 把结果转换为 JavaScript 对象

```js
var xmlhttp = new XMLHttpRequest();
xmlhttp.onreadystatechange = function()  {
    if (this.readyState == 4 && this.status == 200) {
         myObj = JSON.parse(this.responseText);
         document.getElementById("demo").innerHTML = myObj.name;
     }
};
xmlhttp.open("GET", "demo_file.php", true);
xmlhttp.send();
```

#### PHP 数组

在使用 PHP 函数 json_encode() 时，PHP 中的数组也将被转换为 JSON

```php
<?php
$myArr = array("Bill Gates", "Steve Jobs", "Elon Musk");

$myJSON = json_encode($myArr);

echo $myJSON;
?>
```

#### 客户端 JavaScript

这是客户端上的 JavaScript，使用 AJAX 调用来请求上例的 PHP 文件

使用 JSON.parse() 把结果转换为 JavaScript 对象

```js
var xmlhttp = new XMLHttpRequest();
xmlhttp.onreadystatechange = function()  {
    if (this.readyState == 4 && this.status == 200) {
         myObj = JSON.parse(this.responseText);
         document.getElementById("demo").innerHTML = myObj[2];
     }
};
xmlhttp.open("GET", "demo_file_array.php", true);
xmlhttp.send();
```

#### PHP 数据库

PHP 是服务器端编程语言，应该用于只能由服务器执行的操作

请使用 JSON.stringify() 将 JavaScript 对象转换为 JSON

```js
obj = { "table":"customers", "limit":10 };
dbParam = JSON.stringify(obj);
xmlhttp = new XMLHttpRequest();
xmlhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
        document.getElementById("demo").innerHTML  = this.responseText;
    }
};
xmlhttp.open("GET",  "demo_json_db.php?x=" + dbParam, true);
xmlhttp.send();
```

例子





#### PHP 方法 = POST

在向服务器发送数据时，通常最好是使用 HTTP POST 方法

```js
obj = { "table":"customers", "limit":10 };
dbParam = JSON.stringify(obj);
xmlhttp = new XMLHttpRequest();
xmlhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
         myObj = JSON.parse(this.responseText);
         for (x in myObj) {
             txt += myObj[x].name + "<br>";
        }
         document.getElementById("demo").innerHTML = txt;
    }
};
xmlhttp.open("POST", "demo_json_db.php", true);
xmlhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
xmlhttp.send("x=" + dbParam);
```

**PHP 文件中的唯一不同是获取被传输数据的方法**

#### PHP 文件

**使用 $_POST 而不是 $_GET**

```php
<?php
header("Content-Type: application/json; charset=UTF-8");
$obj =  json_decode($_POST["x"], false);
  
$conn = new mysqli("myServer", "myUser", "myPassword", "Northwind");
$result = $conn->query("SELECT name FROM ".$obj->$table." LIMIT ".$obj->$limit);
$outp = array();
$outp = $result->fetch_all(MYSQLI_ASSOC);

echo json_encode($outp);
?>
```

## JSON HTML

**JSON 非常易于转译为 JavaScript。**

**JavaScript 可用于在网页中生成 HTML。**







#### HTML 表格

使用作为 JSON 接收到的数据来生成表格

```html
obj = { "table":"customers", "limit":20 };
dbParam = JSON.stringify(obj);
xmlhttp = new XMLHttpRequest();
xmlhttp.onreadystatechange = function() {
    if (this.readyState == 4  && this.status == 200) {
        myObj = JSON.parse(this.responseText);
         txt += "<table border='1'>"
        for (x in myObj) {
             txt += "<tr><td>" + myObj[x].name + "</td></tr>";
        }
        txt += "</table>" 
        document.getElementById("demo").innerHTML  = txt;
    }
}
xmlhttp.open("POST", "json_demo_db_post.php", true);
xmlhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
xmlhttp.send("x=" + dbParam);
```

#### 动态 HTML 表格

使 HTML 表格基于下拉列表的值：选择一个选项： Customers Products Suppliers

```html
<select id="myselect" onchange="change_myselect(this.value)">
    <option value="">Choose an option:</option>
    <option value="customers">Customers</option>
    <option value="products">Products</option>
    <option value="suppliers">Suppliers</option>
</select>

<script>
function  change_myselect(sel) {
    var obj, dbParam, xmlhttp, myObj,  x, txt = "";
    obj = { "table":sel, "limit":20 };
     dbParam = JSON.stringify(obj);
    xmlhttp = new  XMLHttpRequest();
    xmlhttp.onreadystatechange =  function() {
        if (this.readyState  == 4 && this.status == 200) {
             myObj = JSON.parse(this.responseText);
             txt += "<table border='1'>"
             for (x in myObj) {
                 txt += "<tr><td>" + myObj[x].name + "</td></tr>";
             }
            txt +=  "</table>" 
             document.getElementById("demo").innerHTML = txt;
         }
    };
    xmlhttp.open("POST", "json_demo_db_post.php",  true);
    xmlhttp.setRequestHeader("Content-type",  "application/x-www-form-urlencoded");
    xmlhttp.send("x="  + dbParam);
}
</script>
```



#### HTML 下拉列表

用接收到的 JSON 数据来生成 HTML 下拉列表

```html
obj = { "table":"customers", "limit":20 };
dbParam = JSON.stringify(obj);
 xmlhttp = new XMLHttpRequest();
xmlhttp.onreadystatechange = function() {
    if (this.readyState == 4  && this.status == 200) {
        myObj = JSON.parse(this.responseText);
         txt += "<select>"
        for (x in myObj) {
             txt += "<option>" + myObj[x].name;
        }
        txt += "</select>" 
        document.getElementById("demo").innerHTML  = txt;
    }
}
xmlhttp.open("POST", "json_demo_db_post.php", true);
xmlhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
```

## JSONP

**JSONP 是一种无需考虑跨域问题即可传送 JSON 数据的方法。**

**JSONP 不使用 XMLHttpRequest 对象。**

**JSONP 使用 <script> 标签取而代之。**





#### JSONP 简介

JSONP 指的是 JSON with Padding。

从另一个域请求文件会引起问题，由于跨域政策。

从另一个域请求外部脚本没有这个问题。

JSONP 利用了这个优势，并使用 script 标签替代 XMLHttpRequest 对象

```js
<script src="demo_jsonp.php">
```

**Server 文件**

服务器上的文件在函数调用中封装结果

```php
<?php
$myJSON = '{ "name":"Bill Gates", "age":62, "city":"Seattle" }';
 
echo "myFunc(".$myJSON.");";
?>
//结果
    myFunc({ "name":"Bill Gates", "age":62, "city":"Seattle" });
```

**JavaScript 函数**

函数 "myFunc" 位于客户端，用于处理 JSON 数据

```
function myFunc(myObj)  {
    document.getElementById("demo").innerHTML =  myObj.name;
}
//结果
Bill Gates
```



#### 创建动态脚本标签

**修改**

```js
function clickButton() {
    var s = document.createElement("script");
    s.src = "demo_jsonp.php";
    document.body.appendChild(s);
}
```

#### 动态 JSONP 结果

可通过向 PHP 文件发送 JSON 来创建动态的例子，然后根据这个 php 文件获得的信息让它返回一个 JSON 对象

```php
<?php
header("Content-Type: application/json; charset=UTF-8");
$obj =  json_decode($_GET["x"], false);
 
$conn = new mysqli("myServer", "myUser", "myPassword", "Northwind");
$result = $conn->query("SELECT name FROM ".$obj->$table." LIMIT ".$obj->$limit);
$outp = array();
$outp = $result->fetch_all(MYSQLI_ASSOC);

echo "myFunc(".json_encode($outp).")";
?>
```

**PHP 文件解释：**

- 把请求转换为对象，使用 PHP 函数 json_decode()。
- 访问数据库，并用被请求的数据填充数组。
- 向对象添加数组。
- 使用 json_decode() 函数把该数组转换为 JSON。
- 用 "myFunc()" 封装返回对象。

**JavaScript 实例**

从 php 文件调用 "myFunc" 函数

```php
function clickButton() {
    var obj, s
    obj = { "table":"products", "limit":10 };
    s =  document.createElement("script");
    s.src = "jsonp_demo_db.php?x="  + JSON.stringify(obj);
    document.body.appendChild(s);
 }
function myFunc(myObj)  {
    var x, txt = "";
    for (x in myObj)  {
        txt += myObj[x].name + "<br>";
     }
    document.getElementById("demo").innerHTML = txt;
}
```

#### 回调函数

有时服务器文件提供回调函数作为参数

**PHP 文件会调用您作为回调参数传递的函数**

```js
function clickButton() {
    var s = document.createElement("script");
    s.src = "jsonp_demo_db.php?callback=myDisplayFunction";
    document.body.appendChild(s);
}
```
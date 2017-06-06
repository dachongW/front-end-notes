JavaScript 中的对象，和其它编程语言中的对象一样，可以比照现实生活中的对象来理解它。 JavaScript 中对象的概念可以比照着现实生活中实实在在的物体来理解。



### 对象分类

```javascript
var obj = {
```

- obj 是创建的对象名称。

```javascript
var date = new Date();// 创建一个 Date 对象
```

- 通过 JavaScript 提供的 Object 类型的构造函数来创建自定义对象，如下示例:

```javascript
var obj = new Object();// 创建一个自定义对象
```

### Object.create() 方法

Object.create() 方法创建一个拥有指定原型和若干个指定属性的对象。语法如下:

```javascript
Object.create(proto, [ propertiesObject ])
```

参数:

- proto 参数: 一个对象，作为新创建对象的原型。

通过 Object.create() 方法创建一个新对象，同时扩展自有属性:

```javascript
var flyer = {
```

Object.create() 方法的一些特殊用法:

- 创建一个原型为 null 的空对象。
var obj = Object.create( null );
```

- 实现子类型构造函数的原型继承父类型构造函数的原型。
Sub.prototype = Object.create( Super.prototype );
```

- 创建普通空对象。
var obj = Object.create( Object.prototype );
```

## 对象的属性

### 定义对象的属性

var myCar = new Object();
```

- JavaScript 对象的属性也可以通过方括号访问。对象有时也被叫作关联数组, 因为每个属性都有一个用于访问它的字符串值。
var myCar = new Object();
```

### 访问对象的属性

```javascript
var emp = { ename : 'Tom', salary : 3500 };
```

- JavaScript 对象的属性也可以通过方括号访问。
var emp = { ename : 'Tom', salary : 3500 };
```

### 遍历（枚举）属性


```javascript
var emp = { ename : 'Tom', salary : 3500 };

for (var n in emp){
    console.log(n, emp[n]);
}
```


```javascript
var emp = { ename : 'Tom', salary : 3500 };

var arr = Object.keys(emp);

for (var i=0;i<arr.length;i++){
    console.log(arr[i],emp[arr[i]]);
}
```

var emp = { ename : 'Tom', salary : 3500 };

var arr = Object.getOwnPropertyNames(emp);

for (var i=0;i<arr.length;i++){
    console.log(arr[i],emp[arr[i]]);
}
```

### 属性访问出错
//访问未声明的变量
```

### 检测对象的属性

- 使用 in 关键字。
console.log( 'ename' in emp );
```

- 使用 Object 对象的 hasOwnProperty() 方法。
console.log( emp.hasOwnProperty( 'ename' ));
```

- 使用 undefined 进行判断。
console.log( emp.ename === undefined );
```

- 使用 if 语句进行判断。
if( emp.ename ){
	console.log( 'ename属性存在' );
}
```

### 删除对象的属性

```javascript
// 创建一个 myobj 对象，具有 a 和 b 属性
```

## 对象的方法

```javascript
var obj = new Object();
```

### 调用对象的方法

- 通过点符号来访问一个对象的方法。
var obj = new Object();
```

- 也可以通过方括号访问一个对象的方法。
var obj = {
```

### 删除对象的方法

```javascript
var obj = {
```

> **值得注意的是:** 删除对象的方法时，不需要小括号“()”。如果有小括号则删除失败。
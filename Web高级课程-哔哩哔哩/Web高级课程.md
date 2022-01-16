[TOC]
## 1、ECMAScript 6基础

**ECMAScript 6 简介**

- JavaScript 三大组成部分

    - ECMAScript
    - DOM
    - BOM

- ECMAScript 发展历史 https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Language_Resources
- ECMAScript 包含内容：JS 中的数据类型及相关操作，流程控制，运算符及相关运算......

**ECMAScript 6**

### let 和 const

- let 和 var 的差异

    - let 允许声明一个在作用域限制在块级中的变量、语句或者表达式
      - 块级作用域
    - var 声明的变量只能是全局或者整个函数块的
    - let 不能重复声明
    
    - let 不会被预解析
    - 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/let
    
- const 常量

    - 常量不能重新赋值
    
    - 不能重复声明
    
    - 块级作用域
    
    - const 不会被预解析
    
    - 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/const
    
      
    
      <img src="images/es6/let 与 const 1.png" alt="let 与 const 1" style="zoom: 67%;" />
    
      <img src="images/es6/let 与 const 2.png" alt="let 与 const 2" style="zoom: 67%;" />
    
      <img src="images/es6/let 与 const 3.png" alt="let 与 const 3" style="zoom: 67%;" />
    
###     解构赋值

- 对象的解构赋值

- 数组的解构赋值

- 字符串的解构赋值

- 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment
        
  
  <img src="images/es6/解构赋值 1.png" alt="解构赋值 1" style="zoom:67%;" />
  
  <img src="images/es6/解构赋值(自定义名称) 2.png" alt="解构赋值(自定义名称) 2" style="zoom:67%;" />

### 展开运算符

- 对象展开

- 数组展开

- 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Spread_syntax

<img src="images/es6/展开运算符 1.png" alt="展开运算符 1" style="zoom:67%;" />

<img src="images/es6/展开运算符(不定参) 2.png" alt="展开运算符(不定参) 2" style="zoom:67%;" />

### Set 对象

- Set 对象的数据结构

- Set 相关属性和方法

    - size 属性
    - clear()、delete()、get()、has()、add()
    
- 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Set

<img src="images/es6/Set 对象 1.png" alt="Set 对象 1" style="zoom:67%;" />

### Map 对象

- Map 对象的数据结构

- Map 相关属性与方法

- size 属性

- clear()、delete()、get()、has()、set()

- 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Map

<img src="images/es6/Map 对象 1.png" alt="Map 对象 1" style="zoom:67%;" />

### 函数新增扩展

- 箭头函数

    - 箭头函数的各种写法
    
    - 箭头函数的this问题
    
    - 箭头函数的不定参问题
    
    - 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions
    
- rest 参数设置
- 参数默认值

<img src="images/es6/函数新增扩展(箭头函数) 1.png" alt="函数新增扩展(箭头函数) 1" style="zoom:67%;" />

<img src="images/es6/函数新增扩展(箭头函数 this) 2.png" alt="函数新增扩展(箭头函数 this) 2" style="zoom:67%;" />

<img src="images/es6/函数新增扩展(箭头函数 this) 3.png" alt="函数新增扩展(箭头函数 this) 3" style="zoom:67%;" />

<img src="images/es6/函数新增扩展(箭头函数) 4.png" alt="函数新增扩展(箭头函数) 4" style="zoom:67%;" />

### 新增数组扩展

- Array.from()、Array.of()

- find()、findIndex()、includes()
- flat()、flatMap()
- 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array

<img src="images/es6/新增数组扩展 1.png" alt="新增数组扩展 1" style="zoom:67%;" />

<img src="images/es6/新增数组扩展 2.png" alt="新增数组扩展 2" style="zoom:67%;" />

<img src="images/es6/新增数组扩展 3.png" alt="新增数组扩展 3" style="zoom:67%;" />

<img src="images/es6/新增数组扩展 4.png" alt="新增数组扩展 4" style="zoom:67%;" />

### 新增字符串扩展

- includes(), startsWith(), endsWith()
  
- repeat()
- 模板字符串
- 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String

<img src="images/es6/新增字符串扩展 1.png" alt="新增字符串扩展 1" style="zoom:67%;" />

<img src="images/es6/新增字符串扩展 2.png" alt="新增字符串扩展 2" style="zoom:67%;" />

### 新增对象扩展

- 属性简洁表示法

- 属性名表达式
- 手册地址：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object

<img src="images/es6/新增对象扩展 1.png" alt="新增对象扩展 1" style="zoom:67%;" />

### babel 使用

- Babel 是一个 JavaScript 编译器

- 手册地址：https://www.babeljs.cn/
- Babel 基本是否方法

<img src="images/es6/babel 使用 1.png" alt="babel 使用 1" style="zoom:67%;" />

### 案例一：员工列表

<img src="images/es6/案例一（员工列表）.jpg" alt="案例一（员工列表）" style="zoom:67%;" />

 [员工列表](案例\案例1（员工列表）\index.html) 

### 案例二：百度音乐全选

![案例二（百度音乐榜单）](images/es6/案例二（百度音乐榜单）.jpg)

 [百度音乐榜单](案例\案例2（百度音乐榜单）\index.html) 

## 2、面向对象

### 工厂模式

```js
//    工厂模式
function Tab(){
    //添加原料
    let obj = {};
    //加工原料
    obj.tablength = 1;
    obj.psFor = function(){
        console.log("psFor....");
    }
    //出厂
    return obj;
}

// function Page(){
//     return {
//         pagecount:1
//     };
// }
// 缺点一：
// 对象识别问题；

// let page = Page();

// console.log(tab1.constructor);

// tab1.psFor();
let tab1 = Tab();
let tab2 = Tab();
// tab2.psFor();
// 缺点二：性能问题；
// let str = new String();  //判断类型
// let obj = new Object();
// console.log(tab1.psFor===tab2.psFor);
// 公共空间：原型 prototype； ---》  new 运算符；
```

工厂模式解决了代码复用的问题，

1.但是却没有解决对象识别的问题。即创建的所有实例都是Object类型。(不清楚是哪个对象的实例)

2.没有原型，占用内存。

- 更好的方式？

##new运算符

- new的特点：1.new只能函数 2.自动创建空对象； 3.this绑定到空对象；4 隐式返还this；
- 通过new来改造工厂模式

##构造函数

- 构造函数要通过new来调用 this指向Student
- 约定俗成构造函数首字母大写

##构造函数性能对比工厂函数

- 公共空间存放公共方法

##构造函数原型

<img src="images/面向对象/prototypeimg.png" alt="prototypeimg" style="zoom: 25%;" />

### new 运算符

new运算符：1.执行函数；

​                       2.自动创建一个空对象； 

​                       3.把创建的对象指向另外一个对象；

​                       4.把空对象和函数里的this 衔接起来；(this指向实例化对象)

​                       5.隐式返还this；

```js
function test() {
    console.log("test..");
}
test(); // test..
new test(); // test..
//简化工厂模式；---->构造函数；
// 1.约定俗成：首字符大写；
// 2.属性放在构造函数；方法放在原型；
// let Tab = {}
function Tab() {
    // let obj = {};--->this;
    this.name = "张三";
    // this.hobby = function(){
    //     console.log("篮球");
    // }
    // return obj;
}
Tab.prototype.psFor = function () {
    console.log("psFor...");
};
Tab.prototype.hobby = function () {
    console.log("hobby...", this.name);
};
//每个原型上都有一个预定义属性； constructor---》构造函数；
// 覆盖原本 constructor属性；
Tab.prototype = {
    constructor: Tab,
    psFor() {
        console.log("psFor...");
    },
    hobby() {
        console.log("hobby...", this.name); // hobby... 张三
    },
};

let str = "1212fdsf";
// let str = new String("fdsfdsa");
if (str.constructor === String) {
    console.log("字符串");
} else {
    console.log("不是");
} // 字符串

Tab();
let tab1 = new Tab();
console.log(tab1.constructor === Tab); // true

console.log(tab1.__proto__ === Tab.prototype); // true
console.log(tab1.name); // 张三
tab1.hobby();
let tab2 = new Tab("张三", "lisi");
console.log(tab1.psFor === tab2.psFor); // true
tab2.hobby();
```

**仿写new 运算符**

```js
function myNew(constructor, ...arg) {
    let obj = {};
    constructor.call(obj, ...arg);
    obj.__proto__ = constructor.prototype;
    return obj;
}

let tab1 = myNew(Tab);
console.log(tab1.name) // 张三
tab1.psFor();
```

### prototype原型

- 通过new实例化出来的对象其属性和行为来自两个部分，一部分来自构造函数，另一部分来自原型。
- 当声明一个函数的时候，同时也申明了一个原型 。
- 原型本身是一个对象。
- 对象属性方法查找规则；

### 面向对象编程

 一、面相过程：注重解决问题的步骤，分析问题需要的每一步，实现函数依次调用；

 二、面相对象：面向对象编程是用抽象方式创建基于现实世界模型的一种编程模式；

三、面相对象特性： 抽象、 继承、封装、多态

### 对象和类

​	一、对象：具体的某个事物；(如：小明、叮当猫)

​	二、类：一类事物的抽象；(如：人类、猫类)

### 构造函数继承

- 继承：子类继承父类所有属性和行为，父类不受影响。
- 目的：找到类之间的共性精简代码

```js
function Person(name){
    this.name = name;
    this.eyes = "两只";
    this.legs = "两条";
}
function Student(name){
    Person.call(this,name)
    this.className = "二班";
}
let newPerson = new Student("张三");
console.log(newPerson.className);
```



- 简单原型继承,出现影响父类的情况；

  ```js
  function Person(name){
      this.name = name;
      this.eyes = "两只";
      this.legs = "两条";
  }
  function Student(name){
      Person.call(this,name)
      this.className = "二班";
  }
  Student.prototype = Person.prototype  //直接赋值
  ```





### 原型链

原型链是指对象在访问属性或方法时的查找方式。

1.当访问一个对象的属性或方法时，会先在对象自身上查找属性或方法是否存在，如果存在就使用对象自身的属性或方法。如果不存在就去创建对象的构造函数的原型对象中查找 ，依此类推，直到找到为止。如果到顶层对象中还找不到，则返回 undefined。

2.原型链最顶层为 Object 构造函数的 prototype 原型对象，给 Object.prototype 添加属性或方法可以被除  null 和 undefined 之外的所有数据类型对象使用。

<img src="images/面向对象/原型链.png" alt="原型链" style="zoom:33%;" />



### 原型的深拷贝继承

- 传值和传址问题

  - 基本数据类型：Number、String、Boolean、Null、Undefined
  - 复杂数据类型/引用数据类型:Array、Date、Math、RegExp、Object、Function等

- JOSN序列化的不足

  ```
  如果拷贝对象包含函数，或者undefined等值，此方法就会出现问题
  ```

- 浅拷贝和深拷贝

  ```js
  //递归深拷贝
  function deepCopy(obj){
      let newObj = Array.isArray(obj)?[]:{};
      for(let key in obj){
          if(obj.hasOwnProperty(key)){
              if(typeof obj[key] == "object"){
                  newObj[key] = deepCopy(obj[key]);
              }else{
                  newObj[key] = obj[key];
              }
          }
      }
      return newObj;
  }
  ```

  

###原型的继承

- 深拷贝继承

- 组合继承

  ```js
  function Dad(){
      this.name = "张三";
  }
  Dad.prototype.hobby = function(){
      console.log("喜欢篮球");
  }
  function Son(){
      Dad.call(this);
  }
  let F = function(){}
  F.prototype = Dad.prototype;
  Son.prototype = new F();
  Son.prototype.constructor = Son;
  
  let newSon = new Son();
  newSon.hobby();
  ```


### 案例一：多个选项卡

![案例一（多个选项卡）](images/面向对象/案例一（多个选项卡）.jpg)

 [多个选项卡](案例\案例2（多个选项卡）\1-多个选项卡改造构造 函数.html) 


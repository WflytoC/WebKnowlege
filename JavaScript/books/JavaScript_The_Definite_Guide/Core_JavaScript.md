* Lexical Structure
* Type,Values,and Variables
* Expressions and Operators
* Statements
* Objects
* Array
* Functions
* Classes and Modules
* Pattern Matching with Regular Expressions
* JavaScript Subsets and Extensions
* Server-Side JavaScript

####Lexical Structure

####Type，Values，and Variables

JavaScript类型分为两类：

* primitive types: number、string、boolean
* object types: 对象、数组和函数都属于该类型
* 特殊：null和undefined

对象是无序的name-value的集合。JavaScript定义了几种特殊的对象：

* 数组
* 函数

JavaScript是基于对象的语言，这意味着不是定义全局函数来操作这些类型的值，而是类型调用它们的方法。

在JavaScript中，null和undefined是唯一无法调用方法的值。

Infinity：isFinite(),除了NaN、Infinity、-Infinity返回true。

NaN：不是一个数字，isNaN()

模式匹配：

//之间的文本构成了正则表达式字面量。第二个/可以跟随一个或多个字符。RegExp对象和字符串都有对正则表达式操作的方法。

var pattern = /\d+/g; //pattern是RegExp对象，利用字面量语法。

全局对象：JavaScript解释器启动(或Web浏览器加载页面时)，它会创建一个新的全局对象，初始化属性。

包装对象：string、number、boolean不是对象，但是它们有属性和方法，当引用它们属性和方法时，JavaScript会将它们自动转化为对应的对象，String、Number、Boolean。一旦属性和方法被解析，新创建的对象就会被销毁。

JavaScript会根据需要来进行类型的自动转换。


####Expressions and Operators

####Statements

####Objects

一个对象除了可以拥有自己的属性外，也可以继承来自其它对象的属性，这叫做原型(prototype)。原型继承是JavaScript的关键特点。

An object's prototype is a reference to another object from which properties are inherited.

每个JavaScript对象都有与其相关联的第二个对象，叫作prototype，第一个对象继承自该prototype的属性。

JavaScript的所有类(即函数)都有一个prototype属性，当为JavaScript类的prototype属性添加函数、属性时，则可视为对原有类的扩展。


* 创建对象

		1.对象字面量：使用Object.prototype作为对象的prototype(原型)
		2.使用new来创建对象
			new关键字必须跟随一个函数调用，该函数叫作构造器(使用构造器函数的prototype属性作为对象的prototype(原型))
		3.Object.create()：使用第一个参数作为对象的prototype(原型)
* 查询和设置属性

		.或者[]
* 删除属性

		delete操作符只能删除自己的属性，不能删除继承来的属性。
* 测试属性

		检查对象是否有指定的属性：
			1.in操作符
			2.hasOwnProperty()
			3.propertyIsEnumerable()
* 遍历属性

		1.for/in循环
		2.Object.keys()
		3.Object.getOwnPropertyNames()
* 属性Getter和Setter

		var o = {
			data_prop: "wflyto",
			get accessor_pro() {
				return this.data_prop;
    		},
    		set accessor_pro(newValue) {
				this.data_prop = newValue + (new Date()).toString();
    		}
		}
* 属性Attribtes

		属性拥有attributes，可以声明属性是否可以写入、遍历和配置。
		
		Object.getOwnPropertyDescriptor({x: 1},""x); // 返回：{value：1,writable:true,enumerable:true,configurable:True}

		var o = {};
		Object.defineProperty(o,"x",{value: 1,writable:true,enumerable: false,configurable: true});
*  对象Attributes

		isPrototypeOf()：判断原型关系
		
*  序列化对象

		JSON.stringify();
		JSON.parse();
*  对象方法



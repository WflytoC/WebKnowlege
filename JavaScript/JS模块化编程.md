##Javascript模块化编程

模块就是实现特定功能的一组方法以及记录状态的变量。

####模块的写法：

* 原始写法
* 对象写法
* 立即执行函数写法

####使用模块

JavaScript模块规范有两种：CommonJS和AMD(Asynchronous Module Definition)。

* CommonJS(Webpack、browserify、nodejs)

		var math = require('math');
		math.add(2,3);
* AMD(requireJS)
		
		require(['math'],function(math) {
			math.add(2,3);
		});


####requireJS库的使用

		<script src="js/require.js" data-main="js/main"></script>
		其中，data-main属性指定网页程序的主模块，即整个网页的入口代码。

		require(['moduleA','moduleB','moduleC'],function(moduleA,moduleB,moduleC) {

		});

		AMD模块的写法：

		define(['myLib'],function(myLib) {
			function foo() {
				myLib.doSomething();
			}
			return {
				foo: foo
			}
		});
		
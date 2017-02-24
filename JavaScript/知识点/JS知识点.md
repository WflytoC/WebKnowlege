####prototype

使用prototype属性可以向对象添加属性和方法。

		function employee(name,job,born)
		{
			this.name=name;
			this.job=job;
			this.born=born;
		}

		var bill=new employee("Bill Gates","Engineer",1985);

		employee.prototype.salary=null;
		bill.salary=20000;

####hasOwnProperty

当判断对象属性存在时，hasOwnProperty是唯一可以依赖的方法,该方法判断一个属性是定义在对象本身而不是继承自原型链。

		var boy = {name: 'wflytoc'};
		Object.prototype.age = 21;

		boy.hasOwnProperty('age'); //false
		boy.hasOwnProperty('name'); //true

####splice

该方法改变数组的内容通过移除存在的元素或添加新的元素

		array.splice(start,deleteCount,item1,item2,...);


####js对象

JavaScript中的对象本质上是一个关联数组。

####js作用域

JavaScript没有块级作用域，而是函数作用域(函数体变量提升)

		var name = "A";
		if(true) {
			var name = "B";
		}
		console.log(name);//打印出B

		var name = "A";
		(function() {
			console.log(A);//打印出undefined(因为函数体内的name声明被提升了)
			var name = "B";
		})();

		上面的函数其实是：
		var name = "A";
		(function() {
			var name;
			console.log(A);
			name = "B";
		})();


####==与===

==：不同类型会转化为同一类型，然后看值是否相等；
===：如果类型不同，则结果就是不等。

####typeof与instanceof

两个都是操作符(类似于+)，而不是函数,因此不需要括号。

		var result = typeof name;
		
		var object = new Object();
		var result = object instanceof Object;
		
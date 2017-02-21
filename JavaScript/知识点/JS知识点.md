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
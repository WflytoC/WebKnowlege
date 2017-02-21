


####jQuery库

* jQuery库功能

		HTML元素选取与操作
		HTML事件函数
		CSS操作
		JavaScript特效与动画
		AJAX
		
* jQuery语法

		基础语法：
			$(selector).action()
			1.查询HTML元素
			2.action()执行对元素的操作
	
		$('#content').hide();

####jQuery选择器和事件

* 选择器：

		元素选择器：$("button")
		id选择器：$("#p2")
		类选择器：
* 事件常用方法：
	
		click：单击事件
		dblclick：双击事件
		mouseenter：鼠标移动到元素上事件
		mouseleave：鼠标离开元素事件

* 绑定、解除绑定事件

		bind("click",clickHandler);//1.7以后使用on
		unbind("click");//解除某事件，1.7以后使用off
		unbind("click",click);//解除某事件的指定处理器
* 事件目标与冒泡

		事件对象拥有的属性有：currentTarget(代码中绑定事件的元素)、target(实际发生事件的元素)。

		如果子元素和父元素绑定相同的事件，那么执行的顺序是从子元素到父元素。

		event.stopPropagation();停止父级元素的事件
		event.stopImmediatePropagation();停止所有的事件
* 自定义事件
		
		$("#click").click(function(){
			var e = jQuery.Event("MyEvent");//创建事件
			$("#click").trigger(e);//触发事件
		});
		$("#click").bind("MyEvent",function(e) {
			console.log(e);
		});


####捕获、设置、元素添加、元素删除

* 捕获

		获取元素内容：
			1. $("#content").text();//获取元素的内容
			2. $("#content").html();//可以获取子标签
		获取元素值(表单元素)：
			$("#input").val();//获取表单元素的值
		获取元素属性：
			$("#link").attr("href");		
	
* 设置

		设置/更改元素内容：
			1.$("#content").text("changed");
			2.$("#content").text("<a href=''>baidu</a>");//可以设置标签
		
		设置/更改元素值(表单元素)
			$("#input").val("modified");
		
		设置/更改元素属性：
			$("#link").attr("href","www.baidu.com");//修改单个属性值
			$("#link").attr({"href":"www.baidu.com","title":"baidu"});//修改多个属性值

		在设置/更改元素内容或属性值时，可以传入函数来设置新的值。
			$("#link").text(function(i,o) {
				return "new content";
			});//i是数字，o代表旧的值，返回值是新值

* 添加元素

		添加元素内容：
			1.append：在选中元素内容后面添加内容
			2.prepend：在选中元素内容前面添加内容
			3.before：在选中元素内容前面添加内容(需要换行)
			4.after：在选中元素内容后面添加内容(需要换行)
		
		添加元素：
			1.html："<p>ricky</p>"
			2.jQuery：$('<p></p>').text('ricky')
			3.DOM：document.createElement("p");
				
		
* 删除元素

		remove：删除所有内容
		empty：删除子元素

####效果之隐藏与显示、淡入淡出、滑动、回掉(都是利用display样式属性)

* 隐藏与显示

		$("#content").hide(1000);//隐藏
		$("#content").show(1000);//显示
		$("#content").toggle(1000);//切换隐藏、显示状态
* 淡入淡出(设置元素的透明度)

		$("#content").fadeIn(1000);元素透明度设为0；
		$("#content").fadeOut(1000);元素透明度设为1；
		$("#content").fadeToggle(1000);元素透明度在0和1切换；
		$("#content").fadeTo(1000,0.5);元素透明度设为0.5；
* 滑动

		$("#content").slideDown(1000);元素向下滑动以显示；
		$("#content").slideUp(1000);元素向上滑动以消失；
		$("#content").slideToggle(1000);元素向上滑动、向下滑动切换；
* 回调

		每个动画执行完毕之后可以执行的方法
		$("#content").hide(1000,function() {
			console.log("finish");
		});
		

####异步访问和加载片段

* 异步访问：

		1.$.get/post(url[,data][,success][,dataType]);
		
		2.$.get/post([settings]);
		
		3.$.ajax(url[,settings]);
		
		4.$.ajax([settings]) //1和2是$.ajax的简洁写法
* 加载片段：

		$("#content").load(url[,data][,complete]);从服务器中加载数据，将返回的HTML放到匹配的元素中。

		$.getScript("frag.js",function() {
			sayHello();
		})

####jQuery的扩展与noConflict

* 扩展

		1.$.sayHello = function(){};
		2.$.fn.sayGood = function() {
			$(this).text("Good");
		}
* noConflict

		为了防止其它框架使用$，jQuery使用noConflict()函数来避免命名冲突。只需调用$.noConflict()，然后用jQuery来替代$使用即可。

####CSS操作及jQuery的盒子模型

* CSS方法

		1.css("width")：获取属性值
		2.css("width"，"100px")：设置属性
		3.css({width:"100px",backgroundColor: ""#FF0000});设置一系列属性
		
		1.addClass()：为指定元素添加class(即样式)
				$("div").addClass("style1"）		
		2.removeClass():
		3.toggleClass();
* jQuery盒子模型

		1.height()：内容高度
		2.innerHeight()：内容高度 + 上、下内边距
		3.outerHeight([true])：如果无参数 - 内容高度 + 上、下内边距 + 上、下边框； 如果有参数 - 内容高度 + 上、下内边距 + 上、下边框 + 上、下外边距

####元素的遍历与过滤

* 向下遍历

		1.children([selector])：该方法只获取下一级子元素(儿子级)
		2.find(selector)：该方法可以获取任意级子元素
* 向上遍历

		1.parent([selector])：该方法值获取上一级父元素(父亲级)
		2.parents([selector])：该方法获取所有父级元素
		3.parentsUtil([selector])：该方法获取指定区间的父元素
* 同级遍历

		1.siblings():该方法获取所有同级别的元素
		2.next()：该方法获取下一个同级别的元素
		3.nextAll()：该方法获取下面所有同级别的元素
		4.nextUtil()：该方法获取指定区间的同级元素
		5.prev()：该方法回去上一个同级别的元素
		6.preAll()
		7.preUntil()
* 过滤

		1.$("div p").first()：该方法获取第一个元素
		2.$("div p").last()：该方法获取最后一个元素
		3.$("div p").eq(0)：该方法获取第一个元素
		4.$("div p").filter(".pclass")：该方法获取满足filter里选择器的元素
		5.$("div p").not(".pclass")


####菜单

* 垂直菜单布局
* 水平菜单布局

####标签切换

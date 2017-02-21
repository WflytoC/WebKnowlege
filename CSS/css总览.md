##知识总结

* CSS入门知识
* CSS基本样式
* CSS定位与浮动
* 盒子模型
* 常用操作

####CSS入门知识

* CSS介绍及语法：选择器分组和CSS继承
* 派生选择器

		<li>
			<strong>World</strong>
		</li>

		--css对strong标签应用样式
		li strong {
			color: red
		}
* id选择器
* 类选择器
* 属性选择器(IE6及以下不支持)
		
		<p title="main">
			Main content
		</p>

		--css对p标签应用样式
		[title] {
			color: red
		}
* 属性值选择器

		<p title="main">
			Main content
		</p>

		--css对p标签应用样式
		[title=main] {
			color: red
		}
	
####CSS基本样式

* 背景

		background-color: #eeeeef;背景颜色
		
		background-image: url("hill.jpg");背景图片
		
		background-position: center top;背景图片的起始位置
		
		background-repeat: 背景图片是否以及如何重复

		background-size: 1000px 1000px;背景图片大小

* 文本

		color: red; 文本字体颜色
		text-align: center;文本对齐方式
		text-indent: 2em;文本首行缩进
		text-shadow: 5px 5px 1px #FF0000;文本阴影
		word-wrap：;文本的换行规则
* 字体

		font-family字体系列
		font-size字体尺寸
		font-style字体风格
* 链接

		a:link
		a:visited
		a:hover
		a:active
		text-decoration属性用于去掉链接中的下划线
* 列表

		ul li {
			list-style-image: url("icon.jpg");
		}
		ul li {
			list-style-type: circle;
		}
* 表格

		border: 1px solid blue;表格边框
		border-collapse: collapse;表格折叠
* 轮廓	

####CSS定位与浮动

页面的设计需要通过摆放不同的模块在不同的位置。

* 定位

		CSS定位机制：
			1.普通流：元素按照其在HTML中的位置顺序决定排布的过程；
			2.浮动：

		CSS定位属性：
			1.position：把元素放在一个静态(static：偏移量没效果)的、相对(relative：偏移量是相对于元素原来的位置进行调整，其它元素的位置不受该元素偏移量的影响)的、绝对(absolute：不参与文档的结构，会随着页面滚动而滚动)的、固定(fixed：不参与文档的结构，不会随着页面滚动而滚动)的位置中
			2.top 向上偏移量(偏移量只有在指定position时才有效果，偏移量即距离指定边的距离)
			3.left 向左偏移量
			4.right 向右偏移量
			5.bottom 向下偏移量
			6.overflow 元素溢出其区域发生的事情
			7.clip 元素显示的形状
			8.vertical-align 垂直对齐方式
			9.z-index 堆叠顺序(元素重叠时有效果)
* 浮动

			1.float属性：left(元素向左浮动)、right(元素向右浮动)、none(元素不浮动)、inherit(从父级继承浮动属性)
			2.clear属性：规定元素的哪一侧不允许其它浮动元素(包括继承来的属性) -- left(去掉元素向左浮动)、right(去掉元素向右浮动)、both(左右两侧均去掉浮动)、inherit(从父级继承来clear的值)

			给元素的float属性赋值后，该元素【脱离文档流】，进行左右浮动，紧贴着父元素的左右边框。浮动元素在文档流中空出的位置，由后续的(非浮动)元素填充上去；【块级元素】直接填充上去，浮动元素会【覆盖】非浮动元素；【内联元素】有空隙就插入。

			【浮动元素】会脱离文档流，【块级非浮动元素】在文档结构中不受浮动元素影响，【内联元素非浮动元素】会受浮动元素影响


####盒子模型

	* 概述：margin、border、padding、content
	* 内边距：
	* 边框：
	* 外边距：
	* 外边距合并：选取【多的一方】作为合并后的外边距

####常用操作

* 对齐操作

		1.使用margin属性进行水平对齐：margin:0px auto；
		2.使用position属性进行左右对齐：
			position： absolute；
			left： 10%；
		3.使用float属性进行左右对齐
* 尺寸操作

		width、height、line-height、max-width、min-width、max-height、min-height
* 分类操作

		clear：设置一个元素的某个侧面是否允许其它的浮动元素
		cursor：当指向某元素只上时显示的指针类型
		display：是否以及如何显示元素(取值：inline、block)
		float：元素在哪个方向浮动
		position：
		visibility：是遏制元素是否可见
* 导航栏

		垂直导航栏
		水平导航栏
* 图片操作
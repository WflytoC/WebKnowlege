##知识总结

* CSS入门知识
* CSS基本样式

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
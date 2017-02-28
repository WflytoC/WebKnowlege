####变量(Variables)

Sass使用$符号来标记变量


		$primary-color: #333;

		body {
			color: $primary-color;
		}


####嵌套(Nesting)

Sass可以让你嵌套CSS选择器

		nav {
			ul {
				margin: 0;
				padding: 0;
				list-style: none;
			}
		}


####部分(Partials)

可以创建包含一小块CSS的部分Sass文件，文件名前面是下划线，例如_partial.scss。其它文件可以使用@import指令来导入该部分Sass文件。


####导入(Import)

		//_reset.scss
		html,
		body,
		ul,
		ol {
			margin: 0;
			padding: 0;
		}

		app.scss

		@import 'reset';

		body {
			font: 100% Helvetica,sans-serif;
			background-color: #efefef;
		}


####混合类型(Mixins)

mixin对CSS声明进行分组，甚至可以传入值来让mixin更加灵活。使用@mixin指令来创建mixin。

		@mixin border-radius($radius) {
  			-webkit-border-radius: $radius;
     		-moz-border-radius: $radius;
      		-ms-border-radius: $radius;
          	border-radius: $radius;
		}

		.box { @include border-radius(10px); }


####继承(Extend/Inheritance)

使用@extend让你共享来自某个选择器的CSS属性。

		.message {
			border: 1px solid #ccc;
			padding: 10px;
			color: #333;
		}

		.success {
			@extend .message;
			border-color: green;
		}

####操作符(Operators)

		article[role="main"] {
			float: left;
			width: 600px / 960px * 100%;
		}
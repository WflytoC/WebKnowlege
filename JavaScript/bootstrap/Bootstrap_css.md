####Bootstrap总览

* 移动优先

		<meta name="viewport" content="width=device-width, initial-scale=1">
* 容器

		Bootstrap需要容器元素来包含网页内容和存放我们的网格系统。共有两种容器，可以选择其中之一。

		<div class="container">
			//固定的宽度容器
		</div>

		<div class="container-fluid">
			//完全的宽度容器
		</div>


####网格系统(Grid system)

* 网格系统是通过一系列行(row)和列(column)来创建页面布局的
* 网格类适用于屏幕宽度【大于、等于】临界尺寸的设备，会[覆盖,即不起作用]掉针对更小设备的网格类。比如，对元素应用`.col-md-*`类，不仅仅会影响medium设备的样式，它也会影响large设备(如果`.col-lg-*`类没有设置的话)。

####排版(Typography)

####代码(Code)

####表格(Tables)

####表单(Forms)

####按钮(Buttons)

####图片(Images)

####辅助类(Helper classes)

####响应工具(Responsive utilities)
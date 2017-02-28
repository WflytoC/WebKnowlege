* CSS设置边距：顺时针 -- 上右下左

* margin的值为百分比时，相对于父级元素的width；padding的值为百分比时，相对于自身的width。

* 各浏览器的私有属性标记

		-moz：firefox浏览器私有属性
		-ms：IE浏览器私有属性
		-webkit：chrome、safari私有属性
		-o：opera私有属性
*  CSS 伪元素用于将特殊的效果添加到某些选择器

		
*  media query

		允许设计者针对不同的媒体设备定义不同的CSS样式。media query的语法：

		@media not|only 设备类型 [and 设备特性(支持min/max前缀)]

		@media screen and (max-width: 480px) {

		}

		@media screen and (min-width: 1000px) {

		}

####组件变形

		通过transform(指定变形函数：位移、缩放、倾斜、旋转、矩形变换)、transform-origin(设置变形的中心点)属性来实现组件变形。

		主流浏览器还未支持标准的transform属性，因此开发中还需要添加各浏览器厂商的前缀，例如：-moz-,-webkit-,-o-


####Transition动画

		Transition动画可以控制HTML组件的【某个属性】发生变化时会【经历一段时间】，以平滑渐变的方式发生变化。

		transition属性的值包括四个：
			transition-property：针对哪个CSS属性，当该属性发生变化时，系统就会使用指定的方式就行变化。
			transition-duration:动画持续时间
			transition-timing-function：指定渐变速度
			transition-delay：指定延迟时间

		主流浏览器还未支持标准的transform属性，因此开发中还需要添加各浏览器厂商的前缀，例如：-moz-,-webkit-,-o-

		img#target {
			position: absolute;
			-moz-transition: left 5s linear,top 5s linear;
			-webkit-transition: left 5s linear,top 5s linear;
			-o-transition: left 5s linear,top 5s linear;
		}	


####Animation动画

		CSS3提供了Tween动画支持：Animation动画，该种动画可以定义多个关键帧。

		@-webkit-keyframes 'wflytoc' {
			0% {
				left: 100px;
			}
			40% {
				left: 150px;
			}
			60% {
				left: 75px;
			}
			100% {
				left: 100px;
			}
		}
		div {
			background-color: gray;
			border: 1px solid black;
			position: absolute;
			left: 100px;
			width: 60px;
			height: 60px;
		}
		div:hover {
			-webkit-animation-name: 'wflytoc';
			-webkit-animation-duration: 5s;
			-webkit-animation-iteration-count: 1;
		}	

		
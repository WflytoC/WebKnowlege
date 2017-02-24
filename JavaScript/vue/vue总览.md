##Vue总览

####Vue实例

* Vue组件本质上是扩展的Vue实例
* 每个Vue实例会代理data对象中的所有属性。
* Vue实例暴露了许多有用的实例属性和方法(前缀$)
* 实例生命周期钩子：
		
		beforeCreated
		created
		beforeMount
		mounted
		beforeUpdate
		updated
		activated
		deactivated
		beforeDestroy
		destroyed

####模板语法

* Modifier：修改器(.)

		<form v-on:submit.prevent="onSubmit"></form>
* Filter：过滤器，用来进行文本格式化。过滤器函数将表达式的值作为第一个参数。
* 指令简写： v-bind: -- : v-on: - @

####计算属性和观察者

* computed
* watch

####Class和Style绑定

####条件渲染

`<template>`是不可见的容器

####列表渲染

####事件处理

* v-model

####表单输入绑定

####组件

* 使用Vue.component(tagName,options)来注册全局的组件。
* data必须是函数：传递给Vue构造器的大多数选项可以用在组件中，只有一个特殊：data必须是个函数。
* 复合组件：父-子组件关系 --props down，events up。

		通过props传递数据
		自定义事件
			$on(eventName)：监听事件
			$emit(eventName)：触发事件
* 使用`<slot></slot>`来管理父子内容
* 获取子组件引用：ref


####单文件组件
* Props和states
* render
* statics
* propTypes

####Props和states

组件的数据来自外部(props)或在内部初始化(states)


jsx转化为js：

		 <div>My First component</div>
		--
		React.createElement("div",null,"My First component");

通过this.props可以获取组件的所有属性。

通过getDefaultProps来设置组件的初始属性：

		getDefaultProps() {
			return {
				greeting: ""
			}
		}

states只能在组件内部使用，以下面的方法来设置states：

		getInitialState() {
			return {
				greeting: "Hello,World"
			};
		}

使用this.state来引用state。

每次state改变(调用this.setState()方法)时，ReactJS都会触发组件的重新渲染(即重新调用render()方法)。

####render

render是组件中唯一必须的方法，它应该返回一个子元素，例如JSX结构。如果不想渲染任何东西，可以返回null或false。

####statics

可以在组件中定义静态方法，然后可以利用组件来调用该方法。

		const Main = React.createClass({
			statics: {
				myMethod: (foo) => {
					return foo == "bar";
				}
			},
			render() {
				return null;
			}
		});

		console.log(Main.myMethod("bar"))

静态方法无法获取组件的props和state。

####propTypes

这个对象可以用来对传递给组件的属性值进行验证。


####组件生命周期方法

除了shouldComponentUpdate方法默认返回true外，其它生命周期方法都是空的。

* componentWillMount：组件第一次渲染之前调用(服务端应用可以调用该方法)

* componentDidMount：组件第一次渲染之后调用(服务端应用不要调用该方法)

* shouldComponentUpdate：返回true，则组件更新；返回false，组件不会更新

* componentWillReceiveProps(object nextProps)

* componentWillUpdate：该方法在render方法之前调用，组件首次渲染不会调用该方法

* componentDidUpdate：该方法在render方法之后调用，组件首次渲染不会调用该方法
* componentWillUnmount

####合成事件和虚拟DOM

* 虚拟DOM是真实DOM的简单实现，如果要在虚拟DOM中引用真实DOM元素，可以向元素中添加refs引用。ref="myReference"


		
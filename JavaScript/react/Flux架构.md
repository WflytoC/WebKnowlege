####Flux架构
Flux 是一种架构思想，专门解决软件的结构问题

实现：

* 官方的Flux
* Redux


####官方的Flux

Flux将一个应用分成四个部分：

* View：视图层
* Action(动作)：视图层发出的消息(比如mouseClick)
* Dispatcher(派发器)：用来接受Action、执行回掉函数
* Store(数据层)：用来存放应用的状态，一旦发生变动，就提醒Views要更新视图

Flux 的最大特点，就是数据的"单向流动"：

* 用户访问 View
* View 发出用户的 Action
* Dispatcher 收到 Action，要求 Store 进行相应的更新
* Store 更新后，发出一个"change"事件
* View 收到"change"事件后，更新页面

####Redux





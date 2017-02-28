####导航(标签条)

		<div class="container">
    		<ul id="mytab" class="nav nav-pills/navbar-default nav-justified" role="tablist">
    			<li role="presentation" class="active"><a href="#">Home</a></li>
    			<li role="presentation" ><a href="#">Guide</a></li>
    			<li role="presentation" ><a href="#">About</a></li>
    		</ul>
    	</div>

		利用js插件来实现点击切换标签条效果：

		$("#mytab a").click(function(e) {
    		e.preventDefault();
    		$(this).tab("show");
    	});

####导航条


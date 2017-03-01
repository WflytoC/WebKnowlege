Web性能主要指的时网站的加载速度。

Web浏览器如何与Web服务器通信：

		浏览器获取网页时，它通过HTTP来与服务器通信，浏览器发出HTTP请求，Web服务器会给出响应，包含状态码和内容。

		发出请求后，你会收到200 OK响应码(表明你请求的资源存在)和包含内容的响应(比如index.html)的响应。响应的内容(index.html)会被下载，并由Web浏览器来翻译。


网页是如何被加载的：浏览器下载好index.html后，会发现样式表的`<link>`标签、一些JavaScript文件的`<script>`标签，图片的`<img>`标签。浏览器发现这些引用后，就会发送新的HTTP请求来获取它们。


模拟网络链接：打开Chrome的开发者工具，点击`No throttling`右侧的下拉菜单，选择对应的网络情况。

审计网站：选中`Disable cache`，确保Record按钮是在允许的状态(红色)。

客户端网站的加载时间不同，不仅仅是因为网络连接情况，也因为加载网站的设备的特点。

改善网站性能的目标就是减少数据传输的量。


####压缩资源(Minify assets)

在基于文本的资源中去除空白符和其它不必要的字符。安装`minifier html-minify`用来压缩CSS、JavaScript和HTML资源。


####服务器压缩(Server compression)

Node服务器使用compression包

压缩建议：避免压缩那些已经压缩过的文件类型，比如JPED、PNG、GIF图片。

####优化图片(Optimize images)

网络服务：TinyPNG (http://tinypng.com)




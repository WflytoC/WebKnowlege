webpack.config.js是Webpack的配置文件，在该文件中，可以声明以下参数：

* entry
* output
* plugins
* module(模块加载器：打包之前对源文件进行转化，例如下面代码确保Babel将ES6转化为ES5)
* resolve

		var webpack = require("webpack");
		module.exports = {
			entry: ['./index.js'],
			output: {
					path: './',
					filename: 'bundle.js'
			},
			module: {
				loaders: [{
					test: /.js?$/,//正则表达式匹配，告诉Webpack该加载器操作哪些文件
					loader: 'babel',//用来转换代码的包的名称
					exclude: /node_modules/,//正则表达式匹配，忽略目录或文件
					query: {
						presets: ['es2015','react']
					}//包含加载器的特殊配置	
				}]	
			}

		}
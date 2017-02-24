##Webpack

webpack是现代JavaScript应用的模块打包器。

webpack除了import/export之外，不会改动其它任何代码。如果使用ES5特性，确保使用Babel等转换器。

webpack的四大核心概念：

* Entry
* Output
* Loaders:webpack中的加载器将这些文件转化为模块
* Plugins

		const HtmlWebpackPlugin = require('html-webpack-plugin'); //installed via npm
		const webpack = require('webpack'); //to access built-in plugins
		const path = require('path');

		const config = {
  			entry: './path/to/my/entry/file.js',
  			output: {
    			path: path.resolve(__dirname, 'dist'),
    			filename: 'my-first-webpack.bundle.js'
  			},
  			module: {
    			rules: [
      				{test: /\.(js|jsx)$/, use: 'babel-loader'}
    			] //在require()/import表达式中遇到.js或jsx时，使用babel-loader来转换它
  			},
  			plugins: [
    			new webpack.optimize.UglifyJsPlugin(),
    			new HtmlWebpackPlugin({template: './src/index.html'})
  			]
		};

module.exports = config;
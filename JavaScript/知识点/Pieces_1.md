####for与for-in遍历数组的区别

		var array=['a','b'];
		//标准的for循环
		for(var i=1;i<array.length;i++){
    		alert(array[i]);
		}
		//foreach循环
		for(var i in array){ //这里的i是数组的key，字符串类型
    		alert(array[i]);
		}

for-in循环会枚举原型链上的所有属性。
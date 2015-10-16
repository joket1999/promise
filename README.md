# ' primise'
提供简单的promise实现

## '简单例子'
```javascript
var wait = function(){
	var p = new Promise();
	var tasks = function(){
		console.log("执行完毕！");
		p.resolve();
	};
	setInterval(tasks, 1000);
	return p;
};

when(wait())
.then(function(){ console.log("哈哈，成功了！"); })
```
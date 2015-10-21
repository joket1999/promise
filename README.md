# ' primise'
提供简单的promise实现

## '简单例子'
```javascript
var wait = function(){
	var p = new Promise();
	var tasks = function(){
		console.log("执行完毕！");
		p.resolve('success');
	};
	setInterval(tasks, 1000);
	return p;
};

Promise.when(wait())
.then(function(req){ console.log(req); })
```

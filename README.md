# loadScripts
A tiny async loader for head scripts

e.g.:
```
Promise.all(loadScripts(
	[
		'./res/script/required/a.js',
		'./res/script/required/b.js',
		'./res/script/required/c.js'
    //,ecc..
	],{
		onload:([index,src,node])=>{
			console.log('loaded',{index,src,node})
		}
	})
).then(
	success=>{
		console.log('complete',success)
	}
).catch(case=>{
	console.log('wrong',case)
});
```

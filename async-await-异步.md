    ```javascript
    	function timeout(ms) {
	  return new Promise((resolve) => {
	    setTimeout(() => resolve(ms*2), ms);
	  });
	}
    	
	async function asyncPrint(ms) {
	  console.time('aaa');
	  const sec = await timeout(ms);
	  console.log(sec);

	  const sec2 = await timeout(sec);
	  console.log(sec2);

	  const sec3 = await timeout(sec2);
	  console.log(sec3);

	  console.timeEnd('aaa');
	  console.info('complete');
	}
	asyncPrint(500);
    	
	timeout(500).then(function(value){
		console.log(value);
		return timeout(value);
	}).then(function(value){
		console.log(value);
		return timeout(value);
	}).then(function(value){
		console.info('complete-promise: '+value);
	}).catch(function(error){
		throw new Error(error);
	});
    ```

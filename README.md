# JS-algorithm
##js算法综合，持续更新
###1.数组去重，主要是针对Object的使用，利用key来进行筛选
```
		function fnArr(arr){
			var chackTable={};
			var data=[];
			for(var i=0;i<arr.length;i++){
				if(!chackTable[arr[i]]){
					chackTable[arr[i]]=true;
					data.push(arr[i]);
				}
			}
			return data;
		}
		var testArr=[1,3,4,8,3,10,4,1];
		console.log(fnArr(testArr));
```

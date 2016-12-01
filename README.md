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


###2.冒泡排序
```
		var testArr=[6,3,2,3,0,4,1,9,6];
		function fnArr(arr){
			var data=[];
			for(var i=0;i<arr.length;i++){
				for(var j=0;j<arr.length-i;j++){
					if(arr[j]>arr[j+1]){
						arr[j]=arr[j]+arr[j+1];
						arr[j+1]=arr[j]-arr[j+1];
						arr[j]=arr[j]-arr[j+1];
					}
				}
			}
			return data=arr;
		}
		fnArr(testArr);

		//在这里补充一个小知识，***不借助临时变量，进行两个整数的交换
		//输入 a = 2, b = 4 输出 a = 4, b =2
		//这种问题非常巧妙，需要大家跳出惯有的思维，利用 a , b进行置换。
		//主要是利用 + – 去进行运算，类似 a = a + ( b – a) 实际上等同于最后 的 a = b;
		function swap(a , b) {  
			b = b - a;
			a = a + b;
			b = a - b;
			return [a,b];
		}
		//当然，这种置换也是很灵活的，就像上面的冒泡排序所用的跟着个就略有不同
```

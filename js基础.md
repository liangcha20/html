##  js基础

#####  引入方式 

- 行内式   直接元素绑定事件  

  ```js
  <input type="button" value="asa" onclick="alert('asda')">
  ```

- 内嵌式  用<script></script>存放代码
- 外部链接 <script src= "my.js"></script> 引入

#####  输入输出语句

-  alert()  浏览器弹出
- console.log(); 控制台输出
- prompt('请输入数据'); 弹框输入 输入的值是字符行

#####  变量

- 类型  简单数据类型 numer  string  boolean  null   undefined  复杂数据类型 object
- isNaN()判断非数字 是数字是返回false，不是返回true
- 字符串引号包裹   \n换行 \t tab  \b空格  转义符以\ 开头在字符串里面  字符串和其他类型相加结果为字符串
- 真值可以参与加法运算 当1和0
- 变量声明未赋值就是 undefined   未定义数据类型  和数字相加结果是nan
- null 和数字相加还是数字本身
- typeof（）检测数据类型

#####  数据类型转换

- 转换为字符型    num.toString()  String（变量） +拼接字符串
- 转换为数字型   parseInt(string)  parseFloat(string)  将string转换为数值型
- 转换为boolean型  Boolean（）代表空 undefined  null 0 nan 空字符串的会转换为false 其他为true

#####  数组

- 索引 arr[1],arr[0],arr[3]

- join，就是把数组转换成字符串，然后给他规定个连接字符，默认的是逗号( ，)

  书写格式：join(" ")，括号里面写字符串 ("要加引号"),

  ```js
  var arr = [1,2,3]; 
  console.log(arr.join()); 　　　　// 1,2,3 
  console.log(arr.join("-")); 　　// 1-2-3 c
  onsole.log(arr); 　　　　　　　　// [1, 2, 3]（原数组不变）
  ```

- push(): 把里面的内容添加到数组末尾，并返回修改后的长度。

  pop()：移除数组最后一项，返回移除的那个值，减少数组的length。

  　　　　书写格式：arr.push(" ")，括号里面写内容 ("字符串要加引号"),

  　　　  书写格式：arr.pop( )

  ```js
  var arr = ["Lily","lucy","Tom"]; 
  var count = arr.push("Jack","Sean"); 
  console.log(count); 　　　　　　　　　　// 5 
  console.log(arr); 　　　　　　　　　　　// ["Lily", "lucy", "Tom","Jack","Sean"] 
  var item = arr.pop(); 
  console.log(item); 　　　　　　　　　　 // Sean 
  console.log(arr); 　　　　　　　　　　  // ["Lily", "lucy", "Tom", "Jack"]
  ```

- **shift()：删除原数组第一项，并返回删除元素的值；如果数组为空则返回undefined 。** 

  **unshift:将参数添加到原数组开头，并返回数组的长度 。**

  　书写格式：arr.shift(" ")，括号里面写内容 ("字符串要加引号"),

  ```js
  var arr = ["Lily","lucy","Tom"]; 
  var count = arr.unshift("Jack","Sean"); 
  console.log(count); 　　　　　　　　　　　　　　// 5 
  console.log(arr); 　　　　　　　　　　　　　　　//["Jack", "Sean", "Lily", "lucy", "Tom"] 
  var item = arr.shift(); 
  console.log(item); 　　　　　　　　　　　　　　// Jack 
  console.log(arr); 　　　　　　　　　　　　　　 // ["Sean", "Lily", "lucy", "Tom"]
  ```

- **sort()：将数组里的项从小到大排序**

  书写格式：arr.sort( )

  ```js
  var arr1 = ["a", "d", "c", "b"];
  console.log(arr1.sort()); 　　　　　　　　　　// ["a", "b", "c", "d"]
  ```

  sort()方法比较的是字符串，没有按照数值的大小对数字进行排序，要实现这一点，就必须使用一个排序函数

  ```js
  function sortNumber(a,b) 
  { 　return a - b }
  arr = [13, 24, 51, 3]; 
  console.log(arr.sort()); 　　　　　　　　　　// [13, 24, 3, 51] 
  console.log(arr.sort(sortNumber)); 　　　　// [3, 13, 24, 51](数组被改变)
  ```

- reverse()：反转数组项的顺序。

  书写格式：arr.reverse( )

  ```js
  var arr = [13, 24, 51, 3]; 
  console.log(arr.reverse()); 　　　　　　　　//[3, 51, 24, 13] 
  console.log(arr); 　　　　　　　　　　　　　　//[3, 51, 24, 13](原数组改变)
  ```

- concat() ：将参数添加到原数组中。这个方法会先创建当前数组一个副本，然后将接收到的参数添加到这个副本的末尾，最后返回新构建的数组。在没有给 concat()方法传递参数的情况下，它只是复制当前数组并返回副本。

  书写格式：arr.concat()，括号里面写内容 ("字符串要加引号"),

  ```js
  var arr = [1,3,5,7]; 
  var arrCopy = arr.concat(9,[11,13]); 
  console.log(arrCopy); 　　　　　　　　　　　　//[1, 3, 5, 7, 9, 11, 13] 
  console.log(arr); 　　　　　　　　　　　　　　// [1, 3, 5, 7](原数组未被修改)
  ```

- **slice()：返回从原数组中指定开始下标到结束下标之间的项组成的新数组。slice()方法可以接受一或两个参数，即要返回项的起始和结束位置。在只有一个参数的情况下， slice()方法返回从该参数指定位置开始到当前数组末尾的所有项。如果有两个参数，该方法返回起始和结束位置之间的项——但不包括结束位置的项。**

  　书写格式：arr.slice( 1 , 3 )

  ```js
  var arr = [1,3,5,7,9,11]; 
  var arrCopy = arr.slice(1); 
  var arrCopy2 = arr.slice(1,4); 
  var arrCopy3 = arr.slice(1,-2); 
  var arrCopy4 = arr.slice(-4,-1); 
  console.log(arr); 　　　　　　　　　　　　　　//[1, 3, 5, 7, 9, 11](原数组没变) 
  console.log(arrCopy); 　　　　　　　　　　　 //[3, 5, 7, 9, 11] 
  console.log(arrCopy2); 　　　　　　　　　　　//[3, 5, 7] 
  console.log(arrCopy3); 　　　　　　　　　　　//[3, 5, 7] 
  console.log(arrCopy4); 　　　　　　　　　　　//[5, 7, 9]
  ```

  　　arrCopy只设置了一个参数，也就是起始下标为1，所以返回的数组为下标1（包括下标1）开始到数组最后。 

  　　arrCopy2设置了两个参数，返回起始下标（包括1）开始到终止下标（不包括4）的子数组。 

  　　arrCopy3设置了两个参数，终止下标为负数，当出现负数时，将负数加上数组长度的值（6）来替换该位置的数，因此就是从1开始到4（不包括）的子数组。 

  　　arrCopy4中两个参数都是负数，所以都加上数组长度6转换成正数，因此相当于slice(2,5)。

- splice()：删除、插入和替换。

  删除：指定 2 个参数：要删除的第一项的位置和要删除的项数。

  　　　　书写格式：arr.splice( 1 , 3 )

  插入：可以向指定位置插入任意数量的项，只需提供 3 个参数：起始位置、 0（要删除的项数）和要插入的项。

  　　　　书写格式：arr.splice( 2,0,4,6 )
  替换：可以向指定位置插入任意数量的项，且同时删除任意数量的项，只需指定 3 个参数：起始位置、要删除的项数和要插入的任意数量的项。插入的项数不必与删除的项数相等。

  　　　　书写格式：arr.splice( 2,0,4,6 )

  ```js
  var arr = [1,3,5,7,9,11]; 
  var arrRemoved = arr.splice(0,2); console.log(arr); 　　　　　　　　　　　　　　　//[5, 7, 9, 11] 
  console.log(arrRemoved); 　　　　　　　　　　　//[1, 3] 
  var arrRemoved2 = arr.splice(2,0,4,6); 
  console.log(arr); 　　　　　　　　　　　　　　　// [5, 7, 4, 6, 9, 11] 
  console.log(arrRemoved2); 　　　　　　　　　　// [] v
  ar arrRemoved3 = arr.splice(1,1,2,4); 
  console.log(arr); 　　　　　　　　　　　　　　　// [5, 2, 4, 4, 6, 9, 11] 
  console.log(arrRemoved3); 　　　　　　　　　　//[7]
  ```

- **indexOf()：接收两个参数：要查找的项和（可选的）表示查找起点位置的索引。其中， 从数组的开头（位置 0）开始向后查找。**

  　　　　书写格式：arr.indexof( 5 )

  ***\*lastIndexOf：接收两个参数：要查找的项和（可选的）表示查找起点位置的索引。其中， 从数组的末尾开始向前查找。\**** 

  　　　　书写格式：arr.lastIndexOf( 5,4 )

  ```js
  var arr = [1,3,5,7,7,5,3,1]; 
  console.log(arr.indexOf(5)); 　　　　　　//2 
  console.log(arr.lastIndexOf(5)); 　　　 //5 
  console.log(arr.indexOf(5,2)); 　　　　 //2 
  console.log(arr.lastIndexOf(5,4)); 　　//2 
  console.log(arr.indexOf("5")); 　　　　 //-1
  ```

- **forEach()：对数组进行遍历循环，对数组中的每一项运行给定函数。这个方法没有返回值。参数都是function类型，默认有传参，参数分别为：遍历的数组内容；第对应的数组索引，数组本身。**

  　　　　书写格式：arr.forEach()

  ```js
  var arr = [1, 2, 3, 4, 5]; 
  arr.forEach(function(x, index, a){ 
      console.log(x + '|' + index + '|' + (a === arr)); 
  }); // 输出为： // 1|0|true // 2|1|true // 3|2|true // 4|3|true // 5|4|true
  ```

##### 对象

遍历对象  

```js
for (k  in  obj){  
	console.log(k); //得到的是属性名
    console.log(obj[k]) //得到的是属性值
}
```

##### 字符串方法 #####

- indexof （‘要查找的字符‘，起始位置） lastindexof 相同从后往前找  只返回第一个位置
- str.charAt(0)  /str[0] 返回字符串中第一个字符
- str.substr（起始位置，长度）str.substring(起始位置，结束位置)
- str.replace( 被替换字符，替换字符)  只替换第一个
- str.split ('分隔符') 字符串转为数组
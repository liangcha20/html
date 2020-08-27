##  js dom

######  dom  文档 对象  模型   提供接口

- 一个页面就是一个文档 ，所有标签都是元素，所有内容 (标签、属性、文本、注释等)都是节点
- script 写在标签后面 ，网页时顺序加载

#####  获取元素

- 通过 id   

  ```js
  var as = document.getElementById('sd');
  console.log(as);
  ```

    注意参数是字符串  返回的是整个标签

- 通过 标签名  

  ```js
  var cd = document.getElementsByTagName('p')  
  console.log(cs);
  ```

   注意参数是字符串  返回的是元素对象的集合 以伪数组的形式存储  没有返回的空的伪数组   

   如果通过父元素获取其中的子元素   ，父元素必须是单个对象

  ```js
  var cd = document.getElementsByTagName('div')
  console.log(cd[0].getElementsByTagName('p'));//指明父元素对象
  ```

- html5 新增   

  根据类名  

  ```js
    var nam = document.getElementsByClassName('div')
    console.log(nam);
  ```

  选择第一个元素对象

  ```js
   var ne = document.querySelector('div');
    console.log(ne);
   var nf = document.querySelector('#ar'); //id和类名要加#和.号
     console.log(nf);
  ```

- 获取body 元素

  ```js
   var bn= document.body;
   console.log(bn);
  ```

- 获取html元素

  ```js
   var ht = document.documentElement;
    console.log(ht);
  ```

##### 事件 #####

- 鼠标事件  onclick 左键点击 onmouseover 鼠标经过  

#####  改变元素内容

- element.innerText   全部内容 输出时去除空格和换行 不识别html标签  在替换内容里添加会直接显示

  ```js
     <div>
              <span>moug</span>
              <button  style="background-color:transparent ; border :0px;outline:none; ">asd</button>
          </div>
   
           var bu = document.querySelector('button')
           var  sp = document.querySelector('span')//点击显示
           bu.onclick = function (){
              sp.innerText = '18:00'
           }
  var er = document.getElementById('er')//不点击就显示
  er.innerHTML = avf();
  ```

  

- element.innerHTML  输出时保留空格和换行 识别html标签

#####  修改元素属性   p18

   1、获取元素 

```js
 var af = document.getElementById('af');
 var ag = document.getElementById('ag')
```

  2、 注册事件  处理程序

```js
  ag.onclick = function() {
          af.style.display= 'block';//块标签修改属性
      	img.src=''//图片标签 修改路径
      		input.type=''表单标签修改
         }
```

- 通过classname 修改属性  会覆盖原来的类名 如果要保留原来的类要 " cs   cd"这种形式

  ```js
  <style>
    .cd{
        background-color: hotpink;
        width: 500px;
        height: 200px;
    }
    .cs{
        background-color: indigo;
        width: 200px;
        height: 200px;
    }
    .cf{
        background-color: lawngreen;
        width: 400px;
        height: 100px;
    }
  </style>
  <body>
       <div class="cd" id="ad">
           <div class="cs" id="as"></div>
       </div>
  </body>
  <script>
      var av = document.querySelectorAll('div');
      av[0].onclick = function(){
          av[1].className = 'cf';//不用加 .
      }
  
  </script>
  ```

  

**创建ajax过程**

(1)创建XMLHttpRequest对象,也就是创建一个异步调用对象.

(2)创建一个新的HTTP请求,并指定该HTTP请求的方法、URL及验证信息.

(3)设置响应HTTP请求状态变化的函数.

(4)发送HTTP请求.

(5)获取异步调用返回的数据.

(6)使用JavaScript和DOM实现局部刷新.



箭头函数（操作符左边为输入的参数，而右边则是进行的操作以及返回的值Inputs=>outputs。）、for-of（用来遍历数据—例如数组中的值。）

- static   静态 
- relative   相对   相对于原始位置  原始占有位置仍然保留
- absoult   绝对   父级元素有定位以父级元素为标准移动  没有就以网页为准  不保留位置 
- fixed   固定 不占位置  不随滚动条滚动
- 水平居中  left：50% margin  ：-自己宽度一半 

\+ beforeCreate：实例刚在内存中被创建出来，此时，还没有初始化好 data 和 methods 属性
    \+ created：实例已经在内存中创建OK，此时 data 和 methods 已经创建OK，此时还没有开始 编译模板
    \+ beforeMount：此时已经完成了模板的编译，但是还没有挂载到页面中
    \+ mounted：此时，已经将编译好的模板，挂载到了页面指定的容器中显示
 \- 运行期间的生命周期函数：
   \+ beforeUpdate：状态更新之前执行此函数， 此时 data 中的状态值是最新的，但是界面上显示的 数据还是旧的，因为此时还没有开始重新渲染DOM节点
   \+ updated：实例更新完毕之后调用此函数，此时 data 中的状态值 和 界面上显示的数据，都已经完成了更新，界面已经被重新渲染好了！
 \- 销毁期间的生命周期函数：
   \+ beforeDestroy：实例销毁之前调用。在这一步，实例仍然完全可用。
   \+ destroyed：Vue 实例销毁后调用。调用后，Vue 实例指示的所有东西都会解绑定，所有的事件监听器会被移除，所有的子实例也会被销毁。


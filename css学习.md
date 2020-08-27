# css学习

###### 引入css样式  开发时给body定义一个字体样式

- 采用<style>标签 在<head></head>内定义
- 内部 style=“  “
- 采用<link>标签 进行外部链接 （常用）

##### css选择器

- 根据标签 直接全选  h1{    }

- 类选择器  给标签加上class属性  class=”ak   sd“  一个class内可以放多个 选择器     .ak{ coler = blue;  }

  可以给多个标签同时调用

- id选择器  给标签加上id 属性  id= ‘’ pink ‘’   #pink{   }   id是唯一的  只能使用一个标签调用

- 通配符选择器   *选择所有标签     *{   } 降低页面响应速度 不建议随便使用

##### 字体

- font-size  字体大小 10px
- font-famil  字体样式  多个字体 依次寻找 { font-famil ：Arial，“Microsoft Yahei","微软雅黑”；}
- font-weight 字体粗细  400=normal正常   700=bold加粗 100-900整百
- font-style 字体风格 倾斜 
- 综合写法 {  font  ：font-style   font-weight    font-size    font-famil}后两个不能省略

##### css外观

- color 文本颜色
- line-height 行间距
- text-align 文本对齐方式
- text-index  首行缩进
- text- decoration  文本装饰   none 无   underline 下划线  

##### 复合选择器

-  后代选择器   包括子元素和孙子元素等  选中容器中的某一个或一类标签  .nav  a   {  }
- 子元素选择器   只选子元素  div>p{   }    .nav>p{  }
- 交集选择器   同时满足两个条件   p.red{   }  既是p标签又是class=red的标签 不带空格
- 并集选择器    同时满足多个标签  p, div,.red{   }   集体声明

##### 伪类选择器

-    a:link{ 未访问}  a:visited{已访问}  a:hover{  鼠标经过}   a:active{选定的链接}为某些选择器添加特殊效果  按照顺序来

#####  标签显示模式

1. ######  块级元素

   - 大部分竖向排列的标签  h,div,p,
   - 高 宽  内外边距可定义  默认继承父级宽
   - 独占一行
   - 里面可以放块级和行内元素   文字块内不要放块级元素

2. ###### 行内元素

   - 一行放多个  
   - 高宽直接设置无效，宽高和内容相关
   - 不能放块级元素 

#####  行内块元素  img  input  td 

- 可以设置高宽和对齐等属性   
- 一行可以放多个

#####  标签模式转换

- display:  inline  块级转换为行内
- display  :  block   行内转换为块级

#####  行高  实现文本垂直居中

- 行高=  上距离 +内容宽度+下距离
- 行高 = 盒子高度 文字垂直居中  大于 偏下     小于  偏上

#####  背景

- position  定位  background-position :  center (x坐标) top (y坐标) ; 以左上角为起点 
- background-attachment: fixed;   背景固定
- 简写  background : 背景颜色  背景图片  背景平铺   背景滚动  背景位置

#####   盒子模型

- padding  内边距 上  右    下 左 顺时针  
- 清除元素的内外边距   .{  padding: 0; margin : 0 ;}
- 塌陷问题 解决    给父元素定义上边框 透明 border-top: 1px solid transparent;    父元素添加 overflow ： hidden
- margin  相对于原始位置

#####  浮动  盒子水平显示

- float  浮在标准流上方 不占位置
- 浮动后类似于行内块级元素  
- 浮动后会在一行内显示并且是在顶端对齐，就是元素上边缘对齐

#####  定位   盒子层级显示    子绝父相 position=

- static   静态 
- relative   相对   相对于原始位置  原始占有位置仍然保留
- absoult   绝对   父级元素有定位以父级元素为标准移动  没有就以网页为准  不保留位置 
- fixed   固定 不占位置  不随滚动条滚动
- 水平居中  left：50% margin  ：-自己宽度一半 
- z-index :1 用来在盒子重叠时提升z轴显示级



#####  块级元素水平居中

- 块级元素有宽度的话 margin ：0 auto；
- 行内块元素 父元素添加  text-alagin ：center
- 绝对定位 left：50% ，margin-left：-半个元素宽

##### 垂直居中 #####

- 行高=高度
- vertical-align：middle
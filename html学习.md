#  html学习

### **标签**

 - div标签直接占一行
 - 一行可以多个span标签
 - p  段落标签
 -  hx 标题标签
 -  hr 下划线 单表签
 -  b 加粗  i 倾斜 s 删除线 u 下划线
 -  br 换行标签  单表签
 -  pre 预格式文本 不改变文字格式
 -  空格  &nbsp
### **图像标签属性 img 单标签**
 - alt 文本图像不能显示时的文本
 - title 文本  鼠标悬停时的内容
 - width  height 宽度高度
 - border 数字 图像边框宽度
### **链接标签属性  a**
-base 标签可以确定所有网页链接的打开方式 base target= '_blank' 写在head和head之间
 - herf 路径 外部链接加http 空链接 #
 - target 打开方式 self 此页打开 blank 新建标签页

  ### **相对路径**
 - 同一级 直接输入地址 a.jpg
 - 下一级 img/a.jpg
 - 上一级 ../a.jpg 两级 ../../a.jpg
### **锚点定位**

-给标签加上id 通过herf #id跳转

### **表格标签 展示数据 table**

 - tr 定义表格的行 在table中
 - th 表头 的行会加粗居中内容
 - captio 表格标题 紧跟table标签
 - td 定义单元格 在tr中
 - cellspacing 单元格与边框之间的空白间距
 - align 表格在网页中的对齐方式 左、中、右
 - 表格也可以划分为thead tbody和tfoot

  #### **表格合并**
- 跨行合并：rowspan='合并单元格个数'
- 跨列合并：colspan='合并单元格个数'
### **列表标签**
#### **无序列表** ul
- li 内部列表项 内部什么都可以放是一个容器

### **表单标签**

- form   表单域 多有标签都要在form中
- action url地址   methhod 提交方式 取值为get/post name 表单名称
- input 单标签  type不同属性对应不同文本框 text文本输入框 password密码框 radio 单选按钮checkbox复选框  btton 普通按钮   submit提交按钮reset重置按钮   image图像提交按钮   file 文件域   value默认值 name 区分框的类型后台提交数据使用

- lable 标签 包含input点击文字可以选中输入框

- textarea  文本域      cols=‘每行中的字符数’    rows = ‘显示的行数’
- select    下拉选择   option 为选项


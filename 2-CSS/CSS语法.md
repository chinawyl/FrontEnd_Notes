# 一、CSS概述

### 1.CSS简介

**层叠样式表**(英文全称：Cascading Style Sheets)，能够对网页中元素位置的排版进行像素级精确控制，支持几乎所有的字体字号样式，拥有对网页对象和模型样式编辑的能力。

### 2.CSS代码规范

```css
p {
    color: red;
    font-size: 20px;
}
```

- 标签和属性后面需要空格
- 各属性后面需用分号分隔

### 3.CSS选择器

##### 3.1 标签选择器

```css
标签名 {
    属性1: 属性值1;
}

p {
    color: red;
    font-size: 20px;
}
```

- 属性值前面，冒号后面，保留一个空格
- 标签名和大括号中间保留空格

##### 3.2 类选择器

`css`

```css
.类名 {
    属性1: 属性值1;
    .....
}

.red {
    color: red;
}
```

`html`

```html
<div class='red'>  变红色 </div>
```

- 类选择器在HTML中以 class 属性表示，在CSS中，类选择器以一个点`.`号表示

##### 3.3 类选择器多类名

```css
<style>
        .box {
            width: 100px;
            height: 100px;
        }

        .red {
            background-color: red;
        }

        .green {
            background-color: green;
        }
</style>
```

`html`

```html
<body>
    <div class="red box">红色</div>
    <div class="green box">绿色</div>
    <div class="red box">红色</div>
</body>
```

- 可以把一些标签元素相同的样式(公共的部分)放到一个类里面

- 这些标签都可以调用这个公共的类，然后再调用自己独有的类

- 从而节省CSS代码，统一修改也方便

##### 3.4 id选择器

`css`

```css
<style>
        #lin {
            color:pink;
        }
</style>
```

`html`

```html
<body>
    <div id="lin">霖</div>
</body>
```

- id 属性只能在每个 HTML 文档中出现一次。
- 样式 **#** 定义，结构 **id** 调用，只能调用一次。

##### 3.5 类选择器和id选择器区别

- 类选择器（class）好比人的名字，一个人可以有多个名字，同时一个名字也可以被多个人使用
- id 选择器好比人的身份证号码，全中国是唯一的，不得重复
- id 选择器和类选择器最大的不同在于使用次数上
- 类选择器在修改样式中用的最多，id 选择器一般用于页面唯一性的元素上，经常和 JavaScript 搭配使用

##### 3.6 通配符选择器

```css
* {
    属性1：属性值1;
    ....
}

/*一般是用于清楚元素标签的内外边距*/
* {
    margin: 0;
    padding: 0;
}
```

##### 3.7 CSS选择器总结

|  基础选择器  |          作用           |                 特点                  |    使用情况    |      语法       |
| :----------: | :---------------------: | :-----------------------------------: | :------------: | :-------------: |
|  标签选择器  | 可以选出所有相同的标签  |            不能差异化选择             |      较多      | p {color: red}  |
|   类选择器   | 可以选出1个或者多个标签 |           可以根据需求选择            |     非常多     | .p {color: red} |
|  id 选择器   |   一次只能选择1个标签   | ID 属性只能在每个 HTML 文档中出现一次 | 一般和 js 搭配 | #p {color: red} |
| 通配符选择器 |     选择所有的标签      |       选择的太多，有部分不需要        |  特殊情况使用  | * {color: red}  |

### 4.CSS字体属性

##### 4.1 font-family

```css
body {
    font-family: "Microsoft Yahe",tahoma,arial,"Hiragino Sans GB";
}
```

- 各种字体之间必须使用英文状态下的逗号隔开
- 一般情况下，如果有空格隔开的多个单词组成的字体，加引号
- 建议用英文而不是中文表达字体

##### 4.2 font-size

```css
p{
    font-size: 20px;
}
```

- 谷歌浏览器默认的文字大小为 16px

##### 4.3 font-weight

| **属性值** |                          **描述**                          |
| :--------: | :--------------------------------------------------------: |
|   normal   |           默认值(不加粗的)，相当于**number=400**           |
|    bold    |           定义粗体(加粗的)，相当于**number=700**           |
|   bolder   |                         定义特粗体                         |
|  100-900   | 400等同于 normal，700等同于 bold，注意这个数字后面不跟单位 |

- CSS使用font-weight属性设置字体的粗细
- 实际开发中，一般用**数字表示粗细**

##### 4.4 font-style

| **属性值** |              **描述**              |
| :--------: | :--------------------------------: |
|   normal   | 默认值，浏览器会显示标准的字体样式 |
|   italic   |   浏览器会显示**斜体**的字体样式   |

- CSS使用font-style属性设置文字样式

##### 4.5 字体属性复合写法

`一般写法`

```css
<style>
        /*div标签 文字倾斜 文字加粗 字号16像素 微软雅黑*/
		/* 顺序：font-style font-weight  font-size/line-height  font-family */        

        div {
            font-style: italic;
            font-weight: 700;
            font-size: 16px;
            font-family: 'Microsoft yahe';
        }
</style>
```

`简单写法`

```css
<style>
		div {
            font: italic 700 16px 'Microsoft yahe';
        }
</style>
```

- 使用font属性时，必须按照语法格式顺序书写，**不能更换顺序**，并且各个属性间**以空格**隔开
- 不需要设置的属性可以省略(取默认值)，但必须保留`font-size` 和`font-family`属性，否则 font 属性将不起作用

##### 4.6 CSS字体属性总结

|    属性     |   表示   |                            注意点                            |
| :---------: | :------: | :----------------------------------------------------------: |
| font-style  | 字体样式 |  记住倾斜是 italic，不倾斜是 normal，实际开发最常用 normal   |
| font-weight | 字体粗细 | 加粗是 700 或者 bold ，不加粗是 normal 或者 400，记住数字不加单位 |
|  font-size  |   字号   |            我们通常用的单位是 px ，一定要跟上单位            |
| font-family |   字体   |                实际工作中按照团队约定来写字体                |
|    font     | 字体连写 | ①字体连写是有顺序的，不能随意换位置 ② **字体和字号必须同时出现** |

### 5.CSS文本属性

##### 5.1 color

```css
div {
    color: red;
}
```

- 用于定义文本的颜色

|      表示      |                属性值                |
| :------------: | :----------------------------------: |
| 预定义的颜色值 |       red，green，blue，pink等       |
|    十六进制    |      #FF0000, #FF6600，#29D794       |
|    RGB代码     | rgb（255，0，0） 或rgb(100%，0%，0%) |

##### 5.2 text-align

```css
div {
    text-align:center;
}
```

- 用于设置文本内容的水平对齐方式

| 属性值 |      解释      |
| :----: | :------------: |
|  left  | 左对齐（默认） |
| right  |     右对齐     |
| center |    居中对齐    |

##### 5.3 text-decoration

```css
div {
    text-decoration: underline;
}
```

- 用于装饰文本，可以给文本添加下划线，删除线，上划线等

|    属性值    |              描述              |
| :----------: | :----------------------------: |
|     none     |    默认。没有装饰线(最常用)    |
|  underline   | 下划线，链接自带下划线（常用） |
|   overline   |        上划线(几乎不用)        |
| line-through |        删除线 (不常用)         |

##### 5.4 text-indent

```css
div {
    text-indent: 32px;
}

p{
   text-indent: 2em;
}
```

- 用于指定文本的第一行缩进，通常是将段落的首行缩进
- 通过设置该属性，所有元素的第一行都可以缩进一个给定的长度，如果设置负值会导致部分文字被遮挡
- em是一个相对单位，就是当前元素(font-size)**1个文字的大小**，默认一个文字大小16px
- 如果当前元素没有设置大小，则会按照父元素的一个文字大小

##### 5.5 line-height

```css
p {
   line-height: 26px;
}
```

- 用于设置行间的距离(行高)，可以控制文字行与行之间的距离

![001-行高](./images/001-行高.png)

##### 5.6 CSS文本属性总结

|      属性       |   表示   |                  注意点                  |
| :-------------: | :------: | :--------------------------------------: |
|      color      | 文本颜色 |    通常用十六进制，而且是简写形式 #FF    |
|   text-align    | 文本对齐 |        可以设定文字水平的对齐方式        |
|   text-indent   | 文本缩进 |               段落首行缩进               |
| text-decoration | 文本修饰 | 记住添加下划线 underline 取消下划线 none |
|   line-height   |   行高   |           控制行与行之间的距离           |

### 6.CSS样式表引入方式

##### 1.内部样式表

```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box {
            width: 100px;
            height: 100px;
        }

        .red {
            background-color: red;
        }

        .green {
            background-color: green;
        }
    </style>
</head>
```

- 通常在head标签里面，将样式写在<style>标签里

##### 2.行内样式表

```html
<div style="color: red; font-size: 20px;"></div>
```

- 在元素标签的内部的style属性中设定

##### 3.外部样式表

```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="#">
</head>
```

- 最常用，且可控制多个页面
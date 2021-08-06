# 一、HTML概述

### 1.生成骨架快捷键

```txt
输入!按下tab
```

### 2.骨架标签解释

`<!DOCTYPE html>（文档类型）`

- 用来说明你用的XHTML或者HTML是什么版本
- 告诉浏览器按照HTML5标准解析页面

`<html lang="en">（页面语言）`

- 指定该html标签内容所用的语言
- en 定义语言为英语，zh-CN定义语言为中文

`<meta charset="UTF-8">（字符集）`

- 是多个字符的集合,以便计算机能够识别和存储各种文字
- 让 html 文件是以 UTF-8 编码保存的，浏览器根据编码去解码对应的html内容

<br/>

# 二、标签

### 1.排版标签

- 标题标签h(h1~h6)

- 段落标签p

- 换行标签br

```txt
在 HTML 中，<br> 标签没有结束标签。

在 XHTML 中，<br> 标签必须被正确地关闭，比如这样：<br />
```

### 2.文本格式化标签

| 语义   | 标签                       | 说明                                    |
| ------ | -------------------------- | --------------------------------------- |
| 加粗   | <strong></strong>或<b></b> | 更推荐使用<strong>标签加粗，语义更强烈  |
| 倾斜   | <em></em>或<i></i>         | 更推荐使用<em>标签倾斜，语义更强烈      |
| 删除线 | <del></del>或<s></s>       | 更推荐使用<del>标签做删除线，语义更强烈 |
| 下划线 | <ins></ins>或<u></u>       | 更推荐使用<ins>标签做下划线，语义更强烈 |

### 3.布局标签

##### 3.1 div标签

```txt
div标签一行只能放一个，大盒子
```

##### 3.2 span标签

```txt
span标签一行可以放多个，小盒子
```

### 4.图像标签和文件路径

##### 4.1 图像标签

| 属性   | 属性值   | 说明                                 |
| ------ | -------- | ------------------------------------ |
| src    | 图片路径 | 必须属性                             |
| alt    | 文本     | 替换文本。图像不能显示的文字         |
| title  | 文本     | 提示文本。鼠标放在图像上，显示的文字 |
| width  | 像素     | 设置图像的宽度                       |
| height | 像素     | 设置图像的长高度                     |
| border | 像素     | 设置图像的边框粗细                   |

##### 4.2 文件路径

`相对路径`

| 相对路径分类 | 符号 | 说明                                               |
| ------------ | ---- | -------------------------------------------------- |
| 同一级路径   |      | 图像文件位于HTML文件同一级，如：test.img           |
| 下一级路径   | /    | 图像文件位于HTML文件下一级，如：imsges/test.img    |
| 上一级路径   | ../  | 图像文件位于HTML文件上一级，如：../images/test.img |

`绝对路径`

```txt
电脑本地路径 D:\web\images\test.img

或

完整的网络地址 https://img0.baidu.com/it/u=1669469152.jpg 
```

**注：电脑本地绝对路径通配符与相对路径通配符是相反的**

### 5.链接标签

##### 5.1 链接属性

| 属性 | 作用                                  |
| ---- | ------------------------------------- |
| href | 用于指定链接目标的url地址（必要属性） |

<br/>

| 属性   | 参数        | 作用                               |
| ------ | ----------- | ---------------------------------- |
| target |             |                                    |
|        | _self       | 默认。在相同的框架中打开被链接文档 |
|        | _blank      | 在新窗口中打开被链接文档。         |
|        | _parent     | 在父框架集中打开被链接文档         |
|        | _top        | 在整个窗口中打开被链接文档         |
|        | *framename* | 在指定的框架中打开被链接文档       |

##### 5.2 链接分类

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>超链接标签</title>
</head>
<body>
    <h4>1.外部链接</h4>
    <a href="http://www.qq.com" target="_blank"> 腾讯</a>
    target 打开窗口的方式  默认的值是 _self 当前窗口打开页面  _blank 新窗口打开页面
    <a href="http://www.itcast.cn" target="_blank">传智播客</a>
    
    <h4>2.内部链接: 网站内部页面之间的相互链接</h4>
    <a href="gongsijianjie.html" target="_blank">公司简介</a>
    
    <h4>3.空链接:#</h4>
    <a href="#">公司地址</a>
    
    <h4>4.下载链接: 地址链接的是文件.exe或者是.zip等压缩包形式</h4>
    <a href="img.zip">下载文件</a>
    
    <h4>5.网页元素的链接</h4>
    <a href="http://www.baidu.com"><img src="img.jpg"/></a>
    
    <h6>6.锚点链接</h6>
    1 早年经历<br />
    2 演艺经历<br />
    3 个人生活<br />
    4 <a href="#zuopin">主要作品</a><br />
    5 社会活动<br />
    6 获奖记录<br />
    7 人物评价<br />
    
    <h3 id="zuopin">主要作品</h3>

    参演电影

    侠盗联盟2017-07
    导演冯德伦 主演让-雷诺, 舒淇

    拆弹专家2017
    饰演拆弹专家 导演邱礼涛 主演姜武, 小宋佳,
    黄宗泽
</body>
</html>
```

### 6.注释标签和特殊字符

##### 6.1 注释标签

```html
<!-- 我是sb -->
```

##### 6.2 特殊字符

| HTML 原代码 | 显示结果 | 描述                   |
| ----------- | -------- | ---------------------- |
| \&lt;       | <        | 小于号或显示标记       |
| &gt;        | >        | 大于号或显示标记       |
| &amp;       | &        | 可用于显示其它特殊字符 |
| &quot;      | “        | 引号                   |
| &reg;       | ®        | 已注册                 |
| &copy;      | ©        | 版权                   |
| &trade;     | ™        | 商标                   |
| \&ensp;     |          | 半个空白位             |
| \&emsp;     |          | 一个空白位             |
| \&nbsp;     |          | 不断行的空白           |

### 7.综合案例一

完成如页面所示效果（**代码----->终合案例一**）

### 8.表格标签

##### 8.1 表格基本用法

```html
<table>
    
    <tr>
        <td>单元格内文字</td>
    </tr>
</table>
```

- table标签用于定义表格标签
- tr标签表示表格的行，必须嵌套在table标签中
- td标签表示表格的单元格，必须嵌套在tr标签中
- 表格数据必须放在td标签中

##### 8.2 表头单元格标签

```html
<table>
    <tr>
        <td>单元格内文字</td>
    </tr>
</table>
```

- th标签是**table head**缩写
- th标签会让单元格内容加粗居中显示

##### 8.3 表格属性(实际不常用)

| **属性名**  | **含义**                                 | **常用属性值**                                        |
| ----------- | ---------------------------------------- | ----------------------------------------------------- |
| border      | 设置表格的边框宽度                       | 像素值(默认为0)                                       |
| cellspacing | 设置单元格与单元格边框之间的空白间距宽度 | 像素值(默认为2像素)                                   |
| cellpadding | 设置单元格内容与边框线之间的空白间距宽度 | 像素值(默认为1像素)                                   |
| width       | 设置表格的宽度                           | 像素值                                                |
| height      | 设置表格的高度                           | 像素值                                                |
| align       | 设置表格在网页中的水平对齐方式           | left、center、right                                   |
| bgcolor     | 设置表格的整体背景颜色                   | HTML5 不支持。HTML 4.01 已废弃。 规定表格的背景颜色。 |

```html
<table border="1" cellspacing= "3" cellpadding="5" align="center">
    <th>表头1</th>
    <th>表头2</th>
    <th>表头3</th>
    <th>表头4</th>
    <tr>
        <td>单元格内文字</td>
        <td>单元格内文字</td>
        <td>单元格内文字</td>
        <td>单元格内文字</td>
    </tr>
    <tr>
        <td>单元格内文字</td>
        <td>单元格内文字</td>
        <td>单元格内文字</td>
        <td>单元格内文字</td>
    </tr>
    <tr>
        <td>单元格内文字</td>
        <td>单元格内文字</td>
        <td>单元格内文字</td>
        <td>单元格内文字</td>
    </tr>
</table>
```

##### 8.4 表格案例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table border="1" cellspacing= "0" cellpadding="0" align="center">
        <th>排名</th>
        <th>关键词</th>
        <th>趋势</th>
        <th>今日搜索</th>
        <th>最近七日</th>
        <th>相关链接</th>
        <tr>
            <td>1</td>
            <td>鬼吹灯</td>
            <td><img src="down.jpg"></td>
            <td>345</td>
            <td>123</td>
            <td>
                <a href="#">贴吧</a>
                <a href="#">图片</a>
                <a href="#">百科</a>
            </td>
        </tr>
        <tr>
            <td>2</td>
            <td>三国演义</td>
            <td><img src="up.jpg"></td>
            <td>124</td>
            <td>145444</td>
            <td>
                <a href="#">贴吧</a>
                <a href="#">图片</a>
                <a href="#">百科</a>
            </td>
        </tr>
    </table>
</body>
</html>
```

##### 8.5 表格结构标签

```html
<body>
    <table>
        <thead>
            <th></th>
            <tr>
                <td></td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td></td>
            </tr>
        </tbody>
    </table>
</body>
```

- thead标签用于定义表格头部，必须包含**tr**标签
- tbody标签用于定义表格主体

##### 8.6 合并单元格

`合并单元格方式`

- 跨行合并：rowspan="合并单元格的个数"
- 跨列合并：colspan="合并单元格的个数"

`合并单元格步骤`

- 确定合并方式
- 找到目标单元格（合并的**最左**或**最上**单元格），写上合并方式 = 合并单元格数量。例如：

```html
<td colspan="2"></td>
```

- 删除多余单元格

```html
<table width="500" height="249" border="1" cellspacing="0">
    <tr>
        <td></td>
        <td colspan="2"></td>
    </tr>
    <tr>
        <td rowspan="2"></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
    </tr>
</table>
```

### 9.列表标签

##### 9.1 无序列表

```html
<ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
</ul>
```

- 无序列表的各个列表是没有顺序级别之分，是并列的
- ul标签中只能嵌套li标签，直接在ul标签中输入其他标签或者文字的做法是不被允许的
- li标签之间相当于一个容器，可以容纳所有元素
- 无序列表有自带样式属性，但一般都使用CSS控制

##### 9.2 有序列表(实际不常用)

```html
<ol>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
</ol>
```

- 有序列表为有排列顺序的列表
- ol标签中只能嵌套li标签，直接在ol标签中输入其他标签或者文字的做法是不被允许的
- li标签之间相当于一个容器，可以容纳所有元素
- 有序列表有自带样式属性，但一般都使用CSS控制

##### 9.3 自定义列表

```html
<dl>
    <dt>关注我们</dt>
    <dd>新浪微博</dd>
    <dd>官方微信</dd>
    <dd>联系我们</dd>

    <dt>关注我们</dt>
    <dd>新浪微博</dd>
    <dd>官方微信</dd>
    <dd>联系我们</dd>
</dl>
```

- dl标签只能包含dt标签和dd标签
- dt标签和dd标签没有个数限制，通常是一个dt标签对应多个dd标签
- dt标签和dd标签里面可以放任何标签

# 三、表单标签

在HTML中，一个完整的表单通常由**表单域**、**表单控件**、**提示信息**3个部分构成。表单目的是为了收集用户信息

### 1.表单域

它相当于一个容器，用来容纳所有的表单控件和提示信息，可以通过他定义处理表单数据所用程序的url地址，以及数据提交到服务器的方法。如果不定义表单域，表单中的数据就无法传送到后台服务器 

```html
<form action="url地址" method="提交方式" name="表单域名称">
    各种表单元素控件
</form>
```

### 2.表单控件

##### 2.1 input标签的type属性

| 属性值   | 描述                   |
| -------- | ---------------------- |
| text     | 文本框                 |
| password | 密码框                 |
| radio    | 单选按钮               |
| checkbox | 复选框                 |
| submit   | 提交按钮               |
| reset    | 重置按钮               |
| button   | 可点击按钮             |
| file     | 定义文件浏览和上传按钮 |
| image    | 定义图像形式的提交按钮 |
| hidden   | 定义隐藏的输入字段     |

##### 2.2 input标签其他属性

| 属性      | 属性值       | 描述                              |
| --------- | ------------ | --------------------------------- |
| name      | 由用户自定义 | 定义input元素名称                 |
| value     | 由用户自定义 | 定义input元素的值                 |
| checked   | checked      | 规定此input元素首次加载是否被选中 |
| maxlength | 正整数       | 规定输入字段中的最大长度          |

- name和value值供后台人员使用
- 单选按钮和复选框按钮要有相同的name值
- checked主要针对单选按钮和复选框按钮，只要作用为一打开页面就有默认值
- maxlength一般用于限制表格最大字符数，用的少

##### 2.3 实例

```html
<form action="url地址" method="提交方式" name="表单域名称">
        用户名:<input type="text" value="请输入用户名"><br>
    
        密  码:<input type="password" maxlength="16"><br>
    
        性  别:男 <input type="radio" name="sex" value="男">
    	女:<input type="radio" name="sex" value="女">
    	未知:<input type="radio" name="sex" value="未知"><br>
    
        爱  好:吃饭 <input type="checkbox" name="hobby" checked="checked" value="吃饭">
        睡觉 <input type="checkbox" name="hobby" value="睡觉">
        撸管 <input type="checkbox" name="hobby" value="撸管"><br>
    
        <input type="submit" value="注册">&nbsp;&nbsp;
    	<input type="reset" value="重置">&nbsp;&nbsp;
    	<input type="button" value="获取验证码"><br>
    
        上传文件:<input type="file">上传头像:<input type="image">
    </form>
```

##### 2.4 lebel标签

用于绑定一个表单元素, 当点击label标签的时候, 被绑定的表单元素就会**获得输入焦点**

```html
<label for="username">用户名:<input type="text" id="username"></label>
```

- label标签的for属性值要与相关元素的id属性值相同

##### 2.5 select下拉标签

```html
<form>
    籍贯: 
    <select>
        <option>山东</option>
        <option>北京</option>
        <option>天津</option>
        <option selected="selected">未知</option>
    </select>
</form>
```

- select标签中至少有一对option标签
- selected="selected"为默认选项

##### 2.6 textarea文本域控件标签 

```html
<form>
    今日反馈:
    <textarea cols="50" rows="5">pink老师,我知道这个反馈留言是textarea来做的 </textarea>
</form>
```

- 通过textarea控件可以轻松地创建多行文本输入框.
- cols="每行中的字符数" rows="显示的行数"  我们实际开发不用
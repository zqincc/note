<center>CSS：层叠样式表（Cascading style sheets）</center>

​	CSS is written in style, style is included by head tag,then head tag include title tag.

such as:

CSS note: /**/

# 1 css import mode

​	where is the CSS written in?

css code: no have any format, only is selector and {}.

```
p {

}
```

## 1.1 Embedded type（内嵌式）

​	CSS is written in the style tag.

tips: Although style tag can write anywhere on the pages, style  tag usually is written in head tag.

```
<head>
	<title>D</title>
	<style>
		p {
			/*css note*/
			/*All content of css*/
			/*selector*/
			/*find the tag in HTML.*/
			/*such as*/
			color: red;
			font-size: 30px;// font-size字体大小
			backgroud-color:green;
			/*width and height*/
			width:400px;
			height:400px;
		}
	</style>
</head>
```

## 1.2 External embedding type（外嵌式）

​	CSS is written in a .css fine alone.

tigs: this import mode need a link tag in web.

```
<head>
	<title>Document</title>
	<link rel="stylesheet" href="./xxx.css">
</head>
```

## 1.3 in-link type（行内式）

​	CSS is written in the style attribute of the tag.

tips: this mode will cooperate JavaScript.

```
<body>
	<div style="">this is a div tag</div>
</body>
```

# 2 base selector

## 2.1 tag selector（标签选择器）

​	Select all have the tag.

fomat: tag name {CSS attribute name: attribute value;}

useful: by tag name, find all tag of this class, the set style.

```
<html>
    <head>
    	<title>Document</title>
    	<style>
    		p {
    		/*All tag come into effect.*/
    		}
    	</style>
    </head>
    <body>
    	<p>This is test.</p>
    </body>
</html>
```

## 2.2 class selector（类选择器）

​	who use selcet who.

format: .class name {CSS attribute name: attribute value;}

useful: by class name, find all included class name of tag on the pages.

```
<html>
    <head>
    	<title>Document</title>
    	<style>
    		.Test {
    		/*Use the class will come into effect.*/
    			color: red;
    		}
    	</style>
    </head>
    <body>
    	<p class="Test">This is test.</p>
    </body>
</html>
```

## 2.3 id selector（id 选择器）

format: #id atrribute value {class attribute: attribute vlaue;}

tigs: id select in order to cooperate in JavaScript in the future.

```
<html>
    <head>
    	<title>Document</title>
    	<style>
    		#Test {
    		/*Use the id will come into effect.*/
    			color: red;
    		}
    	</style>
    </head>
    <body>
    	<p id="Test">This is test.</p>
    </body>
</html>
```

## 2.4 wildcard select（通配符选择器）

format: *{CSS attribute name: attribute value;}

```
<html>
    <head>
    	<title>Document</title>
    	<style>
    		* {
    		/*All tag will come into effect.*/
    			color: red;
    		}
    	</style>
    </head>
    <body>
    	<p>p tag</p>
    	<div>div tag</div>
    	<span>span tag</span>
    </body>
</html>
```

# 3 font style

## 3.1 font style:

<table border="2">
    <thead>
        <tr>
            <th>style</th>
            <th>attribute name</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>字体大小</td>
            <td>font</td>
        </tr>
        <tr>
            <td>字体粗细</td>
            <td>font-weight</td>
        </tr>
        <tr>
            <td>字体样式</td>
            <td>font-style</td>
        </tr>
        <tr>
            <td>字体类型</td>
            <td>font-family</td>
        </tr>
        <tr>
            <td>字体类型</td>
            <td>font属性连写</td>
        </tr>
    </tbody>
</table>

## 3.2 font-size:

​	attribute value: digit + px;

​	default value: 16px

## 3.3 font-weight:

​	attribute value:

​		key word:

| 正常 | normal |
| ---- | ------ |
| 加粗 | bold   |

​		digit: 100-900 （整百）

| 正常 | 400  |
| ---- | ---- |
| 加粗 | 700  |

## 3.4 font-style：	

| 正常 | normal(default value) |
| ---- | --------------------- |
| 倾斜 | italic                |

## 3.5 font-family:

| system  | default font-family |
| ------- | ------------------- |
| wimdows | 微软雅黑            |
| macOS   | 苹方                |

```
div {
	/*sans-serif:*/
	/*If user's PC doesn't have YaHei, font-family will use HeiTi.*/
	/*If this is't any font-family in user's PC, show any font-family.*/
	font-family:微软雅黑,黑体,sans-serif;
}
```

## 3.6 Problem

If a tag has the same style, CSS will come into effect in the end.

Such as:

```
p {
	color:red;
	color:blue;
}
```

This CSS will come into color blue.

## 3.7 font related attributes must be conjoined 

Format: font(compound attribute)

Attribute value:

​	style weight size family

Omission requirement:

​	You have to omit the first two. (This operation is equal to setting the default value.)

​	In addition, you can use the alone font style under font. 

```
/*font: style weight size family;*/
p {
	/*A font have many value, space off.*/
	font:italic 700 16px 宋体;
}
```

## 3.8 extend

Color value.

Attribute name: color and background-color.

Attribute value

| Color expression's way | Express meaning                         | Attribute value                        |
| ---------------------- | --------------------------------------- | -------------------------------------- |
| key word               | 预定义的颜色名                          | red、green、blue...                    |
| rgb expression         | 红蓝绿三原色，每项取值范围：0-255       | rgb(0,0,0)、rgb(255,255,255)           |
| rgba expression        | 红蓝绿三原色+a表示透明度，取值范围是0-1 | rgba(0,0,0,0.5)、rgba(255,255,255,0.3) |
| Hexadecimal notation   | #开头，将数字转换为十六进制             | #000000、#ff0000                       |

Tag horizental centering way: margin: 0 auto

```
div {
	margin: auto;
}
<div></div>
```



# 4 text style

<table border="2">
    <thead>
        <tr>
            <th>style</th>
            <th>attribute name</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>行高</td>
            <td>line-height</td>
        </tr>
    </tbody>
</table>

## 4.1 text-indent

Text indent attribute name: text-indent

attribute value:

​	digit + px

​	dight + em (Recommend, 1em = tag's font-size now)

```
p {
	text-indent: 50px;
	/*Usually indent 2 font*/
	/*em: a font-size*/
	text-indent: 2em;
}
```

## 4.2 text-align

| Attribute value | Effect      |
| --------------- | ----------- |
| left            | left align  |
| center          | center      |
| right           | right align |

Tigs: If you need to make the text horizontal centering, set text tag(The parent element of text).

```
p {
	text-align: center;
}
```

Horizontal centering ways(text-align: center)

Which element will Horizental centering?

Text, span tag, a tag, input tag and img tag.

Pay attention:

If you need to set above element horizental centering, you need to set the parent element (text-align: center). 

```
body {
	text-align: center;
}
<body>
	<img sre="./" alt="">
</body>
```

## 4.3 text-decoration

| Attribute value | Effct              |
| --------------- | ------------------ |
| underline       | 下划线（常用）     |
| line-through    | 删除线（不常用）   |
| overline        | 上划线（几乎不用） |
| none            | 无修饰线（常用）   |

## 4.4 line-height

Function: control a line up and down distance.

Attribute name: line-height

Attribute vaule:

​	digit + px

​	multiple (The mutiple of tag's font-size now)

Applycation: 

First, let alone line text vertical centering. line-height: height of font parent' element

Second, Web precise layout will set line-height.(It can cancel up and down distance.)

If set the height and font related attributes must be conjoined, note covers problem.

```
font: style wight size/line-height famuly.
```

# 5 Chrome Debugging tool 

summary: 2023/1/14 learning note.
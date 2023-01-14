<center>CSS：层叠样式表（Cascading style sheets）</center>

​	CSS is written in style, style is included by head tag,then head tag include title tag.

such as:

css note: /**/

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

fomat: tag name {CSS atrribute name: atrribute value;}

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

format: .class name {CSS atrribute name: atrribute value;}

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

format: #id atrribute value {class atrribute: atrribute vlaue;}

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

format: *{CSS atrribute name: atrribute value;}

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

# 3 font and text styles

font style:

<table border="2">
    <thead>
        <tr>
            <th>style</th>
            <th>atrribute name</th>
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

font-size:

​	atrribute value: digit + px;

​	default value: 16px

font-weight:

​	atrribute value:

​		key word:

| 正常 | normal |
| ---- | ------ |
| 加粗 | bold   |

​		digit: 100-900 （整百）

| 正常 | 400  |
| ---- | ---- |
| 加粗 | 700  |

font-style：	

| 正常 | normal(default value) |
| ---- | --------------------- |
| 倾斜 | italic                |

font-family:

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



text style:

<table border="2">
    <thead>
        <tr>
            <th>style</th>
            <th>atrribute name</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>行高</td>
            <td>line-height</td>
        </tr>
    </tbody>
</table>


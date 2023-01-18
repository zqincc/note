# 1 Advanced selector

## 1.1 offspring selector（后代选择器）

space

grammar: selector1 selector2 {CSS}

```
<head>
	<style>
		/*Find div's son to set font color.*/
		/*parent selector + space + child selector + {}*/
		div p {
			color: red;
		}
	</style>
</head>
<body>
	<p>p tag</p>
	<div>
		<p>div's son</p>
	</div>
</body>
```

## 1.2 child selector（子代选择器）

\>

grammar: selector1>selector2 {CSS}

```
div>a {
	color: red;
}
<div>
	/*parent*/
	/*CSS come into effect.*/
	<a>This is in div tag.</a>
	<p>
		/*This is't come into effect.*/
		<a>div tag include p tag, and p tag include a tag.</a>
	</p>
</div>
```

## 1.3 union set selector（并集选择器）

function: Selecting many tag at the time, set the same style.

selector grammar: selector1, selector2, ... {CSS}

```
<head>
	<style>
		p,
		div,
		span,
		h1 {
			color red;
		}
	</style>
</head>
<body>
	/*come into effect.*/
	<p>p tag</p>
	<div>div tag</div>
	<span>span tag</span>
	<h1>h1 tag</h1>
	
	/*Don't come into effect.*/
	<h2>h2</h2>
</body>
```

## 1.4 intersection selector（交集选择器）

Function：Selects tags on the page that satisfy more than one selector.

selecotr1selector2 {CSS}

```
<head>
	<style>
		p.box {
			color: red;
		}
	</style>
</head>
<body>
	<p class="box">p tag and box class, Come into effect.</p>
	<p>Only p tag, don't come into effect.</p>
	<div class="box">div tag and box class, don't come into effct.</div>
</body>
```

## 1.5 hover伪类选择器(hover pseudo-class selector)

Function: Selecting the status of the element above of the mouse, so that to set the style.

作用：选择鼠标悬停在元素上的状态，设置样式。

Selector grammar: selector:hover {CSS}

Warning: 伪类选择器选中的元素某种状态。

## 1.6 emment grammar

Function: By simply writing grammmar, quickly producing code.

| menmory               | example                   | result                               |
| --------------------- | ------------------------- | ------------------------------------ |
| tag name              | div                       | <div></div>                          |
| class selector        | .red                      | <div class="red"></div>              |
| id selector           | #one                      | <div id="one"></div>                 |
| intersection selector | p.red#one                 | <p class="red" id="one"></p>         |
| child selector        | ul>li                     | <ul><li></li></ul>                   |
| interior text         | ul>li{I'm content of li.} | <ul><li>I'm content of li.</li></ul> |
| create many           | ul>li*3                   | <ul><li></li><li></li><li></li><ul>  |


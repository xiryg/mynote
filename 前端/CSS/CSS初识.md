# CSS样式
css，专门用来“美化”标签。
## 在标签上
```html
<div style="color: bisque">冯唐易老，李广难封。</div>
```

## 在head标签里写style标签

```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <style> 
	  .c1{  
            color: red;  
         }  
    </style>  
</head>  
<body>  
    <div class="c1">豫章故郡，洪都新府。</div>  
</body>  
</html>
```

## 在css文件中写
```css
.c2{  
    color: #7719ae;  
}  
.c1{  
    height: 100px;  
}
```
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <link rel="stylesheet" href="2.css">  
</head>  
<body>  
    <div class="c1">豫章故郡，洪都新府。</div>  
    <div class="c2">星分翼轸，地接衡庐。</div>  
</body>  
</html>
```

## 选择器
- ID选择器
```css
#c1{  
    color: #7719ae;  
}
```
-  类选择器
```css
.c2{  
    color: #7719ae;  
}
```
- 标签选择器
```css
div{

}
<div>xxx</div>
```
- 属性选择器
```css
input[type="text"]{  
    border: 3px solid royalblue;  
}  
.v1[xx="123"]{  
    color: pink;  
}  
.v1[xx="456"]{  
    color: gold;  
}
```
```html
<div>  
    <label>  
        用户名：  
        <input type="text" name="user" />  
    </label>  
</div>  
<div class="v1" xx="123">兰亭已矣，梓泽丘墟。</div>  
<div class="v1" xx="456">穷且益坚，不坠青云之志。</div>  
<div class="v1" xx="789">东隅已逝，桑榆非晚。</div>
```
![](https://img.tucang.cc/api/image/show/909627cc98df26fa6df8ed2c1914e4a1)
- 后代选择器
```css
.x1 li{  
    color: pink;  
}  
.x1 > a{  
    color: brown;  
}
```
```html
<div class="x1">  
    <a>百度</a>  
    <div>        <a>谷歌</a>  
    </div>  
    <ul>        <li>茉莉</li>  
        <li>荼蘼</li>  
        <li>蔷薇</li>  
    </ul>  
</div>
```
`.x1 li` 找到属性`x1` 下的 `li` 标签，
`.x1 > a` 找到属性`x1` 下的`a` 标签 (儿子标签)。

![](https://img.tucang.cc/api/image/show/56e3687f832316132991676127dcebff)

## 关于选择器
>  多：类选择器、标签选择器、后代选择器
>  少：属性选择器、ID选择器

关于多个样式和覆盖问题：
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <style>        
        .c1{  
            color: red;  
            border: 1px solid red;  
        }  
        .c2{  
            font-size: 30px;  
            color: palevioletred;  
        }  
    </style>  
</head>  
<body>  
    <div class="c1 c2">中国移动</div>  
</body>  
</html>
```
`c1` 和 `c2` 都作用与 `中国联通` 
![](https://img.tucang.cc/api/image/show/6a762137b4d430937ca02329c26d401b)
前者，`c1` 和 `c2` 样式无重复的。、
![](https://img.tucang.cc/api/image/show/6a633436fa6e97fd4d0276089c605502)
后者，`c2` 有对颜色的样式，就覆盖了 `c1` 的颜色样式。
**注：跟c1 c2 的写的顺序无关，而是和在定义的时候，c1 和 c2 的顺序有关，c2 在 c1 后，c2 的样式会覆盖c1。**

`补充` ：如何不覆盖
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <style>        
        .c1{  
            color: red ! important;  
            border: 1px solid red;  
        }  
        .c2{  
            font-size: 30px;  
            color: palevioletred;  
        }  
    </style>  
</head>  
<body>  
    <div class="c1 c2">中国移动</div>  
</body>  
</html>
```
在样式后加 `! important` 表示很重要。

## 样式
### 1.高度和宽度
```css
.c1{  
    height: 300px;  
    width: 500px;  
}
```
`注意事项` ：
- 宽度：支持百分比。
- 行内标签：默认无效
- 块级标签：默认有效（右侧区域空白，也不给其他占用）
### 2.块级和行内标签
- 块级
- 行内
- css样式：`display: inline-block` 
示例：行内&块级特性
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <style>        .c3{  
            display: inline-block;  
            height: 100px;  
            width: 200px;  
            border: 1px solid red;  
        }  
    </style>  
</head>  
<body>  
    <span class="c3">中国移动</span>  
  
    <span class="c3">中国联通</span>  
  
    <span class="c3">中国电信</span>  
</body>  
</html>
```
![](https://img.tucang.cc/api/image/show/2de2f4ece45cafe3434ec2e619c352dc)
块级和行内的转换：
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
</head>  
<body>  
    <span style="display: block">中国</span>  
    <div style="display: inline">俄罗斯</div>  
</body>  
</html>
```
行内转块级：`style="display: block"`
块级转行内：`style="display: inline"`
### 3.字体设置
- 颜色：可用 `rgb` 
- 大小
- 加粗
- 字体
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <style>        .c1{  
            color: palevioletred;  
            font-size: 30px;  
            font-weight: 600;  
            font-family: "dejavu sans mono", serif;  
        }  
    </style>  
</head>  
<body>  
    <span class="c1">松风吹解带，山月照弹琴。</span>  
</body>  
</html>
```
![](https://img.tucang.cc/api/image/show/33491f9929ac5e9dbdb7e9460c16dcaa)
### 4.文字对齐方式
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <style>        
      .c1{  
            color: #393cb0;  
            height: 60px;  
            width: 300px;  
            font-family: "dejavu sans mono", serif;  
            border: 2px solid palevioletred;  
            text-align: center; /* 水平方向居中 */            line-height: 60px; /* 垂直方向居中 height = line-height*/  
         }  
    </style>  
</head>  
<body>  
    <div class="c1">天上星河转，人间帘幕垂。</div>  
</body>  
</html>
```
![](https://img.tucang.cc/api/image/show/87fbfa9176e8c3fe17593847b95cd2ba)

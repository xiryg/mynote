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


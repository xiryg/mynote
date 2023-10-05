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
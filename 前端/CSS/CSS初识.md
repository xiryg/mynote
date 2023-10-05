css，专门用来“美化”标签。
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
</head>  
<body>  
    <h1>用户注册</h1>  
    <form method="post" action="/post/reg">  
        <label>  
            用户名:  
            <input type="text" name="user"/>  
        </label>  
  
        <label>            密码:  
            <input type="password" name="pwd"/>  
        </label>  
        <label>            性别:  
            <input type="radio" name="gender" value="1">男  
            <input type="radio" name="gender" value="2">女  
        </label>  
        <input type="submit" value="submit按钮">  
    </form>  
  
</body>  
</html>


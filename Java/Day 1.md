# 1. 什么是JDK、JRE

1. JDK = JRE + 开发工具集(例如 Javac、java编译工具等)
2. JRE = JVM + Java SE 标准类库

# 2. Java执行流程

- `javac .java`  编译成  `.class`

# 3. Java开发注意事项和细节说明

![](https://img.tucang.cc/api/image/show/96e1e8441570996e59433ac2bc6088e0)


# 4. 文档注释

```markdown
javadoc [options] [packagenames] [sourcefiles] [@files] [-J<javadocoption>]
```

- javadoc -d d:\\temp -author -version hello.java

# 5. 源文件名(.java) 与类名一致问题
```markdown
1. 类名必须要和java文件名一致吗?
	不是的必须的
   如果类名和java文件名不一致,需要将 `class` 前面的`public`干掉
2. 如果`class`前面带`public`，此时类名要和文件名一致
3. 一个java可以写多个class类，但只能有一个类带public
    但是建议不要随意在一个java文件中写多个class -> 一个java文件中就写一个class ,而且带public
4. main 方法必须写在public类中
```

# 6. println 和 print 的区别
	 相同点：都是输出语句
	 不同点：
		 System.out.println(): 输出之后自带换行效果
		 System.out.print()：输出之后不换行

# 7. 数据类型
![450](https://img.tucang.cc/api/image/show/6a36312c0be75f92f0924fdc1298d5bb)


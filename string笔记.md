#String类

##特点
1. **字符串内容永不可变**



2. **因为字符串不可改变，所以字符串可以共享使用**

3. **字符串效果上相当于`char[]`字符数组,但是底层原理是`byte[]`	字符数组。**
 ----
##构造方法
1.	`public String()`

2.	`public String(char[] array)`

3.	`public String(byte[] array)`

4.	`String str = "Hello";`

 ----
##注意事项
字符串常量池:程序中直接写上的双引号字符串，就在字符串常量池中，池中保存的是地址值。new 的不在常量池当中。

![图片](https://i.imgur.com/aHJDZuY.png)

对于基本类型来说，==是进行数值的比较。

对于引用类型来说，==是进行地址值的比较。

----
##方法
1.	`equals()`

2.	`concat()`

3.	`length()`

4.	`charAt()`

5.	`indexOf()`

6.	`subString()`

7.	`toCharArray()`

8.	`getBytes()`

9.	`replace()`

10.	`split`	


#Static
##特点  
	多个对象共享同一份数据（节约内存）
##用法
###1.	静态变量
	多个对象共享同一个变量
	推荐使用类名称.静态变量
###2.	静态方法
	1.静态方法不属于对象，而是属于类
	2.静态方法推荐使用类名称.静态方法
	3.本类当中的可以直接使用静态方法
###3.	注意事项
	1.静态方法不能直接访问非静态变量（静态先创建的）
	2.静态方法不能使用this

![内存图](https://i.imgur.com/V9mDRIO.png)
###4.	静态代码块
	`static{    
	
	  }` 
	 特点：是第一次用到本类时，执行唯一的一次，不管创建多少对象。
	 用途：一次性地对静态成员变量进行赋值
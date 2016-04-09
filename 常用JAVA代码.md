#常用JAVA代码
1. 随机数

	``` java
	java.util.Random random=new java.util.Random();// 定义随机类
	int result=random.nextInt(10);// 返回[0,10)集合中的整数，注意不包括10
	return result+1;              // +1后，[0,10)集合变为[1,11)集合，满足要求
	```
2. 时间处理
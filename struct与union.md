结构体是一种符合数据类型，在写程序时使用起来很方便，可以把相关的变量放在一起，方便管理，调用也很方便，例如记录时间的相关信息需要很多变量

int num;
char name[20];
int year;
int month;
int day;
char department[50];
char major[50];

这么多变量使用的时候很不方便，还容易出错，使用结构体可以进行很好的管理。

//日期结构体
typedef struct{
	int year;
	int month;
	int day;
}DATE;
//学生信息结构体
typedef struct{
	int num;
	char name[20];
	DATE birthday;
	char department[50];
	char major[50];
}STUDENT;
--------------------- 
上述引用感谢：
作者：晴天小风 
来源：CSDN 
原文：https://blog.csdn.net/Ag_nevergiveup/article/details/78499929 
版权声明：本文为博主原创文章，转载请附上博文链接！
--------------------- 
这样我们可以定义结构体变量如下：
STUDENT Student；
可以通过如下方式调用：
Student.num; // 访问学号
Student.birthday.year; // 访问生日相关信息

结构体在定义的时候还需要注意一个比较高级的问题：内存对齐


联合体是一个非常有意思的东西，外观和结构体很相似，但是它特殊的地方是所有成员公用同一块存储区域，这应该也是它称之为“联合”的原因吧。
联合体让开发人员通过不同的方式去访问同一片存储空间有了很方便的方法。

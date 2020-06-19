#### note_python 3.7
##### 1、python3.7安装与运行
```
python安装实际是安装python解析器，
python解析器是用来解析python代码语言为机器可以识别的机器语言。

安装时，若选择“Add python3.7 to path”，则无需配置环境变量，若没有选择，需要另外配置环境变量。
环境变量配置需要配置两点到系统path：
1、python安装路径,如:D:\python37\
2、python下的Scripts目录路径,如:D:\python37\Scripts

运行：
打开终端窗口:
直接命令行输入：python，回车后出现>>>，此时终端窗口处于python交互式命令行模式，可以输入python代码进行测试，
若想返回window命令行需要输入exit()返回

python文件以.py为尾缀，运行python文件需要进入到该文件的目录下，执行命令"python 文件名"

规则：
1、python是大小写敏感的语言,定义的变量或者函数名，调用时要保持大小写一致
2、python代码第一行语句必须顶到最左边，不能有空格
3、多行之间语句要对齐
4、语句之间可以有空行

```

##### 2、python常用的数据类型 
```
1、整数
2、小数（浮点数）
3、字符串(单引号''，双引号""，三单引号'''字符串'''，三双引号"""字符串""",三引号可以赋值特殊格式，如书信格式的字符串，若用单引号必须得借助“\n”显得麻烦)
4、列表（[],方括号包裹，里面的元素可以属于不同数据类型，而且可以是变量可修改）
5、元组((),圆括号包裹，大体类似于列表，唯一不同的是里面的元素不可修改，但是若元祖的某个元素是列表，此列表元素可修改)
6、字典(类似于对象object)

注意元组变量声明,可以省略圆括号：
a=(1,"你好") <==> a=1,"你好"
只有一个元素的时候,必须加逗号“，”
a=(1,)

数字类型运算：
+
-
*
/：（结果必须是小数，浮点型）
//：（结果是舍去小数，得商）
%：取余
**：次方(如：10**3，为10的三次方，结果是1000)

内置函数type(a),验证变量a的数据类型

```

##### 3、变量与注释
```
a=1
也可以同时为多个变量赋值
age,height=43,170
利用列表或元组给多变量赋值,变量数与元素个数要一致，否则报错:
age,height=[43,170]
age,height=(43,170)  <==> age,height=43,170

注释用#
# 注释注释注释注释注释注释
# 注释注释注释注释注释注释

```

##### 4、字符串操作
```
1、字符串拼接用+

2、字符串元素索引（从左往右，从0开始；从右往左，从-1开始。）
a="abced"
a[0] ==> a
a[-1] ==>d

3、字符串切片
a="abcde"
若想得到“abc”,则a[0:3]或者a[:3] ==> 格式a[起始元素下标:结束元素下标+1]

内置函数len(var)，获取字符串长度

```

##### 5、函数
```
1、定义函数(以关键词def，login为函数名，函数体缩进4个空格)
def login(): # 圆括号中可以有形参
    print() #函数体
	print()	#函数体
	return 0 #返回值

2、函数调用
login()

3、缺省值参数
def login(param1,param2,score=60):
    print()
	print()
    return score+1

调用：login(1,2) ==> 61
	login(1,2,70) ==> 71
	
4、指定参数名调用函数
def login(param1,param2,param3,param4):
	print()
	print()

调用：
login(param3=3,param4=4,param2=2,param1=1)  # 指定参数名调用可以打乱形参顺序
login(1,2,param3=3,param4=4)   # 混合使用时，只要指定了参数名，后续参数也要指定参数名

内置函数:
int()
float()
str()
len()
print()
type()

注意若print()输出字符串，不能用字符串+数字，是需要转换的

```

##### 6、input(),待用户键入信息
```
salary = input('请输入张三的薪资：')
print(salary)

用户键入的值是字符串类型，若得到该值进行运算前需要用转换数据类型

```

##### 7、判断元素是否在列表或元组中
```
list=[1,2,3,[4,5,6],7]
tuple=(1,2,3,[4,5,6],7)
3 in list ==> true
3 in tuple ==> true

注意，此为判断元素是否存在列表或元组中，而不是元素的子元素
4 not in list ==> true
4 not in tuple ==> true

```
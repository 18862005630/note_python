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

##### 8、判断语句
```
A:条件表达式

关键词优先级 （优先级：先-》后）
not（置于表达式前，对表达式结果取反,优先级最高）
and (优先级第二)
or (优先级第三)

条件表达式可以连写，如：num=3,2<num<=5 ==>true
2<num<=5即为条件表达式

example:

not 4 > 6  or  'sk' == 'ok' and  4 > 3

1、先算not表达式,即not 4>6,结果为true
2、再算and表达式,即'sk' == 'ok' and 4>3,结果为false
3、最后再算or表达式,即true or false,结果为true，所以最终结果为true

B:判断语句
if 条件表达式:
	函数体
elif 条件表达式:
	函数体
else:
	函数体

注意， else 和 if 对齐，else 情况下的代码 也要缩进。 

```

##### 9、对象方法
```
对象，即之前的数据类型，每个对象都有其对应的方法，调用方式与函数类似，即“对象.方法()”

1、字符串的方法
count:返回字符串对象中包含多少个指定参数的个数。如:'abcedfabchij'.count('abc') ==> 2,abc出现了两次，即数量为2

find：
查找子字符串在父字符串中出现的第一次下标索引,如果没有则返回-1。如：'abcdefabchij'.find('abc') ==> 0
find可以有第二个参数，表示指定查询开始的位置，如：'abcedfabchij'.find('abc',5) ==> 6 表示从索引5的位置开始找‘abc’,索引5对应f

split:以参数为媒介，将字符串切割成列表。（类似于字符串转数组）
如：
str = 'abc,def,hij'
list = str.split(',')  ==> ['abc','def','hij']
注意：若def前有空格，那么切割下来的列表元素也会保留空格的

splitlines：按换行符将字符串切割成列表
如：
salary = '''
小王  10000元
小李  20000元
小徐  15000元
'''
print(salary.splitlines())  ==》 ['', '小王  10000元', '小李  20000元', '小徐  15000元']

join:以形参为媒介，将列表元素连接成一个字符串。
'|'.join(['abc','def','hij'])  ==> 'abc|def|hij'

strip:去除字符串前面和后面的空格，不去除字符串中间的空格。如：' befd fgh  '.strip() ==>'befd fgh'
lstrip:去除字符串左侧的空格。如：' befd fgh  '.lstrip() ==>'befd fgh  '
rstrip：去除字符串右侧的空格。如：' befd fgh  '.strip() ==>' befd fgh' 

replace:用子字符串替换父字符串中指定的某段字符串。replace(指定要被替换的字符串，子字符串)
如:
str1 = 'abcdefhijabckol'
str1 = str1.replace('abc','ppp')  ==> 'pppdefhijpppkol'

startswith: 方法检查字符串是否以参数指定的字符串 开头，如果是，返回True，否则返回False
endswith: 方法检查字符串是否以指定的字符串 结尾，如果是，返回True，否则返回False
example:
str1 = '我们今天不去上学，我们去踢足球'
str1.startswith('我们')  # 返回 True
str1.endswith('我们')    # 返回 False

isdigit: 方法检查字符串是否全部由数字构成，如果是，返回True，否则返回False

2、列表的方法
append:在列表最后添加一个元素。如：a=[1,2,3],a.append(4) ==>[1,2,3,4]

insert:在列表指定位置插入一个元素。如：a=[1,2,3],a.insert(0,9) ==>[9,1,2,3]

pop:从列表取出指定下标的元素并删除该元素。
如：a=[1,2,3,4,6,7]
b=a.pop(2)  #取出下标2的元素并赋值给变量b，最终在列表a中删除该元素
所以，b的值为3，a的值为[1,2,4,6,7]

remove:根据指定值去列表中删除，但只会删除查找到的第一个值
a=['a','b','c','a']
a.remove('a') ==> ['b','c','a']

reverse:将列表元素倒过来
a=[1,2,3,4,5]
a.reverse() ==>[5,4,3,2,1]

```

##### 10、格式化字符串
```
A、printf风格(%s 为占位符， 对应的格式化对象， 不仅仅是字符串，还可以是整数、 浮点数、列表、元组 等等)
1、使用%s占位符，后续通过元组依次进行赋值
如:
print('税前薪资：%s元，缴税：%s元，税后薪资：%s元' %(salary,tax,aftertax))
前面有3个占位符，元组中也应该有三个元素；注意只有一个占位符时，元组中一个元素后需要加逗号“，”

2、指定宽度和对齐
通过%10s指定格式化结果至少10个字符
'税前薪资：%10s 元' % 100000
'税前薪资：%10s 元' % 10000
'税前薪资：%10s 元' % 1000
结果:
税前薪资：    100000 元
税前薪资：     10000 元
税前薪资：      1000 元

如果我们希望是左边对齐，而不是右边对齐，就可以加一个 "-"
'税前薪资：%-10s 元' % 100000
'税前薪资：%-10s 元' % 10000
'税前薪资：%-10s 元' % 1000
结果:
税前薪资：100000     元
税前薪资：10000      元
税前薪资：1000       元

3、占位符%d和%f
%d:整数占位符
%f:浮点数占位符
补0而非空格：%010d,%010f
保留小数2位小数:%010.2f

B、f-string格式化(必须python3.6以上版本)
格式：在字符串模板前面加上f，然后占位符使用{} ,里面直接放入对应的数据对象。
如：
1、print(f'税前薪资是：{salary}元， 缴税：{tax}元， 税后薪资是：{aftertax}元')
2、指定宽度
print(f'{salary:10}') 
3、指定左对齐(使用"<",则在右侧补空格或0)
salary=8320
f'税前薪资是：{salary:<8}元 ==> 税前薪资是：8320    元
4、小数点后位数
如果我们想指定小数点后保留几位，可以像这样 {salary:<8.1f}
5、不足补0
salary=8320
{salary:08} ==》 00008320
tax=2080
{tax:08.1f} ==》 002080.0

以上是对 数字 的不足补零，如果要对 字符串 不足补零，就应该 使用符号 < 或者 > 同时指定左右对齐方式。字符串补0不指定左右对齐方式会报错。
var='34324'
f'{var:<08}' ==> '34324000' 左对齐则右侧补0
f'{var:>08}' ==> '00034324' 右对齐则左侧补0

6、16进制格式化数字
# 用 x 表示格式化为16进制，并采用小写格式
f'数字65535的16进制表示为：{65535:x}' 
# 用 X 表示格式化为16进制，并采用大写格式
f'数字65535的16进制表示为：{65535:X}'

7、字符串中有花括号，则花括号必须双写转义
如：字符串为：'文章中 { 符号 出现了 xx 次'
times1 = 1000
times2 = 2000
{% raw %}
print(f'文章中 {{ 符号 出现了 {times1} 次')
print(f'文章中 }} 符号 出现了 {times2} 次')
{% endraw %}

8、转义字符'\'
\n:换行
window下路径:
path = 'c:\windows\temp'
需转义为：
path = 'c:\\windows\\temp'

```

##### 11、循环
```
while循环和for循环

while:
i = 1
while i <= 100:
    print(i)
    i += 1

for:
studentAges = ['小王:17', '小赵:16', '小李:17', '小孙:16', '小徐:18']

for student in studentAges:
    print(student)

注意：如果循环一个空列表不会报错，只是不执行
for one in []:
    print(one)

指定循环次数:
# range里面的参数100 指定循环100次
# 其中 n 依次为 0,1,2,3,4... 直到 99
for n in range(100):  
    print(n)
注意：和Python 2 不同， Python 3 中的range 并不是一个函数，不会返回一个数字列表。 Python 3 中的range 是一个类
如果你想返回一个 从 0到99的数字列表， 可以这样写 : list(range(100))

打印出从50 到 100 所有的数字（两个参数指定范围）：
for n in range(50,101):  
    print(n) 
range(50,101) 表示从 50 开始， 到 100 结束

打印50到100，每次递增5（三个参数，前两个指定范围，第三个表示递增数）:
for n in range(50,101,5):  
    print(n) 

enumerate 函数(返回列表元素的同时还返回下标索引，索引与元素本身组成元组返回):
studentAges = ['小王:17', '小赵:16', '小李:17', '小孙:16', '小徐:18']
# enumerate (studentAges) 每次迭代返回 一个元组
# 里面有两个元素，依次是 元素的索引和元素本身 
for idx, student in enumerate(studentAges):
    if int(student.split(':')[-1]) > 17:     # 列表索引-1表示最后一个元素
        print(idx)

continue:结束单次循环，会继续后面的循环
break:终止整个循环
return：只用于函数，若用于循环会报错
【函数】中的循环体内的代码， 使用 return 和 break 都可以从循环中跳出。
但是，break 只是 跳出循环， 如果循环后面还有代码， 会进行执行;return 则会从函数里面立即返回。

列表推导式:
for循环方式：
list1 = [1,2,3,4,5,6]
list2 = []
for num in list1:
    list2.append(num*num)
列表推导式方式（对列表a的所有元素做相同操作得到列表b）：
list1 = [1,2,3,4,5,6]
list2 = [num**2 for num in list1]

循环嵌套:
list1 = ['关羽','张飞','赵云','马超','黄忠']
list2 = ['典韦','许褚','张辽','夏侯惇','夏侯渊']

for member1 in list1:
    for member2 in list2:
        print(f'{member1} 大战 {member2}')

冒泡排序：
def bubbleSort(arr):
    length = len(arr)

    for j in range(length-1,0,-1):
        for i in range(0,length-1):
            if arr[i] > arr[i+1]:
                arr[i], arr[i+1]= arr[i+1],arr[i]

    return arr

```

##### 12、字符编码
```
字符串编码为字节串：str.encode('utf8')
字节串解码成字符串：str.decode('utf8')

```

##### 13、文本文件读写
```
在python语言中，我们要读写文本文件， 首先通过内置函数open 打开一个文件。
open函数会返回一个对象，我们可以称之为文件对象。
这个返回的文件对象就包含读取文本内容和写入文本内容的方法。
要写入字符串到文件中，需要先将字符串编码为字节串。
而从文本文件中读取的文本信息都是字节串，要进行处理之前，必须先将字节串解码为字符串。
文件的打开，分为 文本模式 和 二进制模式。
1、文本模式：
open(
    file, 
    mode='r', 
    buffering=-1, 
    encoding=None, 
    errors=None, 
    newline=None, 
    closefd=True, 
    opener=None
    ) 
以下三个参数最常用:
参数 file：指定了要打开的文件的路径，可以是相对路径也可以是绝对路径
参数 mode:指定文件打开的模式。（r：只读文本模式打开，最常用的模式且默认 w：只写文本模式打开，表示覆盖写文件 a：追加文本模式打开 
如果我们要 读取文本文件内容到字符串对象中 ， 就应该使用 r 模式。
如果我们要 创建一个新文件写入内容，或者清空某个文本文件重新写入内容， 就应该使用 ‘w’ 模式。
如果我们要 从某个文件末尾添加内容， 就应该使用 ‘a’ 模式。）
参数 encoding:指定读写文本文件时使用的字符编解码方式,默认gbk编码

写文件示例：
# 指定编码方式为 utf8
f = open('tmp.txt','w',encoding='utf8')
# write方法会将字符串编码为utf8字节串写入文件
f.write('白月黑羽：祝大家好运气')
# 文件操作完毕后， 使用close 方法关闭该文件对象
f.close()

读文件示例:
# 指定编码方式为 gbk，gbk编码兼容gb2312
f = open('tmp.txt','r',encoding='gbk')
# read 方法会在读取文件中的原始字节串后， 根据上面指定的gbk解码为字符串对象返回
content = f.read()
# 文件操作完毕后， 使用close 方法关闭该文件对象
f.close()
# 通过字符串的split方法获取其中用户名部分
name = content.split('：')[0]
print(name)

注意read函数有参数size，读取文本文件的时候，用来指定这次读取多少个字符。 如果不传入该参数，就是读取文件中所有的内容。
tmp.txt文件内容为：
hello
cHl0aG9uMy52aXAgYWxsIHJpZ2h0cyByZXNlcnZlZA==

# 因为是读取文本文件的模式， 可以无须指定 mode参数
# 因为都是 英文字符，基本上所以的编码方式都兼容ASCII，可以无须指定encoding参数
f = open('tmp.txt')
tmp = f.read(3)  # read 方法读取3个字符
print(tmp)       # 返回3个字符的字符串 'hel' 
tmp = f.read(3)  # 继续使用 read 方法读取3个字符
print(tmp)       # 返回3个字符的字符串 'lo\n'  换行符也是一个字符
tmp = f.read()  # 不加参数，读取剩余的所有字符
print(tmp)       # 返回剩余字符的字符串 'cHl0aG9uMy52aXAgYWxsIHJpZ2h0cyByZXNlcnZlZA==' 
# 文件操作完毕后， 使用close 方法关闭该文件对象
f.close()  

读取文本文件内容的时候，通常还会使用readlines方法，该方法会返回一个列表。 列表中的每个元素依次对应文本文件中每行内容。但此方法每个元素最后都有一个换行符，若不想有换行符可以用字符串函数splitlines()
f = open('tmp.txt')
linelist = f.readlines() 
f.close()  
for line in linelist:
    print(line)

splitlines()方式:
f = open('tmp.txt')
content = f.read()   # 读取全部文件内容
f.close()  
# 将文件内容字符串 按换行符 切割 到列表中，每个元素依次对应一行
linelist = content.splitlines()
for line in linelist:
    print(line)

2、二进制（字节）模式
读示例:
# mode参数指定为rb 就是用二进制读的方式打开文件
f = open('tmp.txt','rb')
content = f.read()   
f.close()  
# 由于是 二进制方式打开，所以得到的content是 字节串对象 bytes
# 内容为 b'\xe7\x99\xbd\xe6\x9c\x88\xe9\xbb\x91\xe7\xbe\xbd'
print(content) 
# 该对象的长度是字节串里面的字节个数，就是12，每3个字节对应一个汉字的utf8编码
print(len(content))

写示例(以二进制方式写数据到文件中，传给write方法的参数不能是字符串，只能是bytes对象):
# mode参数指定为 wb 就是用二进制写的方式打开文件
f = open('tmp.txt','wb')
content = '白月黑羽祝大家好运连连'
# 二进制打开的文件， 写入的参数必须是bytes类型，
# 字符串对象需要调用encode进行相应的编码为bytes类型
f.write(content.encode('utf8'))

二进制方式拷贝一个文件内容：
def fileCopy(srcPath,destPath):
    srcF = open(srcPath,'rb')
    content = srcF.read()
    srcF.close()

    destF = open(destPath,'wb')
    destF.write(content)
    destF.close()

fileCopy('1.png','1copy.png')

with语句(防止程序员忘记调用文件的close方法，python解释器自动调用):
# open返回的对象 赋值为 变量 f
with open('tmp.txt') as f:
    linelist = f.readlines() 
    for line in linelist:
        print(line)

写入缓冲:
f = open('tmp.txt','w',encoding='utf8')
f.write('白月黑羽：祝大家好运气')
# 等待 30秒，再close文件
import time
time.sleep(30)
f.close()
延迟30秒再关闭文件，在30秒之前打开文件会发现没内容，这是因为提交的内容给的是操作系统，操作系统为提高效率将内容写入缓冲，只能等缓冲堆满或者用户调用close操作才能在文件中看到内容。

若想立即看到内容写到文件中，可调用flush方法：
f = open('tmp.txt','w',encoding='utf8')
f.write('白月黑羽：祝大家好运气')
# 立即把内容写到文件里面
f.flush()
# 等待 30秒，再close文件
import time
time.sleep(30)
f.close()

```

##### 14、模块和库
```
一个py文件即为一个模块
模块之间的调用:
1、直接通过关键词import导入模块对象
import aa  
aa.param1  # 调用模块aa的属性
aa.func()  # 调用模块aa的函数

2、通过from import导入模块对象的标识符（属性，函数等）
from aa import func 
func()  # 直接引用模块aa的方法

多模块导入：
import aa,bb,cc
一个模块导入多个标识符:
from aa import func1,var1,func2,var2
导入一个模块中所有标识符:
from aa import *
同名则指定别名：
from aa import func
from bb import func as func2
func() # 调用模块aa的函数
func2() # 调用模块bb的函数

注意bb模块导入aa模块的一个变量后，模块aa和bb分别有一个同名的变量，若改变模块aa的该变量值后，模块bb中的该变量是不变的，他们是分别拥有一个同类型的变量，不是共享一个变量

包：存放py模块文件的目录称为包，且包中需要有一个名为_init_.py的初始化文件，该文件一般为空，也可有代码。当包中模块被导入的时候会执行初始文件的代码。
example:
stock/                        ---   顶层包
        __init__.py           ---   stock包的初始化文件
        food/                 ---   food子包
                __init__.py
                pork.py
                beef.py
                lobster.py
                ...
        furniture/            ---   furniture子包
                __init__.py
                bed.py
                desk.py
                chair.py
                ...
        kitchen/              ---   kitchen子包
                __init__.py
                knife.py
                pot.py
                bowl.py
                ...

import stock.food.beef
# 注意导入的是 stock.food.beef，调用的时候一定要加上所有的包路径前缀
stock.food.beef.stockleft()
或
from stock.food.beef import stockleft
stockleft()

python标准库
1、内置库(函数或类型不需要使用import即可使用)
如内置类型：int、float、str、list、tuple等
内置函数: int，str，print，type，len 等等

其他库需要使用import引入才能使用库里面的函数:
如:sys, os, time, datetime, json，random 等
example:
import sys
sys.exit(0) # 结束python程序

时间：
import datetime

# 返回这样的格式 '20160423'
datetime.date.today().strftime("%Y%m%d") 

# 返回这样的格式 '20160423 19:37:36'
datetime.datetime.now().strftime("%Y%m%d %H:%M:%S")

随机整数:
from random import randint

# 在 数字 1 到 8 之间(包括1和8本身)，随机取出一个数字
num = randint(1,8)
print(num)

安装其他库:
在Python中，安装第三方库，通常是使用pip命令。
那些优秀的第三方库，基本都是放在一个叫 PYPI 的网站上

我们在国内，使用pip 安装的时候，可能由于网络原因，到国外访问 PYPI 会比较慢。
而国内有网站（比如豆瓣）对PYPI 做了镜像备份。
我们可以通过在命令中加上参数 -i https://pypi.douban.com/simple/ ，这样就指定使用豆瓣作为安装包的下载网站。
example:
安装 requests库:
pip install requests -i https://pypi.douban.com/simple/
如果pip安装库的时候，出现SSL错误，可能是网络对https证书校验的问题，可以改用http协议下载:
pip install requests -i http://pypi.douban.com/simple/  --trusted-host pypi.douban.com

注意：安装命令在cmd中运行，不是在python交互式命令行执行。
安装后导入库:
import requests
requests.get('http://www.baidu.com')




```


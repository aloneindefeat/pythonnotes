# Python基础
## 特点

### 1、Simple：
Python语法简单、格式优美，写程序让人有种写作文的感觉，所以显得简单

### 2、Easy to learn：
容易学习，通常解析型语言都比编译型语言容易学习。所谓静态语言和动态语言很重要的一点就是，声明变量是否需要指定其数据类型。

### 3、Free and Open Source:
免费和开源，一旦你要发布你的程序，那么你的源代码就会随着一起发布

### 4、High-level Language：
高层语言也就意味着你能够更简单和轻松地实现一些功能，而不需要考虑程序本身底层的一些细节（比如内存操作等）

### 5、Portable：
可移植性，由于其开源在很多平台上都得到了支持，比如Linux，mac os 都默认安装了python解释器

### 6、Interpreted：
解析型语言，如C/C++语言的执行时要经过编译成机器码才能执行，而Python等动态语言是直接由解释器所解释执行的。通常编译型语言执行速度非常快，解释型语言相对比较慢（开发效率刚好相反）

### 7、Object Oriented：
面向对象特性也是Python的一大特点，当然python也可以面向过程使用

### 8、Extensible：
可扩展性，如果你需要你的一段关键字代码运行得更快或者希望某些算法不公开，你可以把你的部分程序用C或C++编写，然后再你的python程序中使用它们

### 9、Embeddable：
你可以把python嵌入你的C/C++程序，从而向你的程序用户提供脚本功能

## Python定位应用

### 1、web开发（flask/Django/Tornade）

### 2、科学计算/数据分析/算法学习（Numpy/Scipy）

### 3、机器学习（Scikit-Learn）

### 4、网络爬虫（Scrapy/BeautifulSoup）

### 5、图片处理/游戏开发（Pillow）

### 6、运维/测试自动化开发（saltstack）

#### 开启虚拟环境（局部环境）（会污染全局）

### 步骤
print(sys.path)  # 保留python的路径   执行以上两行看到已经把虚拟环境加进来了，可以开始正式地编程了！每一个项目都需要开启自己的一个虚拟环境。

## pip（包管理工具操作）

### pip install novas（下载包裹）机器学习、

### pip install requests == 2.6.0（下载版本）

### pip uninstall novas

### pip show flask（显示包裹信息）

### pip list（显示所有包裹）

### pip freeze > requirements.txt将安装的包裹列表输出到requirements.txt中（生成了一个提示文件），
以便执行pip install -r requirements.txt（虚拟环境被删掉，只下载了项目代码，自己创建回原虚拟环境（tutorial-env\Scripts\activate.bat）。执行pip install -r requirements.txt（下载回之前输到txt文件的包裹），然后pip list 查看时就有了之前被删掉的安装的包裹。）

- 上传到github时，不上传虚拟环境：删掉这个虚拟文件，在项目文件上右击新建一个文件名为.gitignore，在新建的文件里面写上tutorial-env（忽略的文件名，以便后续安装回该虚拟环境文件夹），VCS里的git里的add直接发布，或者在命令行直接写命令一直到git push推上去，进github主页里就没有那个文件了。

## 定义

### python解释器

### python语言特点

- 动态类型、强类型语言

## 输入输出测试工具

### 输入工具  编辑器注释ctrl+/
内建函数 input获取的数据都是字符串类型
string=input("请输入你的名字")   
print(type(string))  

输出工具   
print("123")
print("123","456",end="")
print("123",456,1+2)

格式化打印  字符串用法  %s占位
print("我叫%s,我的年龄是%d,我的成绩%0.2f"%('wss',20,60.09))
print("我叫%s"%'wss')

## 变量

### 变量的定义

- 可变的数据

### 变量的语法

- python赋值变量
1 普通方式   
a = 10

2 链式方式
b=c=d=20

3 多元方式
e,f=10,20

交换方式，变量直接绑定下来，然后依次赋值
e,f = f,e
print(a,b,c,d,e,f)

### 变量命名的特点

- 1 不可以是关键字和保留字  
2 数字、字母、下划线、汉字，数字不能开头  
3 尽量语义化  
4 严格区分大小写  
5 不能使用特殊符号

### 变量的特性

- 不支持自增自减
- 变量可以存储不同的数据类型

## 数据类型

### js与python数据类型的对比

- js：数字、字符串、boolean、null、undefined（声明未定义）、object

- python：数字、字符串、布尔、null、
             列表（数组）元组、  字典（object\json）集合

js分类：基本数据类型和引用数据类型
python分类：可变数据类型和不可变数据类型（全部是引用的）
可变数据类型：列表、字典、集合（其余都是不可变的）

### 布尔型boolean
- 非空非0为真，0或None为假
- Ture   False

### 数字型number

- 整数int

	- 整数的最大值取决于电脑内存的大小，没有上限

- 浮点数float

	- 只要有小数点就是浮点数，无穷小数会做精度的处理（除运算也会做精度的处理）

		- 0.1
		- 5.0

	- 数字精度：内建函数、模板字符串（控制小数精度）

- 负数
- 分数

### 字符串 str

- 语法

	- 1、单引号
	- 2、双引号

		- 换行的时候加 \

	- 3、三引号

		- 三引号''''''(支持换行、块级注释) """""""(注释)

- 注意

	- 只要是用引号括起来的就是字符串
	- python不区分字符和字符串
	- 字符串是不可变对象

- 延展

	- 转义字符  “\”

		- 使用特殊字符时就需要转义字符
常用的转移字符：
\n   \t  \r  \*  \\

	- 字符编码

		- ASCII

			- 起源于美国，主要对英文进行编码

		- GBK：中国的字符编码
		- Unicode：万国码
		- utf-8：更精确的万国码

	- 前缀

		- r“str”r后的字符串为普通字符串
		- b“str”b后的字符串为bytes格式
		- u“str”u后的字符串为Unicode格式

- 重要用法

	- 切片

		- 切片(截取)
切片功能

a = "山西优逸客科技有限公司"
```
print(a[2:5])
```
切片语法   string[start:end:step]  [初始值：结束值：步进值]  所有的值都可以是负值或空 

默认:start == 0（前开始、后开始）  end == 结尾（前结尾、后结尾） step == 1 如果为-1,就是改变方向
```
print(a[-1])
print(a[-2:])
print(dir(a))
```
模仿方法（面向对象）  字符串内建函数（方法）

- 字符串高级

	- 字符串内建函数  print（dir（aa））
会打印出一个列表（数组），里面有双前后下划线的方法称为模板方法（面向对象），把其余的字符串内建函数（字符串的方法）练习一下。

- string.capitalize() 把字符串的第一个字符大写
string.center(width) 返回一个原字符串居中,并使用空格填充至长度 width 的新字符串
string.count(str, beg=0, end=len(string)) 返回 str 在 string 里面出现的次数，如果 beg 或者 end 指定则返回指定范围内 str 出现的次数
string.decode(encoding='UTF-8', errors='strict') 以 encoding 指定的编码格式解码 string，如果出错默认报一个 ValueError 的 异 常 ， 除非 errors 指 定 的 是 'ignore' 或 者'replace'
string.encode(encoding='UTF-8', errors='strict') 以 encoding 指定的编码格式编码 string，如果出错默认报一个ValueError 的异常，除非 errors 指定的是'ignore'或者'replace'string.endswith(obj, beg=0, end=len(string)) 检查字符串是否以 obj 结束，如果beg 或者 end 指定则检查指定的范围内是否以 obj 结束，如果是，返回 True,否则返回 False.

* string.expandtabs(tabsize=8) 把字符串 string 中的 tab 符号转为空格，tab 符号默认的空格数是 8。

* string.find(str, beg=0, end=len(string)) 检测 str 是否包含在 string 中，如果 beg 和 end 指定范围，则检查是否包含在指定范围内，如果是返回开始的索引值，否则返回-1
### 常见的字符串对象
string.format() 格式化字符串

* string.index(str, beg=0, end=len(string)) 跟find()方法一样，只不过如果str不在 string中会报一个异常.

* string.isalnum() 如果 string 至少有一个字符并且所有字符都是字母或数字则返回 True,否则返回 False

* string.isalpha() 如果 string 至少有一个字符并且所有字符都是字母则返回 True,否则返回 False

* string.isdecimal() 如果 string 只包含十进制数字则返回 True 否则返回 False.

* string.isdigit() 如果 string 只包含数字则返回 True 否则返回 False.

* string.islower() 如果 string 中包含至少一个区分大小写的字符，并且所有这些(区分大小写的)字符都是小写，则返回 True，否则返回 False

* string.isnumeric() 如果 string 中只包含数字字符，则返回 True，否则返回 False

* string.isspace() 如果 string 中只包含空格，则返回 True，否则返回 False.

* string.istitle() 如果 string 是标题化的(见 title())则返回 True，否则返回 False

* string.isupper() 如果 string 中包含至少一个区分大小写的字符，并且所有这些(区分大小写的)字符都是大写，则返回 True，否则返回 False

* string.join(seq) 以 string 作为分隔符，将 seq 中所有的元素(的字符串表示)合并为一个新的字符串

* string.ljust(width) 返回一个原字符串左对齐,并使用空格填充至长度 width 的新字符串
string.lower() 转换 string 中所有大写字符为小写.

* string.lstrip() 截掉 string 左边的空格
string.maketrans(intab, outtab)

* maketrans() 方法用于创建字符映射的转换表，对于接受两个参数的最简单的调用方式，第一个参数是字符串，表示需要转换的字符，第二个参数也是字符串表示转换的目标。

* max(str) 返回字符串 str 中最大的字母。
* min(str) 返回字符串 str 中最小的字母。

* string.partition(str) 有点像 find()和 split()的结合体,从 str 出现的第一个位置起,把 字 符 串 string 分 成 一 个 3 元 素 的 元 组 (string_pre_str,str,string_post_str),如果 string 中不包含str 则 string_pre_str == string.

* string.replace(str1, str2,  num=string.count(str1)) 把 string 中的 str1 替换成 str2,如果 num 指定，则替换不超过 num 次.

* string.rfind(str, beg=0,end=len(string) ) 类似于 find()函数，不过是从右边开始查找.
* string.rindex( str, beg=0,end=len(string)) 类似于 index()，不过是从右边开始.

* string.rjust(width) 返回一个原字符串右对齐,并使用空格填充至长度 width 的新字符串
* string.rpartition(str) 类似于 partition()函数,不过是从右边开始查找

* string.rstrip() 删除 string 字符串末尾的空格.
* string.split(str="", num=string.count(str)) 以 str 为分隔符切片 string，如果 num 有指定值，则仅分隔 num+ 个子字符串
* string.splitlines([keepends]) 按照行('\r', '\r\n', \n')分隔，返回一个包含各行作为元素的列表，如果参数 keepends 为 False，不包含换行符，如果为 True，则保留换行符。
* string.startswith(obj, beg=0,end=len(string)) 检查字符串是否是以 obj 开头，是则返回 True，否则返回 False。如果beg 和 end 指定值，则在指定范围内检查.
* string.strip([obj]) 在 string 上执行 lstrip()和 rstrip()
* string.swapcase() 翻转 string 中的大小写
* string.title() 返回"标题化"的 string,就是说所有单词都是以大写开始，其余字母均为小写(见 istitle())
* string.translate(str, del="") 根据 str 给出的表(包含 256 个字符)转换 string 的字符,要过滤掉的字符放到 del 参数中
* string.upper() 转换 string 中的小写字母为大写
* string.zfill(width) 返回长度为 width 的字符串，原字符串 string 右对齐，前面填充0

### 列表List

- 定义

	保存一系列相关数据的集合

- 语法

	arr = [1,2,3,4,5]
访问列表
print(arr[0])

- 注意：

	可以保存任何数据类型


- 访问列表

	 arr[index]

- 常用的遍历列表的方式

	 方法1

		 arr = [[1,2],[3,4]]
```
for i in arr:
    print(i)
    print(arr.index(i),i)
```
range()内建函数：
1个参数：结束的值  会返回包含0-n之间的数的序列
```
print(list(range(10)))    #强制转换成列表
```
2个参数：开始的位置，结束的位置。返回包含开始-结束之间的序列
```
print(list(range(5,10)))
```
3个参数：开始的位置，结束的位置，步进值。

方法2
```
 arr = [[1,2],[3,4]]
for i in range(len(arr)):
    print(i,arr[i])
```
方法3
```
arr = [[1,2],[3,4]]
```
enumerate() 返回列表元素的下标和值
```
print(list(enumerate(arr)))
for i,v in enumerate(arr):
    print(i,v)
```
方法4
赋值 枚举类型去遍历
```
a,b,c,d,e = (1,2,3,4,5)
```
- 列表的长度

	- 获取列表长度
print(len(arr[-1]))

浅拷贝和深拷贝
```
	arr1=arr #传址
	# a=10
	# b=a
	# print(id(a),id(b))   #相等
	# print(id(arr1),id(arr)) #同样相等
	# arr1[0]='pp'
	#print(arr1)
	# print(arr)
	# arr=[1,2,5,8,7]
	# import copy
	# arr1=copy.deepcopy(arr) #deepcopy深拷贝   
	# print(id(arr1),id(arr))  #不相等了
	# arr[2]=200
	# print(arr1)
	# print(arr)   #不相等  所以这个时候要用到深拷贝
	# arr1=arr.copy()  #浅拷贝
```
#### 列表推导式

1.列表推导式
	语法
	
（1）每个元素幂运算
```	
# arr=[1,2,5,8,85,9]
# arr2=[item*item for item in arr]
# print(arr2)
```
(2)输出偶数并且幂运算
```
# arr1=[item*item for item in arr if item%2==0]
# print(arr1)
# #输出1~100的偶数
# arr3=list(range(1,101))
# # print(arr3)
# arr4=[item for item in arr3 if item%2==0]
# print(arr4)
```
推导式的分类：
1 列表推导式   2 字典推导式   3 集合推导式
1 列表推导式

#### Python列表内建函数

* 1.count()：用来统计某一个成员在列表中的出现次数

* 2.index()：返回该元素的下标

* 3.reverse()：就是将列表中的元素前后颠倒

* 4.sort()：将元素从小到大排序
	list1 = [5,8,2,6,7,3]
	list1.sort(reverse=True)
	list1
	[8, 7, 6, 5, 3, 2]	
* 5.append()：向列表中添加成员，一次只能添加一个成员，并且只能添加在列表的末尾。如果想在列表中添加列表，可以通过append()方法
	list1.append('1')
	list1.append(1)
	list1
	[8, 7, 6, 5, 3, 2, '1', 1]	

* 6.extend()：该方法也是向列表中添加成员，并且也是一个参数，但是可以列表扩展列表（如果你想添加多个成员的时候）
	list1 = [123,456,789]
	list1.extend(['wanglu','123',123])
	list1
	[123, 456, 789, 'wanglu', '123', 123]
	list1.extend('love')
	list1
	[123, 456, 789, 'wanglu', '123', 123, 'l', 'o', 'v', 'e']

* 7.insert()：在特定位置添加成员。两个参数，insert(m,member)，在索引为m(也就是第m+1的位置进行添加)

* 8.remove()：从列表中删除指定成员

* 9.del ：用索引进行删除

* 10.pop()：将指定位置的元素取出来，并删除，也就是说有返回值的。

### 元组 tuple 

- 定义：不可改变的列表，不能修改
- 语法

	- 语法：
t1 = ()
print(type(t1))
t2 = (1,)
print(type(t2))
面试题  数组的id地址不变就是一个数组
t1 = ([1,2],[3,4])
t1[0][0] = 2
print(t1)

- 注意

	- 1、元组和列表类似，区别就是元组的元素不可以改变
2、元组通过圆括号定义
3、可以使用切片
4、元组可以定义只有一个元素的元组
	t2 = (1,)
	print(type(t2))
5、空元组   mytuple = ()   #tuple类型
	- 定义一个元组得加逗号，不然定义的就是int型

- 访问元组：同列表
- 便利元组：同列表
- 元组高级

	- 元组的内建函数

		- 元组内建函数
		cmp(tuple1, tuple2)  比较两个元组元素。
		len(tuple)  计算元组元素个数。
		max(tuple)  返回元组中元素最大值。
		min(tuple)   返回元组中元素最小值。
		tuple(seq)  将列表转换为元组。
		- tuple.index(obj,end=len(tuple))
		- tuple.count(obj)   #返回obj出现

### 字典 dict（对象，json）

- 语法

	- 创建方式

* (1)json方式
```
dict1 = {1:123,'name':'wss',(1,2,3):'abc'}
访问
print(dict1[1])
print(dict1['name'])
print(dict1[(1,2,3)])
```
* (2) 通过内建函数dict()创建dict2 = dict() 创建了空字典设置键值
```
dict2[1] = 123
dict2['name'] = 'wss'
dict2[(1,2,3)] = 'abc'
```
访问
print(dict2)
* (3）批量创建键值
dict3 = dict.fromkeys([1,2,3,4,5],'a')
print(dict3)

- 注意

- 1、字典以键值对形式存在：{key:value}
- 2、查找和插入的速度极快，不会随着key的增加而增加
- 3、一些可变的数据类型不可做key值，而value可以是任意数据
- 4、字典中数据元素是无序的，没有办法进行向索引和切片操作
- 5、字典是可变数据类型
	 字典的键需要进行哈希运算，所以键是不可变数据类型（只要键能进行哈希运算，所有内容都可以作为键【字符串、数字型、变量（存的值是不可变的数据类型能够进行哈希运算）

字典访问方式

	 mylist[键]

添加属性和方法

	 mylist['newKey'] = value

删除字典属性和方法

    del删除字典的数据以及字典  通过del
```
		del dict3[2]
		print(dict3)
		del dict3
		print(dict3)
```
 字典推导式
```
1、d2 = { k:str(v)+'m' for k,v in d.items() }
	print(d2)
		 
2、 d3 = { k:str(v + d[k.upper()])+'px' for k,v in d.items() if k.islower()}
	 print(d3)
```
#### 字典常用内建函数

1、D.get(key, 0)       #同dict[key]，多了个没有则返回缺省值，0。[]没有则抛异常

2、D.has_key(key)      #有该键返回TRUE，否则FALSE

3、D.keys()            #返回字典键的列表

4、D.values()          #以列表的形式返回字典中的值，返回值的列表中可包含重复元素

5、D.items()           #将所有的字典项以列表方式返回，这些列表中的每一项都来自于(键,值),但是项在返回时并没有特殊的顺序        

6、D.update(dict2)     #增加合并字典

7、D.popitem()         #得到一个pair，并从字典中删除它。已空则抛异常

8、D.clear()           #清空字典，同del dict

9、D.copy()            #拷贝字典

10、D.cmp(dict1,dict2)  #比较字典，(优先级为元素个数、键大小、键值大小)
                    #第一个大返回1，小返回-1，一样返回0

11、D.pop(key[,default])       #删除字典给定键 key 所对应的值，返回值为被删除的值。key值必须给出。 否则，返回default值。

12、dict.fromkeys(seq[, val])      #创建一个新字典，以序列 seq 中元素做字典的键，val 为字典所有键对应的初始值
dictionary的复制
dict1 = dict        #别名
dict2=dict.copy()   #克隆，即另一个拷贝。

### 集合 set（结合了字典和列表）

- 定义

	- set()    #把其他内容转化为集合

- 集合高级

	- 集合推导式

		- 集合推导式
法1
s1 = {1,2,3,4,5,6}
s2 = { item+1 for item in s1}
print(s2)
法2
s2 = { item for item in s1 if item%2==0}
print(s2)

#### 集合内建函数

add()	为集合添加元素

clear()	移除集合中的所有元素

copy()	拷贝一个集合


difference()	返回多个集合的差集
difference_update()	移除集合中的元素，该元素在指定的集合也存在。

discard()	删除集合中指定的元素

intersection()	返回集合的交集

intersection_update()	删除集合中的元素，该元素在指定的集合中不存在。

isdisjoint()	判断两个集合是否包含相同的元素，如果没有返回 True，否则返回 False。

issubset()	判断指定集合是否为该方法参数集合的子集。

issuperset()	判断该方法的参数集合是否为指定集合的子集

pop()	随机移除元素

remove()	移除指定元素

symmetric_difference()	返回两个集合中不重复的元素集合。

symmetric_difference_update()	移除当前集合中在另外一个指定集合相同的元素，并将另外一个指定集合中不同的元素插入到当前集合中。

union()	返回两个集合的并集

update()	给集合添加元素


#### 通过set集合元素互异性进行列表的去重
```
arr1 = [1,1,2,2]
print(list(set(arr1)))
```
### 测试数据类型

- type

## 运算符

### 算数运算符

- + - * /   %   //地板除   **幂运算

(1)+  加法运算：算数运算，字符串拼接作用   str  list  tuple
print("str1" + "str2")
print([1,2,3] + [4,5,6])
print((1,2,3) + (4,5,6))

(2)*  乘法运算：用法同加法
print('srt1'*2)
print([1,2]*2)
print((1,2)*2)

(3)/  除法的运算结果都是浮点型
print(10/5)

(4)//  地板除:向下取整
print(14//5)

(5)**  幂运算
print(2**3)

### 逻辑运算符

- and  or  not  is  isnot（判断是否为同一个对象）
区分is 、= =：is 判断是否为同一个对象（就一个）
- 面试题（is和==；可变、不可变存储方式的理解）
```
arr1 = [1,2,3]
arr2 = arr1
print(arr1==arr2)
print(arr1 is arr2)    # 是同一个（传址，谁可以用这个数组）
arr1 = [1,2,3]
arr2 = [1,2,3]
print(arr1==arr2)
print(arr1 is arr2)    # 不是同一个

a = 10
b = a
print(a==b)
print(a is b)

a = 10
b = 10
print(a==b)
print(a is b)
```
### 关系运算符

- <  <= >  >=  !=   = =

### 位运算符

- ~a 按位取反  a<<n:左移n位  a>>n:右移n位  &：按位与  |: 或运算  ^:异或运算
- 二进制、八进制、十进制、十六进制

print(0b10)   #输出二进制
FFFFFF   每两位表示一个数
FF
F*16^1+F*16^0 = 255
rgb(255,255,255)

~：按位取反
print(~0b10)
print(~10)
原码  反码  补码

a<<n:左移n位    每移一位乘以2（扩大2倍）
print(2<<1)
10 ->  100

&：按位与   （同真为真，有假为假）
print(2&3)
10
11

|: 或运算   （有真为真）
print(2|3)

^:异或运算  (相同为0，不同为1)
print(2^3)

### 赋值运算符

- =  +=  -=  *=  /=  //=   %=  **=
- a = 10
a/=5   #a = a/5
print(a)

a = 10
a //=3   #a = a//3
print(a)

a = 2
a**= 3   #a = a**3
print(a)

### 一元运算符 （del  删除字典）

- 一元运算符   del
arr = [1,2,3]
del arr
print(arr)

### 三元运算符

- 三元运算符
a,b = 10,20
print("a>b")if a>b else print("b>a")

## 流程控制

### 扩展：random 常用方法

import  random

* 1.  random：生成0到1之间的随机浮点数
print(random.random())
* 2.  uniform(a,b)：生成a到b之间的随机浮点数
print(random.uniform(1,100))
* 3.  randint(a,b)：生成a到b之间的随机整数，闭区间即包括b
print(random.randint(1,100))
* 4.  randrange()：在某个范围内生成一个随机数
print(random.randrange(2))
* 5.  choice()：随机选取序列中的某一个元素
arr = [1,2,4,2,5,6,4,7,3,100,258]
print(random.choice(arr))
fruits = {"apple", "banana", "cherry"}
print(random.choice(fruits))
* 6.  sample()：随机选取序列或集合中的指定个数的元素，返回一个列表
arr = [1,2,4,2,5,6,4,7,3,100,258,99,65,74]
print(random.sample(arr,4))
fruits = {"apple", "banana", "cherry"}
print(random.sample(fruits,2))
* 7.  shuffle()：洗牌，打乱顺序
arr = [1,2,3,4,5,6,7,8,9,22,66,'fgd','dcx']
random.shuffle(arr)
print(arr)

### 分支（必须写内容）

-  if
 a,b=10,20
 if a>b:
     print("a>b")
 elif a==b:
     print("a=b")
 else:
     print("a<b")

 pass   占位
"""
if(a>b){
}
"""

### 循环

（1）for
range()序列
for i in range(1,11):
    print(i)

（2）while
a1,b1=10,20
while a1<b1:
    print(a1)
    a1+=1

for 与 while
是否明确循环次数

(3)干预循环

- 列表推导式

	- 列表推导式
"""
js中：
let arr = []
for(let i=0;i<11;i++){
    arr.push('a')
}
"""

arr = [i for i in range(1,10)]
arr = ['a' for i in range(1,10)]

- 列表转字符串
列表转字符串   jion把列表里的所有字符串进行拼接

print(",".join(['1','2','3','4']))

99乘法表
arr = "\n".join(["".join(['%s*%s=%s '%(j,i,j*i)for j in range(1,i+1)]) for i in range(1,10)])
print(arr)

## 函数

### 定义

- 将特定功能的代码进行封装，以便重复利用

### 优点

- 使程序更加简单
- 逻辑性更强
- 调用更方便
- 维护起来更加容易

### 语法

- ## 一、语法

def 函数名（形参）：
    函数体
    return [value]

#### 语法注意

- 函数相对于del关键字必须保持一定的空格缩进

#### 调用

"""
函数名（实参）
"""

### 参数形式

- 必选参数（不写就错）

	- def fn(name):
    print(name)
fn()       # TypeError

- 缺省参数 (必选参数和默认参数的顺序不可调整，默认第一个形参)

	- def fn(name,sex='男'):
    print(name,sex)
fn('wss')     # 换位置会出现SyntaxError

- 可变参数

	- def fn(name,sex='男',*cj):
    print(name,sex,cj,type(cj))
fn('wss','男',12,34,45)

- 关键字参数

	- def fn(name,sex='男',*cj,**attr,):
    print(name,sex,cj,attr,type(attr))
fn('wss','男',12,14,34,56,height=180,weight=100)


- 传参的顺序：必选参数、默认参数（缺省参数）、可变参数、关键字参数
- 特殊用法：万能参数

	- def fn(*args,**kwargs):
    print(args,kwargs)
fn(12,3445,2244,age='18',name='wss')

- 解构用法   加一个*，解构出来    加一个**，解构出来
```
def fn(a,b,c,d):
    print(a,b,c,d)
arr = [1,2,3,4]
fn(*arr)

def fn(name,age,sex):
    print(name,age,sex)
dict1 = {'name':'wss','age':18,'sex':'男'}
fn(**dict1)     #  fn(name='wss',age=18,sex='男')  也可  fn(name='wss',sex='男',age=18)   使用键值形式可以不遵循顺序
```
### 返回值

- return

	- def fn():
    return 1,2,3
print(fn())     #返回值不可以是多个，如果有多个返回值，默认为元组
	- return作用:返回并终止函数
return注意：
    
		1、可以写多个return语句，最终只有一个被执行
    	
		2、不能在return语句之后书写代码
    	
		3、return只能返回一个数据，如果想返回多个数据必须为list/tuple/dict
a,b,c=fn()
print(fn(1,2,3))   #1,2,3

### 例子（ 斐波那契数列）

（1）输出第几个斐波那契数列的值
def f(n):
    a,b=1,1
    if n==1 or n ==2:
        return 1
    else:
        i=3
        while i<=n:
            a,b=b,a+b
            i+=1
        return b
print(f(int(input("输入一个数："))))

（2）输出斐波那契数列  （yield）
def fab(max):
    n, a, b = 0, 0, 1
    while n < max:
        yield b
        a, b = b, a + b
        n+=1
for i in fab(10):
    print(i)

### 高阶函数

- 实参高阶函数

	- 把函数名当作参数传递给另一个函数

- 返回值高阶函数

	- 返回值中包含函数名

		- 1 普通写法
		
		加法运算
		```
		def fn(a,b,c):
			return a+b+c
		print(fn(1,2,3))
		```
		### 柯里化写法
		```
		def fn(a):
			def fn1(b):
				def fn2(c):
					return a+b+c
				return fn2
			return fn1
		print(fn(10)(20)(30))
		```
### 匿名函数  lambda

- 语法

	- lamdba   参数1，参数2，..:函数体

- 调用

	- 自调用
		- print((lambda a,b:a+b)(10,20))

	- 作为回调函数进行使用

		高阶函数中作为参数
```
def fn1(a):
    return lambda  b: lambda c:a+b+c
print(fn1(10)(20)(30))
```
		赋值
```
		-  fn = lambda a,b:a+b
 print(fn(10,20))
```
### 局部变量与全局变量

- global: 顶层全局变量 
```
	- a = 123
def fn():
    global a     # 声明成全局变量
    a = 456
    print(a)
fn()
print(a)
```
- nonlocal：不是局部也不是全局，必须在嵌套函数中使用
（嵌套函数中的上层变量）
```
	- a = 123
def fn1():
    a = 456
    def fn2():
        nonlocal a     # 不是局部
        a = 789
        print(a)
    fn2()
    print(a)
fn1()
print(a)
```
### 作用域

- 命名空间
- python的四个作用域LEGB
- 作用域搜索顺序

	- python作用域搜索顺序遵循LEGB规则

### 闭包函数

- 在一些语言中，在函数中可以（嵌套）定义另一个函数时，如果内部的函数引用了外部的函数的变量，则可能产生闭包。闭包可以用来在一个函数与一组“私有”变量之间创建关联关系。在给定函数被多次调用的过程中，这些私有变量能够保持其持久性

### 递归函数

- 如果一个函数在内部不调用其它的函数，而是自己本身的话，这个函数就是递归函数。

### 装饰器

- 定义

	- 装饰器实际上就是为了给某个程序增加功能

- 使用场景

	- 定义公式：<函数+实参高阶函数+返回值高阶函数+闭包函数+语法糖=装饰器>
	- 比如该程序已经上线或者已经被使用，那么久不能大批量地修改源代码，这样是不科学也是不现实的。

- 装饰器三原则

	- 不能修改被装饰函数的源代码
	- 不能改变被装饰函数的调用方式
	- 满足1、2的情况下给程序增加功能

- 添加新功能：输出总时间

	- import time 
```
def fn():   #所有的函数必须放在前面 ；定义好了写到内存中，没执行
    time.sleep(1)
    print("end..")
 fn()

方式一
def fn2(fn1):    # 局部的fn1  调用完fn2应该注释掉内部的变量
    def newFn():
         start = time.time()
        fn1()    # 函数的闭包，内层函数使用外层变量fn1
		         end = time.time()
        print("总时间：%s"%(end-start))
     return newFn    # 返回newFn给fn2，相当于此时的fn2就是newFn了；注意这里不是返回newFn()
 fn = fn2(fn)    # 开始的fn是全局的fn作为实参给fn2，执行将newFn给fn2，把原来上边的fn覆盖了而存储成了newFn，然后再把fn2赋给此刻的fn
 fn()
```
#### 方式二：装饰器语法
```
# def fn2(fn1):
#     def newFn():
#         start = time.time()
#         fn1()
#         end = time.time()
#         print("总时间：%s"%(end-start))
#     return newFn

# @fn2
# def fn():
#     time.sleep(1)
#     print("end..")

# @fn2
# def fn1():
#     print("abc")

# fn()
# fn1()
```
- 装饰器的传参

	- 原函数传参
```
		- def fn2(fn1):
    def newFn(*args,**kwargs):
        start = time.time()
        fn1(*args,**kwargs)   # 解构一下
        end = time.time()
        print("总时间：%s"%(end-start))
    return newFn

@fn2
def fn(name):
    time.sleep(1)
    print("my name is %s"%name)

fn("wss"
```
	- 装饰器传参
```
		- def fn2(funName):
    def argsfn(fn):
        def newFn(*args,**kwargs):
            print("这是装饰(%s)函数"%funName)
            start = time.time()
            fn(*args,**kwargs)   # 接收参数
            end = time.time()
            print("总时间：%s"%(end-start))
        return newFn
    return argsfn

@fn2('fn函数')
def fn(name):
    time.sleep(1)
    print("my name is %s"%name)

fn("wss")
```
- 装饰器嵌套

```
@fn2()
@fn1()
def fn():
    pass
"""

		- # 定义@fn1装饰器：输出装饰器名字
def fn1(funName1):
    print("%s在执行装饰器"%funName1)
    def newFun(fn):
        def newFun2(*args,**kwargs):
            print("%s在调用"%funName1)
            fn(*args,**kwargs)
        return newFun2
    return newFun

# @fn2装饰器  输出装饰器的名字
def fn2(funName2):
    print("%s在执行装饰器" % funName2)
    def newFun(fn):
        def newFun2(*args,**kwargs):
            print("%s在调用"%funName2)
            fn(*args,**kwargs)
        return newFun2
    return newFun

@fn2("fun2")
@fn1("fun1")
def fn(name):
    print(name)

fn("wss")
```
了解装饰器运行流程: 装饰器执行是按照从上到下执行

- 装饰器高级

	- 类装饰器

## Python网络爬虫

### 概述

- 定义

	- 网络爬虫（又称为网页蜘蛛，网络机器人，在FOAF社区中间，更经常的称为网页追逐者），是一种按照一定的规则，自动地抓取万维网信息的程序或者脚本，另外一些不常使用的名字还有蚂蚁、自动索引、模拟程序或者蠕虫。

- 分类

	- 通用爬虫

		- 百度搜入：爬取，搜索排名，为了更好检索内容、更好地获取关机键   搜索引擎优化

	- 聚焦爬虫

		- 猎头：爬取简历进行推荐，把用户的有价值的数据爬取下来了；正常公开免费的数据可以获取

- 工作流程

	- 1.设置爬取地址，设置请求头（导航，嵌套爬取）
	- 2.解析页面，获取需要信息（分析页面）
	- 3.数据存储（mysql、表格、其他数据库比如基于内存存储的数据库）

- Robots协议

	- Robots协议（也称为爬虫协议、机器人协议等）的全称是"网络爬虫排除标准"（Robots Exclusion Protocol），网站通过Robots协议告诉搜索引擎哪些页面可以抓取，哪些页面不能抓取。
	- Robots协议：https://www.taobao.com/robots.txt

- 常用工具

	- Builtwith  识别网站所用技术

		- import builtwith
print(builtwith.builtwith('https://www.wordpress.com'))

	- whois  查询网站所有者的工具
	- uriilb.robotparser  解析robots.txt工具

### HTTP概述

- http协议

	- HyperText Transfer Protocol, 超文本传输协议

- https

	- Hypertext Transfer Protocol over Secure Socket Layer
HTTP下加入SSL层，HTTPS的安全基础是SSL，HTTPS的安全基础是SSL，因此加密的详细内容就需要SSL。

- 区别

	- HTTPS存在不同于HTTP的默认端口及一个加密/身份验证层（在HTTP与TCP之间）
	- HTTPS广泛用于万维网上安全敏感的通讯，例如交易支付方面
	- HTTP端口号：80；HTTPS端口号：443

- 客户端HTTP请求（带上请求头，证明）
先请求DNS服务器，把ip地址请求到，才能知道请求的是哪台电脑
还要带上一些请求头，

	- 请求报头
客户端带一些信息给服务器

		- Host（主机和端口号）

			- http://118.190.150.35:9000/login

		- Connect（链接类型）：keep alive 长连接，不需要每次都去请求
		- User-Agent（浏览器名称）

			- 使用fake_useragent包

				- from fake_useragent import UserAgent

ua = UserAgent()      # 实例化出来
headers={
    "User-Agent" :ua.random
}

		- Accept（接收传输文件类型）
	
			- */* 什么都可以接收
image/gif 希望接收GIF图像格式的资源
text/html 表明客户端希望接收html
text/html,application/xhtml+xml;q=9,image/*;q=0.8
支持html文本、xhtml和xml文档、所有的图像格式资源，q为权重(0<=q<=1)默认为1（规定分号前面的内容），越靠近1表示越希望";"之前的内容，为0 不希望的类型
```
	 Referer（页面跳转处）

		- 表明产生请求的网页来自于哪个URL

	 Accept-Encoding（浏览器接受文件编码格式）
	 Accept-Language（浏览器接受语言种类）
	 Accept-Charset（浏览器可接受字符编码）
	 Cookie（浏览器本地Application中）
	 Content-Type（POST请求中数据的数据类型）
```
*  响应报头

		 Cache-Control：must-revalidate，no-cache，private

		 服务器不希望客户端缓存资源，下次必须重新请求
Cache-Control：max-age=86400
在86400秒的时间内，客户端可以从缓存中读取资源

- Connection：keep-alive

	- 告诉客户端服务器的tcp连接也是一个长连接，客户端可以继续使用这个tcp链接发送http请求

- Content-Encodeing：gzip

	- 告诉客户端服务端发送的资源时采用gzip编码的

- Content-Type：text/html;charset=UTF-8

	- 告诉客户端资源文件类型还有字符编码

- Date：Sun，21 Sep

	- 服务器发送资源时间

- Expires:Sun...

	- 告诉客户端在这个时间内，可以直接访问缓存副本

- Pragma：no-cache与Cache-Control
- Server 服务器信息
- Transfer-Encoding:chunked

	- 告诉客户端，服务器发送的资源的方式是分块发送的

- Vary：Accept--Encoding

	- 告诉缓存服务器，缓存压缩文件还是非压缩文件

* 响应状态码
```
100~199  服务器成功接收部分请求，需要客户端继续提交其余请求
200~299  服务器成功接收请求并已完成整个处理过程
200  请求成功
300~399  为完成请求，客户需要进一步细化请求
307  304   使用缓存资源
400~499 客户端请求有错误
404  无法找到页面
403  服务器拒绝访问
500~599  服务器端出现错误
500  请求未完成
```
### 数据获取

- 数据采集

	- urllib包  （包里有丰富的API）

		- 概述

			- uillib是一个收集了多个使用URL的模块的软件包

		- 组件

			- request：打开和阅读url地址的包
urllib.request

				- urlopen

			- error：包含 urllib.request 抛出的异常
urllib.error
			- parse：用于处理 URL
urllib.parse

				- 编码转换

					- parse.urlencode({}）
					- quote("太原"）

						- 把汉字转换为编码

				- urlparse(url)

					- 解析url各个部分

			- robotparser：用于解析 robots.txt 文件
urllib.robotparser

		- 响应类型为json

			- json.loads(str)      将 str 转换为 dict
			- json.dumps(dict)     将 dict 转换为 str

	- requests包
通过urllib底层实现
（在urllib的基础上进行更好的封装）

		- http://docs.python-requests.org/zh_CN/latest/
index.html

		- GET请求

			- get(URL,params,headers,timeout)

				- res = requests.get('www.baidu.com')   响应一个地址
				- res.text  查看响应内容
res.content  字节流
res.url  完整的地址
res.encoding  响应字符编码
res.status_code  响应码

		- POST请求

			- post(URL,data,header={})

				- data={}
				- res.text
res.json()  显示json

		- 代理

			- proxies = {"http":"http：//12.34.56.79:9527"}
response = response.get("http://www.baidu.com",proxies = proxies)

				- proxie = {
        'http':'http://%s'%ip,
        'https': 'https://%s'%ip,
    }
				- requests.get('http://wwww.baidu.com',proxies=proxie,timeout=10)     # 请求百度，测试ip地址是否可用

			- 本地配置代理

				- export HTTP_PROXY="http://12.34.56.79.9527"
				- export HTTPS_PROXY="https://12.34.56.79.9527"

		- cookie和session（保存在浏览器的数据）

			- 包中利用cookie以及session来实现登录
			- 子主题 4
			- 日报实例

				- 日报系统中找到学生id
可以在布局里找，也可以在updatecontent里找，就是提交两次可以出现。
			- 获取cookie

				- res = sess.post("http://118.190.150.35:9000/login",data=data)
coo = sess.cookies
cookiesDict = requests.utils.dict_from_cookiejar(coo)
print(cookiesDict)

		- 处理HTTPS请求SSL证书验证

			- response = requests.get("https://www.baidu.com/",verify=True)
			- 跳过验证 verify=False （默认）

	- fake-useragent  工具

		- 安装  pip install fake-useragent import User Agent
		- 使用

			- ua=User Agent（）
			- ua.ie
			- ua.firefox
			- ua.chrome
			- ua.random

	- Selenium（浏览器测试）

		- 概述

			- Selenium是一个web的自动化测试工具，最初是为网站自动化测试而开发的，类型像我们玩游戏时用的按键精灵，可以按指定的命令自动操作，不同的是Selenium可以直接运行在浏览器上，它支持所有主流的浏览器（包括PhantomJS这些无界面的浏览器）

				- js，把页面滚动到底部

		- 中文文档

			- https://selenium-python-zh.readthedocs.io/en/latest/installation.html

		- 安装

			- pip install selenium 

		- 常用组件

			- webdriver

				- 操作步骤

					- 导入 from selenium import webdriver
					- driver.get("http://118.190.150.35:9000/login")

					- 操作数据
					- drive.quit()  关闭浏览器

				- 详细操作

					- 获取页面元素

						- driver.find_element_by_id('loginForm') #通过ID获取元素

* driver.find_element_by_name('continue') #通过name属性获取元素

* driver.find_element_by_xpath("//form[@id='loginForm']/input[4]") #通过XPath查找元素
	 driver.find_element_by_link_text('Continue')	#通过链接文本获取超链接

* driver.find_element_by_partial_link_text('Conti')
* driver.find_element_by_tag_name('h1') #通过标签名查找元素
* driver.find_element_by_class_name('content') #通过Class name 定位元素
* driver.find_element_by_css_selector('p.content') #通过CSS选择器查找元素

#### 事件

##### 步骤
```
from selenium.webdriver import ActionChains

# 导入 ActionChains 类
loginbtn = driver.find_element_by_partial_link_text("登") 
# 获取元素
action = ActionChains(driver)
# 创建对象
action.click(loginbtn)
# 填写事件
action.click(loginbtn).perform()  
# 执行事件
click()  单击
double_click()  双击
context_click(ac)  右击
click_and_hold()  按下
drag_and_drop(e1,e2)  将元素e1移动到e2
drag_and_drop_by_offset(e1,x,y)  将元素移动位置
release(e)  释放鼠标按钮
pause(num)  停几秒
send_keys(con)  将con发送到当前聚焦元素
send_keys_to_element(ele,con)  将con发送到元素
```
#### 下拉框处理

##### 步骤

	弹窗处理
	
	alert = driver.switch to alert()  获取弹框内容
	
	页面切换
	
	driver.switch_to_alert()  获取弹窗内容
	for handle in driver.window_handles:
	driver.switch_to_window(handle)
	
	页面前进和后退
	
	driver.forward()  #前进
	driver.back()  #后退
	
	Cookies

#### 组件

* etree（文档树）

	HTML初始化生成一个XPath解析
	tostring（html，encoding=''）
	xpath() 通过获取路径来获取资源

* re  正则

	- 概述

		用来描述或者匹配一系列符合某种规则得字符串的表达式
		（输入用户名密码，长度不够，特殊符号，怎样知道输入的格式对不对）

	- 正则表达式

		- 元字符
		- 原子表
		- 数量
		```
			* 0个或多个
			+ 1个或多个
			？ 0个或者1个
			{n}n个
			{n，}n个或多个
			{n，m}n个到m个   贪婪
		```
```
res = re.findall(r"\w*","this is div")
res = re.findall(r"\w+","this is div")
res = re.findall(r"\w?","this is div")
res = re.findall(r"an?","this is a an div")     # 后边的n可有可无
res = re.findall(r"</?div>?","<div>this is div</div>")      # / 可有可无
res = re.findall(r"\w{2}","abcdefg")
res = re.findall(r"\w{2,3}","this is div")      # 贪婪特点：尽可能多
res = re.findall(r"\w{2,}","this is div")       # 贪婪： 选择全部
print(res)
```
其他
^  以什么开始
$   以什么结束


### re 模块

* re常用函数

	re.match(pattern,string,flags=0)

	- pattern  正则表达式
	* steing  要匹配的字符串
	* flag  模式
	
	尝试从字符串的起始位置匹配一个模式，如果不是起始位置匹配成功的话，
	成功返回正则对象
	```
	group(num=0)
	groups()
	```
	re.search(pattern,string,flags=0)

	* pattern  正则表达式
	* steing  要匹配的字符串
	* flag  模式
	
	re.search() 扫描整个字符串并返回第一个成功的匹配
	成功返回正则对象

		group(num=0)
		groups()

	re.sub(pattern,repl,string,count=0,flags=0)

	* pattern  正则中的模式字符串
	* repl  替换的字符串也可为一个函数
	* string  要被查找替换的原始字符串

	count  模式匹配后替换的最大次数，默认0，表示替换所有的匹配

#### sub  替换函数
```
# res = re.sub("山西","陕西","山西优逸客","陕西",1)
# def fn(a):
#     res = str(int(a.group())*2)
#     return res
#
# res = re.sub("\d+",fn,"山西优逸客 就业人数1000 高薪就业900")
# print(res)
```

re.compile(pattern[,flags])

* pattern  一个字符串形式的正则表达式
* flags  可选，表示匹配模式

re.findall(string[,pos[,endpos]])

* 在字符串中找到正则表达式所匹配的所有子串，并且返回一个列表，如果没有找到匹配的，则返回空列表。
* string  待匹配的字符串

pos  可选参数，指定字符串的起始位置，默认为0

endpos  可选参数，指定字符串的结束位置，默认为字符串的长度

re.finditer()

* 返回一个迭代器。可以循环的、一次性输出

re.split(pattern,string[,maxsplit=0,flags=0])

* pattern  匹配的正则表达式
* string  要匹配的字符串
* maxsplit  分割次数
* flags  标志位

#### split 拆分函数
```
# rege = re.compile('[;,.]')     # 正则表达式,变成原子表
# res5 = rege.split('a;b,c.d')
# res5 = re.split('[;,.]','a;b,c.d')
# print(res5)
```
#### 匹配模式

- re.I  忽略大小写

- re.L  表示特殊字符集 \w , \W,  \b ,\B, \s ,\S 依赖于当前环境
- re.M  多行模式
- re.S  使特殊字符匹配任何字符，包括换行，如果没有此标志，将匹配任何内容除换行符
- re.X  此标志允许编写正则表达式，看起来更好。在模式中的空白将被忽略，除非当在字符类或者前面非转义反斜杠和当一条线包含一个# ，既不在字符类中或由非转义反斜杠，从最左侧的所有字符之前，这种# 通过行末尾将被忽略。
```
# rege = re.compile('[a-z]',re.I)        # re.I忽略大小写
# res = rege.findall("absdhoashODISAHNO")
# print(res)

# rege = re.compile("""[a-z] # 字母""",re.X)
# res = rege.findall("""
# absdhoashODISAHNO
# hfadshfi
# """)
# print(res)
```

### 数据存储

- Mysql
- redis
- 文件存储



### Scrapy框架

- 概述

### 常见反爬策略

- 构造合理请求头

	- Accept
	- User-Agent

		- 第三方库

	- Referer
	- Accept-Encoding
	- Accept-Langukage

- 检查网站生成的Cookie

	- editthiiscookie

- 动态内容获取
- 限制爬取速度
- 处理验证码

	- 超级鹰/云大码

- 隐藏

	- 代理服务

## 模块与包

## 常用系统内建函数

### 		内置函数		
abs()	dict()	help()	min()	setattr()
all()	dir()	hex()	next()	slice()
any()	divmod()	id()	object()	sorted()
ascii()	enumerate()	input()	oct()	staticmethod()
bin()	eval()	int()	open()	str()
bool()	exec()	isinstance()	ord()	sum()
bytearray()	filter()	issubclass()	pow()	super()
bytes()	float()	iter()	print()	tuple()
callable()	format()	len()	property()	type()
chr()	frozenset()	list()	range()	vars()
classmethod()	getattr()	locals()	repr()	zip()
compile()	globals()	map()	reversed()	__import__()
complex()	hasattr()	max()	round()	 
delattr()	hash()	memoryview()	set()


### 类与对象概述

- 类：类是对象的抽象，比如飞机图纸，月饼模具
- 对象：对象是类的实例，比如飞机、月饼
- 面向对象的三大特点：封装、继承（默认继承object）、多态
- 关系：类是对象的模型，对象是类的具体实例化

### 语法

```
class  类名(基类、父类)
    * 实例属性
    def __int__(self):   # self => this 实例 ;  __int__ => constructor (构造函数)
        self.name='wss'
        self.age = 18
    * 实例方法
    def say(self):
        print(self.name)
```
```
# class Person:
#     def __init__(self,name='wss',age=18):
#         self.name= name
#         self.age = age
#     def say(self):
#         print("my name is %s"%self.name)
#     def a(self):
#         print("I am %s years old"%self.age)
# # 实例化，创建对象
# xm = Person('小明',17)
# xm.say()
# xm.a()
```

### 案例

- 案例一：时钟
```
## 创建一个时钟类
# 属性  小时:分钟:秒钟
# 方法
# run  表跑起来
# set  设置时间
# print（obj）  输出现在的时间
# class Clock:
#     def __init__(self,hou=0,min=0,sec=0):     # 魔法方法
#         self.hou = hou
#         self.min = min
#         self.sec = sec
#     def __str__(self):    # 对实例的描述  print(obj) 打印 __str__()魔法方法的返回值
#         return '%0.2d:%0.2d:%0.2d'%(self.hou,self.min,self.sec)
#     def run(self):
#         while True:
#             print(self)
#             time.sleep(1)   # 阻塞代码
#             self.sec += 1
#             if self.sec>59:
#                 self.min+=1
#                 self.sec=0
#                 if self.min>59:
#                     self.hou+=1
#                     self.min=0
#                     if self.hou>23:
#                         self.hou=0
#
#
# c1 = Clock(0,0,0)
# c1.run()
```
- 案例二：烤地瓜

####  创建一个烤地瓜类
```
# 属性：
# cookedLevel：这是数字；0~3表示还是生的，超过3表示半生不熟，超过5 表示已经烤好了，超过8表示已经烤成了木炭！地瓜刚开始的时候是生的。
# cookedString：这是字符串；描述地瓜的生熟程度
# condiments:这是地瓜的配料表，比如番茄酱、芥末酱
# 方法：
# cook() 把地瓜烤一段时间
# addCondiments() 给地瓜添加配料
# __init__() 设置默认属性
# __str__() 让print的结果看起来更好一些
```
```
class Potato:
    def __init__(self,cookedLevel=0,cookedString='生',condiments='番茄酱'):
        self.cookedLevel = cookedLevel
        self.cookedString = cookedString
        self.condiments = condiments
        self.condimentsList = ['芥末酱','番茄酱','甘梅酱']
    def __str__(self):
        return '您好，这是您的%s口味的%s的地瓜'%(self.condiments,self.cookedString)
    def cook(self,min):
        # while True:                    # 没有这行代码，结果打印一行
        #     time.sleep(1)                     # 阻塞代码
            self.cookedLevel += min             # 每秒加一
            if self.cookedLevel>=0 and self.cookedLevel<4:
                self.cookedString = '生'
            elif self.cookedLevel<6:
                self.cookedString = '半生不熟'
            elif self.cookedLevel<8:
                self.cookedString = '可以享用了'
            elif self.cookedLevel>=8:
                self.cookedString = '糊巴了'
    def addCondiments(self,num):
        self.condiments = self.condimentsList[num]

# 客户来了
p1 = Potato()
p2 = Potato()
p3 = Potato()
p4 = Potato()

p1.cook(2)
p2.cook(5)
p3.cook(7)
p4.cook(9)

p1.addCondiments(0)
p2.addCondiments(2)
p3.addCondiments(1)
p4.addCondiments(2)

print(p1)
print(p2)
print(p3)
print(p4)
```

#### 类变量（类可以使用的属性）与实例变量（实例可以使用的属性）


类变量：定义在类中，可以被类方法（修改），可以被实例访问
实例变量：实例变量只能实例调用，且权重大（优先级大），它是后写的，可以把之前的内容覆盖掉

- 案例
```
# class P:
#     sex = '男'       # 类变量，能够被实例继承（图纸）
#
#     def __init__(self):
#         self.name = 'xm'        # 实例属性，实例变量
#         self.sex = '男'          # 实例变量只能实例调用，且权重大（优先级大），它是后写的，可以把之前的内容覆盖掉
#
#     @staticmethod  # 静态类方法，什么都不能调用，就是一个普通的公共函数功能， 连指针都没有
#     def say2():
#         print("this is static")
#
#     @classmethod        # 类方法，可调用类变量
#     def setSex(cls,sex):
#         print(cls.name)
#         cls.sex = sex
#
#     def say1(self):      # 实例方法，可调用实例的方法和属性，还可以调用继承过来的类变量
#         print(self.name)
#         print(self.sex)


# xm = P()
# # xm.sex = '女'        # 创建了实例属性（实例对象），给实例重新赋予属性
# P.sex = '女'       # 所有的实例用的都是同一个类变量
# print(xm.sex)       # 类变量可以被实例调用，实例变量与类变量重名时，优先调用实例变量
# print(P.sex)        # 类变量也可以被类调用

# xh = P()
# xh.say1()
# xh.say2()

# xm = P()
# print(xm.name)
# print(xm.sex)   # 小明的sex继承的类变量
# P.setSex('女')   # 调用类方法，修改类变量
# print(xm.sex)
# xm.setSex('男')     # xm这个实例调用了继承的类方法，修改了类变量
# print(xm.sex)
# xm.sex = '女'    # 添加了实例属性sex，覆盖了继承来的类变量sex，并没有修改了类变量
# print(xm.sex)
# print(P.sex)
```
### 静态类方法、类方法、实例方法

- 静态类方法

	- @staticmethod

- 类方法

	- @classmethod

- 实例方法

### 私有属性和私有方法

- __spam

	- 所谓私有，就是在外部不能调用，方法之间可以使用的私有方法以及属性需要在方法名或属性名前加"__",但是python中没有真正的私有方法、私有属性
```
# class P():
#     def __init__(self,name,age):
#         self.__name = name
#         self.__age = age
#     def say(self):
#         print("my name is %s"%self.__name)      #内部可以使用__name
#
# p = P('小红',19)
# print(dir(p))
# p.__name = "肖红"     # 外部不可使用__name
# p._P__name = "肖红"       # 君子协议，但是可以强制改
# p.say()
```
### 装饰器

- @property 私有：将方法改成一个同名的属性，这个属性不能修改（因为就没有这个属性，只能看）
```
# class P():
#     def __init__(self,name,age):
#         self.__name = name
#         self.__age = age
#     def say(self):
#         print("my name is %s"%self.__name)
#
#     @property       # 装饰器
#     def name(self):
#         return self.__name
#
# p = P('小红',19)
# print(dir(p))
# p.name = "1234"   # 只能让外部看，不能修改（比如，血量，枪，金币）
# print(p.name)
```
- 类装饰器
```
	- def MyClass(obj):
    obj.age = 19        # 类变量
    obj.say = lambda cls:print(cls.age)     # 类方法
    return obj

@MyClass
class P:
    def __init__(self,name):
        self.name = name
class A:

p = P("小红")
print(dir(p))
```
- 实例方法装饰器
```
	- import time

def sumtime(fn):
    def newFn(self,*args,**kwargs):
        start = time.time()
        fn(self,*args,**kwargs)
        end = time.time()
        print("%s你好帅"%self.name)
        print("总时间：%s"%(end-start))
    return newFn
```
#### 实例方法装饰器
```
class P:
    def __init__(self,name):
        self.name = name
    @sumtime
    def run(self):
        time.sleep(1)
        print(self.name)

p = P("wss")
p.run()
```
### 继承与多重继承

- 宗旨：深度优先、从左至右

	- 继承
```
# class Y:
#     def __init__(self):
#         self.tool = "石头"
#     def run(self):
#         print("直立行走")
#
# class P(Y):
#     def __init__(self):
#         super().__init__()    # super 相当于this指针，用来引用父类而不必显式地指定它们的名称
#         self.cloth = ""
#     def say(self):     # 派生出来的新方法
#         print("沟通交流")
#
# p1 = P()
# print(dir(p1))
# p1.say()
```
#### 多重继承：从左至右，深度优先（python3）
```
# class A:
#     def __init__(self):
#         pass
#     def run(self):
#         print("A")
#
# class B:
#     def __init__(self):
#         pass
#     def run(self):
#         print("B")
#
# class C(A):
#     def __init__(self):
#         pass
#     def say(self):
#         print("C")
#
# class D(B):
#     def __init__(self):
#         pass
#     def say(self):
#         print("D")
#     def run(self):
#         print("D->run")
#
# class F(C,D):
#     def __init__(self):
#         pass
#
#
# print(dir(C))
# print(dir(D))
# f = F()
# f.say()     # 从左至右
# f.run()     # 从上到下,深度优先
```
		- 多重继承
		- # 多重继承：从左至右
```
# class Car():
#     def __init__(self):
#         self.pp = ""
#         self.color = ""
#     def run(self):
#         print("启动")
#
# class FT(Car):
#     def __init__(self):
#         super().__init__()  #super 相当于this指针，用来引用父类而不必显式地指定它们的名称
#         self.type = ""
#
# class HG(FT):
#     def __init__(self):
#         super(HG,self).__init__()
#         self.price = ""
#
# hg1 = HG()
# print(dir(hg1))

### super()
```
- super 相当于this指针，用来引用父类而不必显式地指定它们的名称

### 魔法方法

- __slots__  限制Class属性和方法
```
# class P:
#     """
#     Person类    人类
#     """
#     def __init__(self):
#         pass
#     __slots__ = ['name','sex']
#     __name__ = "Person"
#     def run(self):
#         print(self.__doc__)
#
# p = P()
# P.name = "wss"
# p.sex = "男"
# # p.age = 18
# print(dir(p))
# print(p.__doc__)
```
- __name__   类名字
-  print(self.__doc__)  类文档字符串、开头注释
```
# 拿到函数的注释
# def fn():
#     """
#     this is fn
#     :return:
#     """
#     pass
# print(fn.__doc__)
```
- __new__  与  __init__  关系

	- __new__   ：第一步、创建一个对象，必须有返回值。把实例创建出来，可能任何属性都没有
	- __init__    ：第二步、给实例初始化，赋予属性

- __str__   给实例一个描述
- __del__   实例注销时调用


#### 验证

- ifinstance（）来检查一个实例的类型

	- print(isinstance(obj，class))  验证obj是否为class的实例

- lssubclass（）来检查类的继承关系

	- print(issubclass(P,A))

- type（）查看类型
dir（）获取对象的属性和方法

### 文件操作

#### 操作文件的步骤

- 1、打开文件
2、操作文件（读写）
3、关闭文件

#### open（）函数的用法

- open(文件路径，打开模式（读、写、读写、二进制、普通内容）)  打开文件
```
file 文件路径
mode 读取模式：
     r: 读取文件内容
     r+：读写，从头覆盖旧内容，没有文件则报错
     w: 每次都重新写入，路径不对会创建新文件
     w+：读写，路径不对会创建新文件
     a：追加，路径不对会创建新文件
     a+：读，追加
     rb、rb+、wb、wb+、ab、ab+   以二进制的方法处理
```
encoding 字符编码  

errors(出错处理机制)

strict(默认)

ignore(忽略)



#### 读文件

- f.read([num])

	- num代表字符的数量，默认为全部

- f.readline([num])

	- 文件读取每一个行，通过\r \n EOF (文件结束标识) 来区分每一行,num代表输出的字符

- f.readlines()

	- 读取每行内容，以列表的形式输出

#### 写文件

- f.write(str)

	- 每次都重新写入，路径不对会创建新文件

- f.writelines()

	- 读写，路径不对会创建新文件

#### 操作指针

- f1.seek(p,0)

	- 每个uincode码，3个字节。移动文件指针到第p个字节

- f1.seek(p,1) 

	- 相对于当前位置往后移p（文件以二进制方式打开）

- f1.seek(-2,2)

	- 文件尾之后的p个字节(负值就是倒着往回)  （文件以二进制方式打开）

- f.tell()

	- 返回文件读取指针的位置

#### 关闭文件

- f.close()

	- 1、把缓存区的内容写到硬盘  2、关闭文件

- f.flush()

	- 把缓冲区的内容写到硬盘

### pickle持久化（写到硬盘中）

- import pickle
```
 # pickle.dump(obj,file)       # 把obj存储到file文件中
 # pickle.load(obj,file)     # 把file文件中的数据进行读取
 # f = open("./day04.txt",'rb+')
 # obj = [1,2,3,4,5,6,7,8,9]
 # pickle.dump(obj,f)    # 把obj存储到file文件中
 # obj = pickle.load(f)        # 把file文件中的数据进行读取
 # print(obj)
 # f.close()
```

### 异常
定义：

  * 因为程序出现错误而在正常流程控制以外采取措施的行为
  * 当python检测到一个错误时，解释器就无法继续执行了，反而出现了一些错误的提示，这就是所谓的异常
	finally：无论出不出现异常都要执行
```
### ### 文件打开或读取时，可能会发生IORrror异常，可能导致文件无法关闭。出现异常
# try:        # 可能会错误的代码
#     # print(1/0)      # 程序员逻辑错误，水平不够高
#     f = open("day04.txt",'r',encoding="utf-8")
#     con = f.read()
#     print(con)
# except:     # 出错异常执行的代码
#     print("文件出错了")
# except:   异常类 as e:
	  pass
# else:
#		没有发生异常执行的程序
# finally:        # 不管正确还是错误，总会执行
#     # print("finally")
#     f.close()
# 自定义异常
class myError（Excep）
```

### with 上下文管理器
重点：（面试题必问：上下文管理器怎么做到的？)

* 定义：上下文管理器是一个对象，它定义了在执行with语句时要建立的运行时上下文，上下文管理器处理执行代码块所需的运行时上下文的入口与出口，上下文管理器通常使用with语句调用，但是也可以通过直接调用他们的方法来使用）

* 作用：with还可以很好的处理上下文环境产生的异常

* 用途：保存和恢复各种全局状态
		锁定和解锁资源
		关闭打开的文件等
* ——enter——（） with语句将__enter__（）方法的返回值绑定到语句as子句中
* __exit__(ext_type,exc_value,traceback)
* 如果上方没有异常退出，那么所有三个参数都将是none
* __exit__()方法可以处理异常是with语句的强大之处

### 生成器

​	概念：由于受到内存限制，列表容量有限，，为了节省空间，，列表元素通过算法推算出来。一边循环一边计算的机制，称为生成器：generator。

生成器不但可以作用于for循环，还可以被next()函数不断调用并返回下一个值，直到最后抛出StopIteration错误表示无法继续返回下一个值了。

​	generator保存的是算法，每次调用`next(g)`，就计算出`g`的下一个元素的值，直到计算到最后一个元素，没有更多的元素时，抛出`StopIteration`的错误。 

#### 方法

​	send()方法，用于给生成器发送某一信息， 

​	close()方法关闭生成器 

​	next()方法查看元素 

​	创建一个generator：
		第一种方法：只要把一个列表生成式的`[]`改成`()`，就创建了一个generator： 

>>> L = [x * x for x in range(10)]
>>> L
>>> [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
>>> g = (x * x for x in range(10))
>>> g
>>> <generator object <genexpr> at 0x1022ef630>

​	创建了一个generator后，基本上永远不会调用`next()`，而是通过`for`循环来迭代它，并且不需要关心`StopIteration`的错误。

generator非常强大。如果推算的算法比较复杂，用类似列表生成式的`for`循环无法实现的时候，还可以用函数来实现。

​		第二种方法：如果一个函数定义中包含`yield`关键字，那么这个函数就不再是一个普通函数，而是一个generator： 

​	斐波那契数列：

```
def fib(max):
    n, a, b = 0, 0, 1
    while n < max:
        print(b)
        a, b = b, a + b
        n = n + 1
    return 'done'
```



`fib`函数实际上是定义了斐波拉契数列的推算规则，可以从第一个元素开始，推算出后续任意的元素，这种逻辑其实非常类似generator。

也就是说，上面的函数和generator仅一步之遥。要把`fib`函数变成generator，只需要把`print(b)`改为`yield b`就可以了：

```
def fib(max):
    n, a, b = 0, 0, 1
    while n < max:
        yield b
        a, b = b, a + b
        n = n + 1
    return 'done'

```

函数是顺序执行，遇到`return`语句或者最后一行函数语句就返回。而变成generator的函数，在每次调用`next()`的时候执行，遇到`yield`语句返回，再次执行时从上次返回的`yield`语句处继续执行。 

但是用`for`循环调用generator时，发现拿不到generator的`return`语句的返回值。如果想要拿到返回值，必须捕获`StopIteration`错误，返回值包含在`StopIteration`的`value`中： 

```
>>> g = fib(6)
>>> while True:
...     try:
...         x = next(g)
...         print('g:', x)
...     except StopIteration as e:
...         print('Generator return value:', e.value)
...         break
...
g: 1
g: 1
g: 2
g: 3
g: 5
g: 8
Generator return value: done
```

#### 总结：

generator是非常强大的工具，在Python中，可以简单地把列表生成式改成generator，也可以通过函数实现复杂逻辑的generator。

要理解generator的工作原理，它是在`for`循环的过程中不断计算出下一个元素，并在适当的条件结束`for`循环。对于函数改成的generator来说，遇到`return`语句或者执行到函数体最后一行语句，就是结束generator的指令，`for`循环随之结束。

请注意区分普通函数和generator函数，

​	普通函数调用直接返回结果；

​	generator函数的“调用”实际返回一个generator对象；


### 迭代器
* 定义：一次性可以输出多个值的容器

* 可以被next()函数调用并不断返回下一个值、直到出错的对象称为迭代器：Iterator

* 可以直接作用于`for`循环的数据类型有以下几种：
   - 一类是集合数据类型，如`list`、`tuple`、`dict`、	set`、`str`等；
   - 一类是`generator`，包括生成器和带`yield`的generator function。

* 这些可以直接作用于`for`循环的对象统称为可迭代对象：`Iterable`。

* 可以使用`isinstance()`判断一个对象是否是`Iterable（可迭代的）`对象：

* 生成器都是Iterator对象，但list、dict、str虽然是Iterable，却不是Iterator。

* 把list、dict、str等Iterable变成Iterator可以使用iter()函数为什么list、dict、str等数据类型不是Iterator？
	- 这是因为Python的Iterator对象表示的是一个数据流，Iterator对象可以被next()函数调用并不断返回下一个数据，直到没有数据时抛出StopIteration错误。可以把这个数据流看做是一个有序序列，但我们却不能提前知道序列的长度，只能不断通过next()函数实现按需计算下一个数据，所以Iterator的计算是惰性的，只有在需要返回下一个数据时它才会计算。
### 模块与包
模块：python脚本文件

包：模块的集合

包类似于文件夹，模块相当于文件

分类：正规包  命名空间包

正规包：文件夹中包含__init__.py文件

命名空间包：不包含__init__.py文件

正规包与命名空间包区别：
* 命名空间包不受物理位置限制

包的导入顺序：
* re.py先从当前目录寻找包，然后从系统路径中寻找

* sys.path 列表数据，保存的寻址路径，可以i添加自己的路径

四种调用方式：
* from box import aa——> aa.pp()
* import box.aa——> box.aa.pp()
* from box import aa as a
* import box.aa as a

包的导入方式在非主运行包中，可以使用相对路径的方式的导入  . 当前目录  .. 上一级目录











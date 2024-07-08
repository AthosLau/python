# 一、python基础

## 1、注释

```python
# 单行注释

'''
多行注释
'''

"""
多行注释
"""
```



## 2、常量和变量

```python
# 定义常量：
PAI = 3.14
# python中的常量并非不能改变，而是我们约定俗成不要去改变。


# 定义变量：
name = 'athos'
# 变量存储在栈中，存放的是地址的引用，执行堆中的空间，每个变量在堆中，至少有id、type、value三个属性
```



## 3、数据类型

### 3.1 整数：int

```python
# 整数类型的范围可以取无限大，所以非常适合科学计算
# 常用进制表示：
    0b      2进制
    0x      16进制
    0o      8进制
# int() 转为整数类型
    浮点数直接舍弃小数，int(9.9)=9
    布尔类型，int(True)=1, int(False)=0
    字符串，形态相似可以转，否则报错
```



### 3.2 小数：float

```python
float：3.14 或 314e-2相当于 314 * 10的-2次方
```



### 3.3 布尔类型：bool

```python
True		# 非空
False		# null、空值（比如：''、[]、{}...）

# 布尔类型，常用作于条件判断的结果
```



## 4、标识符

```python
# 由数字、字母、下划线组成
# 数字不能开头
# 不能是关键字
```



## 5、命名规则

```python
# 大驼峰：Phone，MyPhone						# 类
# 小驼峰：maxSpeed					
# 下划线：name，my_name		   				# 变量、函数、模块、包
# 混合写：SPEED，MAX_SPEED					# 全局变量
```



## 6、关键字

```python
import keyword
print(keyword.kwlist)
```



## 7、输出：print

```python
print()					# 打印换行
print(end="\n")			# 打印换行

print(内容)			 
# 小括号里，可以放变量、常量、表达式1
# 可以写多个，但要使用逗号隔开
```



## 8、格式化输出

```python
%c      # 字符
%s      # 字符串
%d      # 整数
%f      # 小数，默认6位小数
%.2f    # 带2位小数
\n      # 换行
\t      # tab键

print("姓名：%s\t\t性别：%c\t\t年龄：%d\t\t余额：%.2f" % ('athos', '男', 29, 19.99))
# 输出结果：
姓名：athos		性别：男		年龄：29		余额：19.99
```



## 9、输入：input

```python
password = input("请输入密码：")
print(password)
# 1、input只能接收1个变量，多个输入使用多个input接收
# 2、输入的变量一定是字符串类型
```



## 10、运算符

### 10.1 赋值运算符

```PYTHON
=

# 将等号右边的值赋值给左边
```



### 10.2 算术运算符

```PYTHON
+ - * / // % **

# 字符串和整数相乘，表示字符串重复N次
# 整除//，取商得到的结果是整型
# 和浮点数进行运算，结果一定是浮点数类型
```



### 10.3 复合运算符

```PYTHON
+= -= *= /= //= %= **=

# a += 1 等价 a = a + 1
```



### 10.4 比较运算符

```PYTHON
== != > < <= =>

# 只能做数值的比较
```



### 10.5 逻辑运算符

```PYTHON
and or not

and：两个都要
    True and True 	= True
    True and False 	= False 
    False and True	= False
    False and False = False
or：只要一个满足
	True or True 	= True
    True or False 	= True 
    False or True	= True
    False or False 	= False
not：非、取反
	not True = False
    not false = True
```

```python
Pytho的开发借助了C语言的思想：
由于C语言中没有True、False，它用0和非0表示；
0表示不成立，非0就表示成立
所以结果也会借助于C语言显示值，而不会显示True或者False

# 特殊情况
print(100 and 200)		# 输入结果：200		# 100和200都不是0，相当于True and True,但C语言中没有True，则返回右边的值
print(0 and 200)		# 输入结果：0		# 相当于 False and True，右边不再判断，直接返回左边
print(True and 0)		# 输入结果：0		# 相当于 True and False，返回False对应的值
print(0 and False)		# 输入结果：0		# 当相于 False and True，右边不再判断，直接返回左边 

print(100 or 200)		# 输入结果：100		# 左侧已满足True，右边不再判断，直接返回左边
print(0 or 200)			# 输入结果：200		# 左侧不满足，再去判断右侧，结果返回右侧
print(True or 0)		# 输入结果：True		# 左侧已满足True，右边不再判断，直接返回左边
print(0 or False)		# 输入结果：False	# 左侧不满足，再去判断右侧，结果返回右侧
```



### 10.6 三元运算符

```python
def get_big_num(a, b):
	return a if a > b else b
	
get_big_num(11, 22)
```



## 11、if条件判断

```python
# 单分支
if 条件判断:
	pass


# 双分支
if 条件判断:
	pass
else:
	pass


# 多分支
if 条件判断:
	pass
elif 条件判断:
	pass
elif 条件判断:
	pass
...
else:
    pass


# 嵌套
if 条件判断:
    pass
	if 条件判断:
        pass
    ...
else:
    pass
```



## 12、循环

### 12.1 while循环

```python
while 条件判断:
	pass


# 死循环
while True:
	pass


# 循环嵌套
while 条件判断:
    pass
	while 条件判断:
        pass
```

```python
1、求1-100累加和
2、求1-100之间累加和
3、求1-100之间能被3和7整除的数的所有数的和
4、99乘法表
```



### 12.2 for循环

```python
for 临时变量 in 可迭代对象:
	pass
	
# 可迭代对象：字符串、列表、元组...
# range(10)			0-9
# range(1,10)		1-9
# range(1,10,2)		1,3,5,7,9

for 临时变量 in 可迭代对象:
	...
	for 临时变量 in 可迭代对象:
```



### 12.3 break & continue

```python
break：结束break所在域的整个循环，
continue：结束本次循环，继续下次循环
```



### 12.4 循环中使用else

```pythoN
while 条件判断:
	pass
	break
	pass
else:			# 在上面的循环中，如果是因为调用break而执行结束的，else中的代码不执行。如果没有匹配到break，而是正常结束的，那么会执行else下的代码
	pass
```



## 13、常用函数

```python
id(XXX)				# 查看变量地址引用
type(XXX)			# 查看数据类型
round(XXX)     		# 四舍五入，返回新
del XXX           	# 删除变量，垃圾回收
del(XXX)			# 删除元素
len(XXX)			# 字符长度、列表|元素个数、字典键值对个数
max(XXX)			# 最大值
```



## 14、字符串

### 14.1 定义字符串

```python
str1 = 'www.athoslau.com'
str2 = "www.athoslau.com"
str3 = """www.athoslau.com"""			# 也是多行注释
str4 = '''www.athoslau.com'''			# 也是多行注释
```



### 14.2 下标

```python
str1 = 'www.athoslau.com'

print(len(str1))		# 输出字符长度：16

# 字符串下标从0【左边】开始，对应第一个字符
str1[0]		w
str1[1]		w
...
str1[15]	m
# 字符串下标从-1【右边】开始，对应最后一个字符
str1[-1]	m
str1[-2]	o
...	
str1[-16]	w
```



### 14.3 字符串切片

```python
str[起始:结束:步长]

# 默认步长为1
# 步长为正数，从左往右切
# 步长为负数，从右往左切
# 起始位就是下标
# 结束位，只能取到结束位的前一位

str1 = 'www.athoslau.com'

str1[-4:]			#.com
str1[:3]			# www
str1[3:5]			# .a
str1[2:]			# w.athoslau.com
str1[2:-1]			# w.athoslau.co
str1[1:5:2]			# w.
str1[5:1:-1]		# ta.w
str1[::1]			# www.athoslau.com
str1[::]			# www.athoslau.com 
```



### 14.3 字符串常见操作

```python
str1 = 'www.athoslau.com'

str1.find('.')					# 从左往右边找第一个匹配中的，3
str1.rfind('.')					# 从右往左边找第一个匹配中的，12
str1.count('.')					# 统计字符出现的次数
str1.replace('athos','masiu')	# 替换字符内容
str1.split('.', 1)				# 以指定字符为分隔符，切几刀，返回列表['www', 'athoslau.com']
str1.startswith("www")			# 判断是否以...开头
str1.endswith(".com")			# 判断是否以...结尾
str1.lower()					# 大写转小写
str1.upper()					# 小写转大写
str1.strip()					# 删除字符串两端的空白字符
str1.partition("athos")			# 分割，成三个子串，athos为1串，其余两端各为1串
str1.splitlines()				# 按照行为分割符，返回一个列表，主要针对跨行的字符串，即多行注释
str1.isalpha()					# 判断字符是否都为字母，则返回True
str1.isalnum()					# 判断字符是否只有数字、字母组成，则返回True
str1.isnumeric()				# 判断字符是否都为数字，则返回True
str1.isdigit()

str2 = '.'
words = ['www','athoslau','com']
str2.join(words)				# 使用字符.将多个字符串拼接起来
```



## 15、列表

### 15.1 定义列表

```python
li = [11, 'athos']

# 列表中可以存任何数据类型，但是一般为了避免操作出错，列表只存储同一数据类型

print(li)			# [11, 'athos']
```



### 15.2 下标

```python
li = [11, 'athos']

# 列表也有下标，从0开始，但超过列表元素个数，就会被抛出越界异常
li[0]		# 11
li[1]		# athos
```



### 15.3 遍历

```python
li = [11, 'athos']

# 方法1：
for x in li:
	print(x)
    
# 方法2：
i = 0
while i < len(li):
    print(li[i])
    i += 1
```



### 15.4 列表常见操作

```python
list1 = [11, 22, 33, 44, 55]
list2 = [66, 77]

## 加
list1.append(66)		# 向列表中追加元素

list1.extend(list2)		# 将列表元素取出，然后追加到列表
print(list1)      		# [11, 22, 33, 44, 55, 66, 77]

list1.insert(1, 88)		# 在指定的下标处，插入元素
print(list1)			# [11, 88, 22, 33, 44, 55, 66, 77]


## 删
del list1[2]			# 删除指定下标的元素
list1.pop()				# 删除最后一个元素
list1.remove(元素值)	  # 根据元素的值进行删除


## 改
list1[下标] = 值	      # 修改值


## 查
元素值 in 列表			
元素值 not in 列表

11 in list1
```



### 15.5 列表排序

```python
list1 = [11, 22, 55, 44, 33]

list1.sort()					# 升序: 11,22,33,44,55
list1.sort(reverse=True)		# 降序: 55,44,33,22,11	
list1.reverse()					# 倒序：142 -> 241
```



### 15.6 列表嵌套

```python
list1 = [
	['上海', '广州'],
	['北京', '深圳', '香港']	
]

list1[1][2]		# 对应香港
```

```python
# 案例：列表嵌套字典，对列表进行排序

lidt = [
	{"name": "athos", "age": 19},
	{"name": "bogo", "age": 25},
	{"name": "gob", "age": 17}
]

lidt.sort()
```



### 15.7 打乱列表

```python
import random

list_t = [11, 22, 33, 44, 55]

# shuffle 表示洗牌的意思
random.shuffle(list_t)
print(list_t)
```



## 16、元组

### 16.1 元组特点

```python
元组定义后，只能查，不能被修改（增、删、改）
```



### 16.2 定义元组

```python
tuple1 = (11, 22, 33) 
```



### 16.3 遍历元组

```python
 for t in tuple1:
 	print(t)
```



## 17、集合

### 17.1 集合特点

```python
集合中，不允许有重复元素
定义时，可以重复元素，但是使用时，会自动去重
集合中的元素，没有固定顺序
```



### 17.2 定义集合

```python
set = {11, 22, 33}
```



## 18、列表、元组、集合互转

```python
# 生成新的数据，不会修改原来的
list(XXX)		# 转为列表
tuple(XXX)		# 转为元组			快速去重
set(XXX)		# 转为集合
```



## 19、字典

### 19.1 定义字典

```python
dict1 = {
	key: value,
	key2: value2
}
```



### 19.2 字典常见操作

```python
dict1 = {
	key: value,
	key2: value2
}

## 查
dict1[key2]				# 获取key2对应的值，值不存在，则会报错KeyError
dict1.get("key2","没有") 	   # 如果key2对应的值存在，则返回，如果不存在，则返回 没有 

## 增
dict1['key3'] = 'value3'

## 删
del dict1				# 删除整个字典
del dict1["key1"]		# 删除指定元素
dict1.clear()			# 清空整个字典

## 改
dict1['key2'] = 'value22'
```



### 19.3 字典遍历

```python
dict1 = {
	key1: value1,
	key2: value2,
	key3: value3
}

# 遍历字典，默认只会得到key，等价下面的遍历key
for key in dict1:
	print(key)

# 遍历key
for key in dict1.keys():
	print(key)
	
# 遍历value
for value in dict1.values():
	print(value)
	
# 遍历键值对
for item in dict1.items():
	print(item)		# 得到的是元组
```



## 20、推导式

```python
# 用于快速生成
- 列表推导式
- 集合推导式
- 字典推导式
```



### 20.1 列表推导式

```python
# 案例：记录1-100中的偶数到列表中
# 原始写法
list1 = []
for i in range(100):
	if i % 2  == 0:
		list1.append(i)


# 普通列表推导式写法：
list2 = [ x for x in rang(100) if x % 2 == 0]


# for循环嵌套，生成列表推导式
list3 = [ (x,y) for x in range(1,3) for y in rang(3)]
[(1,0),(1,1),(1,2),(2,0),(2,1),(2,2)]

# 案例：
a = [x for x in range(1, 101)]
b = [a[x:x+3] for x in range(0, len(a), 3)]
print(a)
print(b)
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14,...
[[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12],...
```



### 20.2 集合推导式

```python
list2 = {x for x in rang(100) if x % 2 == 0}
```



### 20.3 字典推导式

```python
list4 = {x: 1111 for x in rang(100) if x % 2 == 0} 

# 快速更换key和value

```



## 21、拆包

### 21.1 拆列表、拆元组

```python
拆列表、拆元组，语法是一样的
nums = [11, 22, 33, 44]
nums = (11, 22, 33, 44)

# 方式1：
nums1, nums2, nums3, nums4 = 11, 22, 33, 44

# 方式2：
nums1, nums2, nums3, nums4 = (11, 22, 33, 44)
print(nums1)
print(nums2)
print(nums3)
print(nums4)

# 方式3：
nums1, nums2, nums3, nums4 = nums
print(nums1)
print(nums2)
print(nums3)
print(nums4)
```

### 21.2 拆字典

```python
dict1 = {
	key1: value1,
	key2: value2
}

k1, k2 = dict1		# 得到的是key

for item in dict1.items:
	a, b = item		# 此时得到key和value
	
for k,y in dict1.items:
	print(k)
	print(v)
```



### 21.3 交换变量

```python
a = 1
b = 2
a, b = b, a		# 快速交换变量
```



## 22、函数

### 22.1 定义和调用函数

```python
def 函数名称(形参):
    """
    函数说明文档，说明函数功能
    """
	pass
	
函数名称(实参)
```



### 22.2 函数参数

```python
def add_2_nums(num1, num2):		# 定义形参
    print(num1 + num2)

add_2_nums(1,2)					# 调用函数传递实参
```



### 22.3 返回值

```python
def add_2_nums(num1, num2):
    return num1 + num2			# 返回值，这样的形式是返回一个元组

resulut = add_2_nums(1,2)		# 变量接收函数的返回值
print(result)

return后的语句将不再执行，结束函数的运行
```



### 22.4 参数类型

```
- 无参，无返回值
- 无参，有返回值
- 有参，无返回值
- 有参，有返回值
```



### 22.5 函数嵌套

```
def test1():
	print("test1")
	
def test2():
	test1()
	print("test2")

test2()
```



### 22.6 局部变量、全局变量

```python
num1 = 123

def f1():
	num1 = 7788		# 实际上是定义了与全局变量同名的局部变量
	print(num1)

def f2():
	pint(num1)
	
def f3():
	global num1		# 引用全局变量，并修改值
	num1 = 3344
	print(num1)
	
print(num1)			# 输出 3344，在f2中已经被修改


f1()		# 输出 7788
f2()		# 输出 123
f3()		# 输出 3344


## 总结：
定义全局变量，使用全部大写，多个单词使用下划线连接
函数中要想修改全局变量，使用global关键字
```



### 22.6 缺省参数

```python
def add_2num(num1, num2=2):  # num2=2，写在形参中，就是缺省参数，应当写在形参列表的最后
    print("%d + %d = %d" % (num1, num2, num1 + num2))


add_2num(18)  # 调用函数，未传参，则使用默认值
add_2num(18, 35)  # 调用函数，传了参，就不再使用默认参数

总结：
缺省参数，只能写在形参的右边
```



### 22.7 命名参数

```python
def add_3num(num1, num2, num3=3, num4=4):
    print("%d + %d + %d = %d" % (num1, num2, num3, num1 + num2 + num3))

add_3num(7, 8,num3=9 num3=35)		# 调用函数时，将指定实参传递给指定实参

总结：
命名参数只能写在实参的右边
```



### 22.8 不定长参数

```python
# 不定长参数，传递的实参的个数任意

def test(a, b, c100, d=200, *args, **kwargs):
	print("a=", a)				# 1
    print("b=", b)				# 2
    print("args=", args)		# (3,4)
    print("kwargs=", kwargs)	# { "name": "athos", "site": "www.athoslau.top" }
    
sum_nums(1,2,3,4, name='athos', site='www.athoslau.top')



*args		# 调用函数时，多余的未命名参数，都以元组的形式存储到 args 中
**kwargs	# 调用函数时，多余的命名参数，都以键值对的形式存储到 kwargs 中
```



### 22.9 函数返回值拆包

```python
def test():
	return 11,22,33
	
a,b,c = test()
```



### 22.10 使用*拆包

```python
def test(a, b, c):
	print(a, b, c)

nums = [11, 22, 33]

如何将nums列表中的元素传进函数test()?

test(*nums)		# * 可以针对列表、元组、集合进行拆包
```



### 22.11 使用**拆包

```python
def test(aa, bb, cc):
	print(aa)
	print(bb)
	print(cc)

nums = {
	'aa': 11,
	'bb': 22,
	'cc': 33
}


test(**nums)	#· ** 可以针对字典拆包
```

```pythoN
def test1(*args, **kwargs):
    print("-----------test1-------------")
    print("args=", args)
    print("kwargs=", kwargs)


def test2(*args, **kwargs):
    print("-----------test2-------------")
    print("args=", args)
    print("kwargs=", kwargs)
    test1(args, kwargs)
    # 相当于test1((11,22,33),{'name': 'athos', 'site': 'ww.athoslau.top'})，没有进行拆包

test2(11, 22, 33, name='athos', site='ww.athoslau.top')


运行结果：
-----------test2-------------
args= (11, 22, 33)
kwargs= {'name': 'athos', 'site': 'ww.athoslau.top'}
-----------test1-------------
args= ((11, 22, 33), {'name': 'athos', 'site': 'ww.athoslau.top'})
kwargs= {}
```

```pythoN
def test1(*args, **kwargs):
    print("-----------test1-------------")
    print("args=", args)
    print("kwargs=", kwargs)


def test2(*args, **kwargs):
    print("-----------test2-------------")
    print("args=", args)
    print("kwargs=", kwargs)
    test1(*args, **kwargs)
    # 相当于test1(11,22,33,name='athos',site='www.athoslau.top') 都传递给了 test1中的*args

test2(11, 22, 33, name='athos', site='ww.athoslau.top')


运行结果：
-----------test2-------------
args= (11, 22, 33)
kwargs= {'name': 'athos', 'site': 'ww.athoslau.top'}
-----------test1-------------
args= (11, 22, 33)
kwargs= {'name': 'athos', 'site': 'ww.athoslau.top'}
```



### 22.12 函数的引用

```
def test():
	return 123
	
num = test
num2 = test()

print(num())
print(test())
print(num2)
以上三个输出结果都是一样的	
```



### 22.13 匿名函数

```python
# 概念：
使用lambda定义的函数，但是没有名字。用一行代码，只适合完成简单的函数定义
匿名函数可以当做实参，传递到函数中去
一般情况下，通过一个变量 指向匿名函数，然后使用变量名()进行调用
匿名函数本身就有return,不需要再单独写

# 定义匿名函数语法：
lambda 形参, 形参: 表达式
lambda : 表达式					# 不需要参数的情况



# 案例1
test = lambda a, b : a + b
sum2 = test(11, 22)


# 案例2：匿名函数当实参
def fun(a, b, opt):
    print(a)
    print(b)
    print("result = %d" % opt(a, b))		# 2、此时opt指向了匿名函数，所以，再将a,b传递给匿名函数中去

fun(1, 2, lambda x, y : x + y)	# 1、匿名函数做实参传递
```

```
# 案例：匿名函数应用：对列表中嵌套的字典进行排序

stus = [
	{"name": "athos", "age": 18}
	{"name": "rocket", "age": 19}
	{"name": "jack", "age": 17}
]

def sort_by_age(temp_dict):
	return temp_dict['age']
	
stus.sort(key=sort_by_age)

# 使用lambda表达式
stus.sort(key=lambda temp_dict: temp_dict['age'])


```



### 22.14 递归函数

```bash
一个函数中，调用了函数本身，那么这个函数就叫做递归函数

缺点：极度占用内容，python限制了嵌套调用的次数，据说约997次

应用：1、面试
2、数据结构的学习
3、解决阶乘问题

5！==> 5*4*3*2*1
4! ==> 4*3*2*1

def mult_nums(n):
    if n > 1:
        return n * mult_nums(n - 1)
    else:
        return 1


ji = mult_nums(4)
print(ji)
```



## 23、文件操作

```
# 1、写入文件（打开文件、写入、关闭文件）
f = open("文件路径", "操作类型")
	f.write()

操作类型：
W		-- 写字符串(文本类)
wb		-- 写二进制(图片、视频等)
r		-- 读取

# 读取文件（打开文件、读取、关闭文件）
f = open("文件路径", "r")
	content = f.read		# 一次性全部加载
	content = f.readline	# 一次读取1行内容

# 3、关闭文件
f.close()
```





# 二、面向对象

## 1、定义类，创建对象

```python
# 定义类
# class Person:					# 定义格式1
class Person(object):			# 定义格式2
    def __init__(self, name, age):
        self.name = name		# 实例属性
        self.age = age
	
    # 实例方法
    def print_info(self):
        print("姓名：%s\t\t年龄：%d" % (self.name, self.age))


# 创建实例对象
stu = Person("athos", 18)
stu.print_info()
```



## 2、\__init__方法

```
1、在创建对象时，会自动调用__init__()方法，进行初始化（设置一些默认的属性）

class Person(object):
    def __init__(self, name, age):
        self.name = name

athos = Person("atos")
```



## 3、私有属性和私有方法

```python
class Person(object):
    def __init__(self, name, age):
        self.name = name
        self.__age = age  # 将年龄设置为私有属性


    def __set_age(self, age):
        if age > 0:
            self.__age = age
        else:
            self.__age = 0


    def print_info(self):
        print("姓名：%s\t\t年龄：%d" % (self.name, self.__age))



stu = Person("athos", 18)

# print(stu.__age)        # 这行代码会报错，因为不能直接访问私有属性
stu.__age = 20            # 这行代码也会报错，因为不能直接修改私有属性
stu.print_info()

	
stu._Person__age = 100   # 使用名称重整的方式修改私有属性
stu.print_info()
#姓名：athos		年龄：18
#姓名：athos		年龄：100



总结：
1、私有属性，用 __变量名 表示
2、私有方法，用 __方法名 表示
3、私有属性的含义：为了隐藏属性或者功能，不希望被外部直接调用
4、一般在实例方法中，调用私有属性
5、私有属性和私有方法，不能在外部通过实例对象直接调用，否则会报错
6、在外部，实例对象._类__属性名  实例对象._类__方法名 可以调用，但不推荐使用
```



## 4、对象关联

### 4.1 关联单个对象

```python
# 方法1
class Student(object):
    def __init__(self, name):
        self.name = name


class Classroom:
    def __init__(self, cname):
        self.cname = cname

    def show_info(self):
        print("教室：%s\t\t学生：%s" % (self.cname, self.student))


stu = Student("张三")
clsroom = Classroom("302班")

clsroom.student = stu   # 对象关联方式1
clsroom.show_info()     # 教室：302班		学生：<__main__.Student object at 0x000001F02E9970A0>
```

```python
# 方法2
class Student:
    def __init__(self, name):
        self.name = name
        
        
class Classroom:
    def __init__(self, name):
        self.student = None
        self.name = name

    def add_student(self, student):  # 定义方法，实现对象关联
        self.student = student

    def show_info(self):
        print("教室：%s\t\t学生：%s" % (self.name, self.student))


stu = Student("张三")
clsroom = Classroom("302班")

clsroom.add_student(stu)    # 调用方法，将实例对象的引用当实参
clsroom.show_info()         # 教室：302班		学生：<__main__.Student object at 0x0000028E988F7070>

print(clsroom.student.name)	# 张三
```

### 4.2 关联多个对象

```python
通过定义列表、字典、集合，用来存储多个对象

# 方法2
class Student:
    def __init__(self, name):
        self.name = name



class Classroom:
    def __init__(self, name):
        self.students = list()			# 定义列表，存储多个student对象
        self.name = name

    def add_student(self, student): 
        self.students.append(student)

    def show_info(self):
        for student in self.students:
            print("教室：%s\t\t学生：%s" % (self.name, student.name))

            
clsroom = Classroom("302班")
stu1 = Student("张3")
stu2 = Student("张4")

clsroom.add_student(stu1)
clsroom.add_student(stu2)
clsroom.show_info()
```



## 5、继承

```python
1、python支持多继承，即一个类中，写多个父类
2、子类可以使用父类中的方法
3、子类也可以使用自己类中同名的方法
4、父类中一般写的是所有子类都适用的方法


class A(Object):
	pass

class B:
	pass
	
class C(A, B)
	pass
```



## 6、重写

```python
重写：在子类中重新书写和父类中相同的方法

class Father:
	def fa1():
		pass
		
class Son(Father):
	def fa1():		# 这就是重写
		pass
```



## 7、super方法

```python
接着上面，父类中的方法，并非完全不能使用，需要再添加一些功能，那么子类在重写时，使用super()调用父类方法后，再添加自己的新功能

class Father:
	def fa1(self):
		pass
		
class Son(Father):
	def fa1(self):		# 重写
		super().fa1()	# 先调用父类中的方法
		pass			# 再添加子类的新功能
		
```



## 8、多态



## 9、静态方法

```python
1、在类中定义的方法前，加上@staticmethod
2、类方法的应用场景：不需要写self、cls，只是想单纯地输出一些信息，这些信息和对象、类属性不相关
3、静态方法可以用实例对象去调用：实例对象.静态方法()   
还可以通过类去调用：类.静态方法名()

@staticmethod
def show_info():
	pass
```



## 11、类属性

```python
# 应用场景：多个实例对象，可以共享的数据

class Tool(object):
    # 定义类属性，做计数器
    num = 0

    def __init__(self, name):
        self.name = name
        Tool.num += 1   # 每实例化对象一次，计数器+1


chutou = Tool("锄头")
tieqiao = Tool("铁锹")
print(Tool.num)			# 输出结果：2	
```



## 10、类方法

```python
# 1、通过实例对象.类方法(), 也可以通过类名.类方法()

class Tool(object):
    # 定义类属性，做计数器
    num = 0

    def __init__(self, name):
        self.name = name
        self.add_sum()

    @classmethod		# 定义类方法
    def add_sum(cls):
        cls.num += 1

    @classmethod
    def print_info(cls):
        print("num = %d" % cls.num)


chutou = Tool("锄头")
tieqiao = Tool("铁锹")
print(Tool.num)  	# 调用类属性，输出结果：2
Tool.print_info()	# 调用类方法
```



## 类对象

```python
所有实例对象，都有一个属性__class__，同一个类的所有实例对象都指向了同一个类对象，避免重复代码浪费空间
```



## dir(实例对象)

```python
除了 __class__ 之外，实例对象还有哪些属性？

print(dir(实例对象))
['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'add_sum', 'name', 'num', 'print_info']
```





# 三、Pyhton高级

## 1、迭代器

### 1.1 引入

```python
class StuSystem(object):
    def __init__(self):
        self.stus_lists = []

    def add_info(self):
        new_stu = {}
        stu_name = input("请输入姓名：")
        stu_age = input("请输入年龄：")
        stu_class = input("请输入班级：")

        new_stu["stu_name"] = stu_name
        new_stu["stu_age"] = stu_age
        new_stu["stu_class"] = stu_class

        self.stus_lists.append(new_stu)


stu_sys = StuSystem()
stu_sys.add_info()
stu_sys.add_info()
stu_sys.add_info()


# 问题：如何才能实现使用for循环遍历系统中的所有学生信息，下面的方法能实现么?
for stu in stu_sys:
    print(stu)
    
"""
Traceback (most recent call last):
  File "D:\PLearning\迭代器\01、引入迭代器.py", line 25, in <module>
    for stu in stu1:
TypeError: 'StuSystem' object is not iterable
"""
```

总结：

实际开发中，经常需要快速将对象转换为其他不同的数据类型。

迭代器，就是为了解决对象不可迭代的问题https://www.bilibili.com/video/BV1AN4y137uT/?p=3&spm_id_from=pageDriver&vd_source=372b9d438c51e9e9ffb63f6e38e889d0



### 1.2 什么是迭代

迭代就是访问集合的一种方式。



### 1.3 什么是可迭代对象

可以通过for循环遍历的，就是可迭代对象（列表、元组、字典、字符串）

不可迭代对象（整数、浮点数）



### 1.4 判断是否是可迭代对象

```
from collection.abc import Iterable

print(isinstance([], Iterable))
```



### 1.5 迭代器

迭代器是一个可以记住遍历的位置的对象。送代器对象从第一个元素开始访问，直到所有的元素被访问完结束。送代器只能往前不会后退。

```
list1 = [11, 22, 33, 44]
iter_list =iter(list1)		# iter() 获取迭代器
print(next(iter_list))		# next() 取迭代器的值
print(next(iter_list))
print(next(iter_list))
print(next(iter_list))

print("++++++++++++++++++++")
for num in list1:
    print(num)

'''
11
22
33
44
++++++++++++++++++++
11
22
33
44
'''
```

### 1.6 next()取值的异常

```python
list1 = [11, 22, 33, 44]
iter_list =iter(list1)		# iter() 获取迭代器
print(next(iter_list))		# next() 取迭代器的值
print(next(iter_list))
print(next(iter_list))
print(next(iter_list))
#print(next(iter_list))		# 第5个元素不存在，迭代器取值时会报错

# 处理next()异常
try:
    print(next(iter_list))
except StopIteration as ret:
    print("警告：迭代器取值，超过了元素个数")


print("++++++++++++++++++++")
for num in list1:
    print(num)

'''
Traceback (most recent call last):
  File "D:\PLearning\迭代器\迭代器.py", line 7, in <module>
    print(next(iter_list))		# 第5个元素不存在会报错
StopIteration
11
22
33
44
'''

```







# 模块

## 模块：time

```
import time

time.strftime("%H:%M:%S", time.localtime())			# 得到字符串格式的时间，以HH:MM:SS显示
```

## 模块：random

```
import random

random.int(1,10)				# 生成随机整数 1 - 9
random.shuffle(list_t)			# 打乱列表的元素排列顺序
random.choice(list_t)			# 随机任意选一个
```

## 模块：sys

```
import sys

sys.argv				# 列表，表示传递进终端中的参数，可以用下标来取

print(sys.argv[1])
```

## 模块：os




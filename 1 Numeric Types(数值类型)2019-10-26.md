数字常量
====
```
>>> 1234    # 整数
1234
>>> 99999999999999999999999999999999999999999999999999  # 可表示无穷大的数
99999999999999999999999999999999999999999999999999
>>> 1.232455   # 符点数（小数）
1.232455
>>> 1.     # 小数点后的零可以省略，依旧是符点数
1.0
>>> .548777  # 小于1的小数，0可以省略
0.548777
>>> 3.147e10  # 科学计数法，整数位只能有1位数字，3.147×10的10次幂
31470000000.0
>>> 3.147e-2  # 3.147×10的-2次幂
0.03147

```
运算符号
====
```×
>>> 1 + 2
3
>>> 5 - 4
1
>>> 2 * 2
4
>>> 4 / 2   # / 除的结果是符点数
2.0
>>> 6 / 4
1.5
>>> 6 // 4  # //除的结果是整数
1
>>> 7 >> 1  # 位操作，把 7 转换为二进制数111，右移一位是11，即十进制数3
3
>>> 7 << 1  # 位操作，把 7 转换为二进制数111，左移一位是1110，即十进制数14
14
>>> 8 & 5   # 按位与，把8和5分别转换为二进制数1000和0101，按位与
0
>>> 8 | 5   # 按位与，把8和5分别转换为二进制数1000和0101，按位或
13
>>> not 1   # 非运算，非0永远代表True，0代表False
False
>>> not 0   # 返回值为布尔类型（bool），bool类型只有两个值True和False，注意第一个字母是大写，小写的true和false不是bool类型
True
>>> not 1212
False
```
内置数学函数
====
```
>>> pow(2, 10)   # 乘方运算
1024
>>> 2 ** 10    # 和 ** 运算符结果一致，但效率更高
1024
>>> abs(-10)   # 求绝对值
10
```


----
```
>>> 12 + 30.5     # 整数和符点数相加为符点数
42.5
>>> int(3.634)    # 符点数转换为整数
3
>>> float(32)     # 整数转换为符点数
32.0
```
变量
====
## 变量命名规则
```
>>> _a = 3    # 变量名首字符必须以字母或 _ 开头，不能以数字或其它符号开头
>>> _ = 1     # 后面的字符可以是字母、数字、下划线，但不能含有其他符号
>>> 1a = 1
  File "<stdin>", line 1
    1a = 1
     ^
SyntaxError: invalid syntax
>>> a123-123
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'a123' is not defined
>>> a123_234234 = 1
```
```
>>> a = 3
>>> b = 4
>>> a + 1, a - 1
(4, 2)
>>> b * 3
12
>>> b / 2
2.0
>>> a % 2  # 取余运算
1
```
## 关系运算符
```
>>> 1 > 2
False
>>> 2 > 1
True
>>> 2 >= 2   # 大于等于
True
>>> 2 <= 7   # 小于等于
True
>>> 2 != 7   # 不等于
True
>>> 2 == 2   # 判断是否相等
True
>>> a = 3    # =是赋值运算，不同于数学里的等号
>>> 2 == 2.0
True
>>> X = 2
>>> Y = 4
>>> Z = 6
>>> X < Y < Z
True
>>> X < Y and Y < Z
True
```
## type函数可以输出数据的类型
```
>>> type(1 > 2)
<class 'bool'>
>>> type(1)
<class 'int'>
>>> type(1.2)
<class 'float'>
>>> type(True)
<class 'bool'>
>>> true = 1
>>> type(true)
<class 'int'>
```
## 内置数学工具
```
>>> import math   # 引入math数学库
>>> math.floor(2.4)   # floor函数，是求小于该数的最大整数
2
>>> math.floor(-2.4)
-3
>>> math.trunc(2.4)   # trunc函数，是求该数距离0最近的整数，也可以理解为取整
2
>>> math.trunc(-2.4)
-2
>>> help(math.floor)  # 利用help函数查询某个函数的具体含义及使用方法

>>> help(math.trunc)

>>> math.pi           # 圆周率
3.141592653589793
>>> math.e            # 自然常数e
2.718281828459045
>>> math.sqrt(2)      # 开平方
1.4142135623730951
>>> sum([1, 2, 3, 4])  # 求和
10
>>> sum(1, 2, 3, 4)    # sum只能接受一个参数，可以是列表或元组
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: sum expected at most 2 arguments, got 4
>>> sum([1, 2, 3, 4])
10
>>> min(3, 1, 10, 2)   # 求最小值
1
>>> max(3, 1, 10, 6)   # 求最大值
10
```

## 随机数
```
>>> import random      # 引入random随机数库
>>> random.random()    # 生成一个0到1之间的数
0.7167219605180954
>>> random.randint(1, 100)   # 生成一个1到100之间的整数
46
```
## 分数
```
>>> from fractions import Fraction   # 引入分数类型 Fraction
>>> x = Fraction(1, 3)      # 创建分数对象
>>> x
Fraction(1, 3)
>>> print(x)
1/3
>>> y = Fraction(4, 6)     # 自动约分
>>> y
Fraction(2, 3)
>>> z = x + y      # 两个分数进行 + - * / 运算后，结果还是分数类型
>>> z
Fraction(1, 1)
>>> print(z)
1
>>> type(z)
<class 'fractions.Fraction'>
>>> x - y
Fraction(-1, 3)
>>> x * y
Fraction(2, 9)
>>> x / y
Fraction(1, 2)
>>> Fraction(.25)     # 把小数直接转换成分数
Fraction(1, 4)
>>> Fraction(1)
Fraction(1, 1)
>>> Fraction(10)
Fraction(10, 1)
>>> Fraction(10.8)
Fraction(3039929748475085, 281474976710656)
>>> Fraction(1.3)
Fraction(5854679515581645, 4503599627370496)
>>> Fraction(.35)
Fraction(3152519739159347, 9007199254740992)
>>> Fraction(.25)
Fraction(1, 4)
>>> Fraction(1.25)
Fraction(5, 4)
>>> Fraction('1.25')
Fraction(5, 4)
```

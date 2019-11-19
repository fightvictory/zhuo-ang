字典 dictionary
===
```
{key1: value1, key2: value2, ...}
```

### 字典的操作
```
>>> D = {'Num': 1, 'name': 'zhuoang', 'gender': 'male'}     # 字典的定义
>>> D['Num']       # 以下标的方式取出 key 对应的 value
1
>>> D['name'] 
'zhuoang'
>>> len(D)         # 求字典中键值对的个数
3
>>> D
{'Num': 1, 'name': 'zhuoang', 'gender': 'male'}
>>> 'name' in D    # 求 key 是否在字典中
True
```

### 字典的方法
```
>>> list(D.keys())      # keys方法是求出字典中所有key, 用 list 生成列表
['Num', 'name', 'gender']
>>> list(D.values())    # values方法是求出字典中所有value, 用 list 生成列表
[1, 'zhuoang', 'male']


>>> D['Num'] = 2        # 给字典中已经存在的 key 赋值时，则修改对应的值 value
>>> D
{'Num': 2, 'name': 'zhuoang', 'gender': 'male'}
>>> D['gender']         # 读取字典中 key 对应的值
'male'
>>> D['age']            # 当读取的 value 在字典中不存时，则报错
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'age'
>>> D['age'] = 14       # 当给字典中不存在的 key 赋值时，则向字典中增加了新的键值对
>>> D
{'Num': 2, 'name': 'zhuoang', 'gender': 'male', 'age': 14}

>>> list(D.items())     # items 方法，取出字典中所有的键值对，用 list 生成列表，列表元素是一个元组 tuple
[('Num', 2), ('name', 'zhuoang'), ('gender', 'male'), ('age', 14)]
```

```
>>> D.get('age')     # get 方法可以取出字典中键对应的值
14
>>> D.get('hobby')   # get 方法对不存在的 key 取值时，没有任务输出
>>> print(D.get('age'))
14
>>> print(D.get('hobby'))   # 但用 print 输出时，显示 None， None 是python中的常量，表示什么也没有
None
>>> D.get('hobby', 'study')  # 可以给 get 方法设置第二个参数，当对不存在的 key 取值时，输出默认值，而不输出None
'study'

>>> D.update({'hobby': 'study', 'address': 'Siping'})  # update 方法为原字典增加键值对
>>> D
{'Num': 2, 'name': 'zhuoang', 'gender': 'male', 'age': 14, 'hobby': 'study', 'address': 'Siping'}

>>> D.pop('hobby')   # pop 方法删除字典中的键值对
'study'
>>> D
{'Num': 2, 'name': 'zhuoang', 'gender': 'male', 'age': 14, 'address': 'Siping'}
```

### 遍历字典
```
>>> for key in D:      # 遍历字典
...     print(key)
... 
Num
name
gender
age
address
>>> for item in D:     # 同时输出 key 和 value
...     print("key:%s, value:%s" % (item, D[item])
... 
... )
... 
key:Num, value:2
key:name, value:zhuoang
key:gender, value:male
key:age, value:14
key:address, value:Siping
```

### 遍历列表 list
```
>>> for c in L:                  # 使用 index 方法，效率很低
...     print(L.index(c), c)
... 
0 a
1 b
2 u
3 c

>>> for (i, c) in enumerate(L):      # 使用系统方法，enumerate 实现索引值和无素值的输出
...     print(i, c)
... 
0 a
1 b
2 u
3 c

>>> for (i, c) in enumerate(L, 1):     # 第二个参加，可以指定起始值
...     print(i, c)
... 
1 a
2 b
3 u
4 c
```

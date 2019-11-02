```
>>> help(str)

>>> min('d', 'a', 'c', 't')
'a'
>>> min('d', 'a', 'c', 'T')
'T'
>>> 'a' > 'A'
True
>>> ord('a')
97
>>> ord('A')
65
>>> ord('6')
54
>>> ord('0')
48
>>> chr(97)
'a'
>>> help(ord)

>>> help(chr)
```

字符串
======
```
>>> "I love Python"
'I love Python'
>>> 'I love Python'
'I love Python'
>>> 'a'
'a'
>>> 'b'
'b'
>>> '''dafewaoejfrkldjsfaksjewijfklsadjfaeiw
... jfalskfjsklfjadskfjas
... fjslkjfadlsfkjas'''
'dafewaoejfrkldjsfaksjewijfklsadjfaeiw\njfalskfjsklfjadskfjas\nfjslkjfadlsfkjas'
>>> """ fiowejrfksfjaoewfj
... dsfjioejwfoijqiofjwaq
... vcx,mvcxz,.mvkladsfvxcvz"""
' fiowejrfksfjaoewfj\ndsfjioejwfoijqiofjwaq\nvcx,mvcxz,.mvkladsfvxcvz'
>>> print('''abc
... bcd
... efg''')
abc
bcd
efg
>>> title = "meaning"'of'"Life"
>>> title
'meaningofLife'
>>> title = 'meang "of" Life'
>>> title
'meang "of" Life'
>>> 'knight\'s'
"knight's"
>>> 'knight\"s'
'knight"s'
>>> 'knight"s'
'knight"s'
>>> 'knight's'
  File "<stdin>", line 1
    'knight's'
            ^
SyntaxError: invalid syntax
>>> 'knight\'s'
"knight's"
```
>>> s = 'a\nb\tc'
>>> s
'a\nb\tc'
>>> print(s)
a
b	c
>>> s = 'a\nb\tc\vd'
>>> print(s)
a
b	c
         d
>>> 'abcdefg\
... hijklmn\
... opqrst'
'abcdefghijklmnopqrst'
>>> 'fdasfadsfadssssssssssssssssssss\sssssssssssssssssssssssssssssssss
  File "<stdin>", line 1
    'fdasfadsfadssssssssssssssssssss\sssssssssssssssssssssssssssssssss
                                                                     ^
SyntaxError: EOL while scanning string literal
>>> print('fadsfasfadsfadsfadsfadsf\
... fdsfadslfjadslfadjslf\fadsfsadlfadjslf')
fadsfasfadsfadsfadsfadsffdsfadslfjadslfadjslf
                                             adsfsadlfadjslf
>>> 'asdfasfa\\rewrewrewr'
'asdfasfa\\rewrewrewr'
>>> 'asdfasfa\\rewrewrewr'
'asdfasfa\\rewrewrewr'
>>> 'asdfasfa \\ ewrewrewr'
'asdfasfa \\ ewrewrewr'
>>> '\\'
'\\'
>>> '\'
  File "<stdin>", line 1
    '\'
      ^
SyntaxError: EOL while scanning string literal
>>> print('\\')
\
>>> '\n'
'\n'
>>> print('dfasfads\nfdsafadsfa')
dfasfads
fdsafadsfa
>>> print('dfasfads\\fdsafadsfa')
dfasfads\fdsafadsfa
>>> '\a'
'\x07'
>>> print('\a')

>>> print('\a')

>>> print('\a')

>>> for i in range(10):
...     print('\a')
... 










>>> import time
>>> for i in range(10):
...     print('\a')
...     time.sleep(1)
... 










>>> s = 'Python'
>>> len(s)
6
>>> 'acd' + 'def'
'acddef'
>>> 'Hi! " * 4
  File "<stdin>", line 1
    'Hi! " * 4
             ^
SyntaxError: EOL while scanning string literal
>>> 'Hi! ' * 4
'Hi! Hi! Hi! Hi! '
>>> print('=' * 80)
================================================================================
>>> myjob = 'hacker'
>>> for c in myjob:
...  print(c)
... 
h
a
c
k
e
r
>>> help(print)

>>> for c in myjob:
...  print(c, end='')
... 
hackfor c in myjob:
... 
  File "<stdin>", line 2
    
    ^
IndentationError: expected an indented block
>>> for c in myjob:
...  print(c, end=' ')
... 
h a for c in myjob:
... 
  File "<stdin>", line 2
    
    ^
IndentationError: expected an indented block
>>> for c in myjob:
...  print(c, end='_')
... 
h_a_for c in myjob:
...  print(c, end='000000000')
... 
h000000000a000000000c000000000k000000000e000000000r000000000>>> 
>>> print('abc', '123', 'xyz', sep='####')
abc####123####xyz
>>> help(print)

>>> s = "I love Python"
>>> s[0]
'I'
>>> s[5]
'e'
>>> s[-1]
'n'
>>> len(s)
13
>>> s[12]
'n'
>>> s[-1]
'n'
>>> s[-2]
'o'
>>> s[-3]
'h'
>>> s[2:6]
'love'
>>> s[0:6]
'I love'
>>> s[:6]
'I love'
>>> s
'I love Python'
>>> s[7:-1]
'Pytho'
>>> s[7:]
'Python'
>>> s[:]
'I love Python'
>>> s = "abcdefghijk"
>>> s[:]
'abcdefghijk'
>>> s[::2]
'acegik'
>>> s[::1]
'abcdefghijk'
>>> s[::]
'abcdefghijk'
>>> s[::0]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: slice step cannot be zero
>>> s[::-1]
'kjihgfedcba'
>>> "42" + 1
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: must be str, not int
>>> "42" + str(1)
'421'
>>> s = 1
>>> '42' + s
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: must be str, not int
>>> '42' + 's'
'42s'
>>> '42' + str(s)
'421'
>>> int('42') + 1
43
>>> int('42') + s
43
>>> s
1
>>> s = 'spam'
>>> s[0] = 'x'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
>>> s = 'x' + s[1:]
>>> s
'xpam'
>>> s = 'I love Python'
>>> s.replace('Python', 'Java')
'I love Java'
>>> s
'I love Python'
>>> s = s.replace('Python', 'Java')
>>> s
'I love Java'
>>> age = 10
>>> print("the boy is %d" % age)
the boy is 10
>>> print("the boy is %d years old" % age)
the boy is 10 years old
>>> age = 20
>>> print("the boy is %d years old" % age)
the boy is 20 years old
>>> address = "四平"
>>> print("the boy is come from %s, he is %d years old" % address, age) 
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: not enough arguments for format string
>>> print("the boy is come from %s, he is %d years old" % (address, age))
the boy is come from 四平, he is 20 years old
>>> "the boy is come from %s, he is %d years old".format(address, age)
'the boy is come from %s, he is %d years old'
>>> "the boy is come from {0}, he is {1} years old".format(address, age)
'the boy is come from 四平, he is 20 years old'
>>> help(str)


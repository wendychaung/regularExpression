# 正则表达式

```
g 全文搜索匹配(不添加代表搜索到第一个停止)

i 忽略大小写，默认是大小写敏感

m 多行搜索
```


**原义文本字符**

**元字符（有特殊含义的非字母字符）**
```
\t 水平制表符

\x0B 垂直tab而已

\v 垂直制表符

\n 换行符

\r 回车符

\0 空字符

\f 换页符
```

**[]来构造类**

**^ 取反** 
在类中，表示取反

**范围类[a-z]**
如果需要匹配"-"，就写成[a-z-]

**预定义类**
```
. == [^\r\n] 除了回车换行意外事件的所有字符

\d ==[0-9] 数字字符

\D ==[^0-9] 非数字字符

\s ==[\t\r\x0B\n\f] 匹配任何不可见字符，

\S ==[^\t\r\x0B\n\f] 非空字符串

\w ==[a-zA-Z_0-9] 单词字符，包括大小写字母，数字，下划线

\w ==[^a-zA-Z_0-9] 非单词字符
```


**边界**

```
^ 以**开始

\b 单词边界

$ 以***结束

\B 非单词边界
```


**量词**

```
？最多出现一次

+ 至少出现一次

* 出现任意次 

{n} 出现n次

{n,m}出现n-m次

{n,} 至少出现n次
```

**贪婪模式** 
尽可能多的匹配

**非贪婪模式** 
在量词后加上？

**分组**
用()分组，可以让量词作用于分组

**或**
使用|可以实现

**分组捕获**
可以$来代替对分组内进行捕获

**忽略分组**
在分组内加上 ?:
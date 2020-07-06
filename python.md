# python的WEB框架 开发：1、django；2、flask

# python文件头模板
## python在Linux下的文件头
```
#! /usr/bin/python
```
## 常用的编码格式
```
# -*- coding:UTF-8 -*-
```
## 函数格式
'''
    def main():
        # 主函数
        pass
    if __name__ == '__main__'
        main()
'''
### Python 编译为exe

# IP代理（爬虫）
```
    httpbin.org
    httpbin.org/ip   （查IP）
```
* 快代理、云代理
* 911s5
* https://www.zionladderh.com/register/wqJ1wqXCqsOIworCgsKUwoXCosKlw5PCpMKUwo7CssOKwr7CmnnDksOUwp7Ch8Kzw4nCjsOOdMKqwqnDjcKRwrXClMKI/


* winver      查看系统版本
* cmd   netstat    查看开启的端口
* ettercap 
* dsniff   嗅探密码
* Fluxion无限攻击工具

** (表示乘方)   //(表示除取整) a in b (成员运算符)
# 字符串切片：
a = 'afewfa'
print(a[0])    输出第一个
print(a[0:3])  从第下表为0的取到第3个字符
print(a[0:5:2]) 从下表为0的取到第5的，并且中间隔一个
print(a[0:-1])  从下表为0的取到倒数第二个


a.capitalize()   首字母大写
a.swapcase()     大小写翻转
a.title()        每个单词的首字母大写
a.center(10,'*') 把a居中，并用*填充有空余的位置
a.startswith('a') 判断字符串是以a开头的吗
a.endswith('f')  判断字符串是否是以f结尾
a.startswith('avd',2,5)   判断字符串小标为2到第5个是否是avd
a.find('si')    查找字符位置
a.replace('i','N')   替换
a.isalpha()      判断a中是否全为字母（空格除外）
a.isnumeric()    判断a中是否全为数字
a.strip('*')     去除*号
a.lstrip()或a.rstrip()
a.split（'.'）   以点标识分隔



# 列表：
(有序)
li = ['xiaoguo','xiaoming',123]
## 增
li.insert(0,'first')   在字典下表为0处出入first
li.append('last')      在末尾插入last
## 删
li.pop()               删除最后一个
del li[2:4]            批量删除从下表为2开始到第4个
li.remove('xiaoguo')   精确删除
li.clear()             删除所有
## 改
li[2]='csdc'           修改下表为2的
## 查
li.count('xiaoming')   查询列表中'xiaoming'的个数
li.index('xiaoming')   查询列表中'xiaoming'的列表位置
ss.sort()              将列表排序



# 字典
(无序,键值对)
dic = {"name":"xiaoguo","age":18,"job":"driver"}
## 增
dic["addr"] = "menyuan"    在字典中添加
## 删
dic.pop("job")             在字典中删除job的键值对
## 改
dic["age"] = 21             修在字典中age的值
## 查
for key,value in dic.items():
    print(key+"--->"+value)    查看键值对

for i in dic:
    print(i)                   只看键
for i in dic:
    print(dic[i])              只看值

print(dic.keys())              查看有格式的值
print(dic.values())            查看有格式的键


# 集合 
(无序，不重复)
set1 = {1,53,4,3,}
## 增
set1.add('sad')
## 删
set1.remove(3)
set1.pop()                     随机删除
set1.clear()
## 取交集
print(set1 & set2)
## 取并集
print(set1 | set2)
## 取差集
print(set1 - set2)
## 取反交集
print(set1 ^ set2)


# 元组 （touple）
无法修改，只能查
toupl = ("xiaoguo","xiaohong","xiaoming")

## 转换
li = list(touple)              元组转列表
set2 = set(touple)             元组变集合

# 循环
for i in range (1,11,2)
    print(i)

------------------------------------------------

# 文件操作
### 读文件
f = open("a.text",'r',encoding='utf-8')
data = f.read()
print(data)
f.readline()              只读取一行
f.readlines()             把文件的每一行加入到列表中
f.read(4)                 每次读取4个字
f.close()
### 写文件
f = open('a.tex','w',encoding='utf-8')
f.write('neirong')         覆盖写入
'r'----->'a'               追加写入
f.write('fads')
f.close()                   
###  免关闭操作文件
with open('./a.txt','w') as f
    f.write()


# 控制操作系统
import os
print(os.path.isfile('C:/Users/31650/Desktop/a.txt'))    判断是否存存在
os.mkdir('c:/Users/31650/Desktop/a)         创建文件夹
os.rmdir('c:/User/31650/Desktop/a)          删除该文件夹
print(os.listdir('c:/'))                    列出所有文件夹
print(os.system('ipconfig'))                直接执行操作系统的命令
print(os.system('dir'))                     查看当前目录
print(os.system('netstat -ano'))            查看该系统的所有端口
print(os.system('whoami'))                  谁在操作该电脑



` with open可以用逗号打开多个文件句柄 `
```
with open('./a.txt','r') as f1,open('./b.txt','w') asf2:
    data = f1.read()
    data = data.replace('a','A')
    f2.write(data)

```
-----------------------------------------------

# 函数
#### 无返回值
def 函数名():
    （函数体）

#### 有返回值
def 函数名():
    （函数体）
    return 返回值

#### 带参函数 
###### 默认参数
`形参可以带默认，例如（x=2）`
`默认参数可以是一个可变数据类型,如list、dic、tuple、set`
def 函数名(形参):  `可以为列表`
    （函数体）
    return 返回值

###### 不定长参数(元组)
`*args为关键字`
def fun1(name,age,*args):
    print(name)
    print(age)
    print(args)
    pass
t = ('a','b','c','d')   
（以元组的方式进行传输）
fun1(*t)  `传入实参时前面要加*`

###### 传入字典到函数
`dic为字典名`
def fun2(**dic):
    print(dic)
    pass
dic1 = {'name':'xiaoguo','age':23}
fun2(**dic1)    `传入实参时前面要加**`

###### 多种参数传递
`*args,**kwargs为关键字`
def fun3(a,v,*args,**kwargs):
    pass


#### 匿名函数
x = lambda y,z:y+z
`函数名为x，y、z为参数`

* 在函数内使用全局变量  `global a `
* list、dic、set、tuple可变的数据可以在函数中修改

#### 嵌套函数
* 应用上一层的变量,会改变上一层的值 `nonlocal b` 
def add_b():
    b = 1
    def do_global():
        b = 10
        def dd_nonlocal():
            nonlocal b 
            b = b+20
            print(b)
            pass
        dd_nonlocall()
        print(b)
        pass
    do_global()
    print(b)
    pass

    `结果为：30 30 10`

def max(x,y):
    m = x if x>y else y
    return m
    pass
def max4(a,b,c,d):
    mid1 = max(a,b)
    mid2 = max(mid1,c)
    mid3 = max(mid2,d)
    return mid3
    pass


#### 函数名代表为内存地址
* 所以函数名可以用变量代替
`不加括号为内存地址，加括号为运行`
def f1():
    print('i am fu1')
    pass
def f2():
    print('i am fu2')
    pass
def f3():
    print('i am fu3')
    pass

li = [f1,f2,f3]
dic = {'hanshu1':f1,'hanshu2':f2,'hanshu3':f3}

li[1]()
dic['hanshu3']()

#### 闭包函数
def func():
    name = 'xiaoguo'
    def inner():
        print(name)
        pass
    print(inner._closure_) `判断是否为闭包函数，如果是就返回cell，如果不是就none
    return inner
    pass

f = func()
f()

def wrapper():
    money = 1000
    def func():
        name = 'apple'
        def inner():
            print(name,money)
            pass
        return inner
        pass
    return func
    pass

f = wrapper()
i = f()
i()

###### 闭包传参
def func(a,b):
    def inner(x):
        return a*x+b
        pass
    return inner
    pass
f = func(4,5)
print(f(2))


import time
def func1():
    print('dai can bibao')
    pass
def timer(func):
    def inner():
        start = time.time()
        func()
        print(time.time()-start)
        pass
    return inner
    pass
f = timer(func1)
f()

# 装饰器
###### 不带参数
import time
def timer(fun):
    def inner():
        start = time.time()
        fun()
        print(time.time()-start)
        pass
    return inner
    pass

@timer
def func1():
    print('i am a zhuangshiqi')
    pass

###### 带参数的
def timer(fun):
    def inner(a):
        start = time.time()
        fun(a)
        print(time.time()-start)
        pass
    return inner
    pass

@timer
def func1(a):
    print('i am a zhuangshiqi')
    time.sleep(a)
    print('haha,sleep2')
    pass
fun1(2)


* 带不定长参数的
def func(fun):
    def inner(*args,**kwargs):
        fun(args,kwargs)
        pass
    return inner
    pass

@func
def func1(*args,**kwargs):
    print(args,kwargs)
    pass
func1('A','df',23,'fa23',name='xiaoguo',age='23')


###### 查看函数的本名称和注释
def func1():
    '''我是一个注释'''
    print('i am not a zhushi')
    pass
f = func1
print(func1.__doc__)   # 查看注释
print(f.__name__)      # 查看原函数名


###### 装饰器传参
def out(flag):
    def func(fun):
        def inner(a):
            if flag:
                print('it is begin')
                fun(a)
                print('it is down')
            else:
                print('it is doesnt begin')
            pass
        return inner
        pass
    return func
    pass

@out(True)
def func1(a):
    print(a)
    pass

func1('haha,i am back')

def first(fun):
    def inner():
        print('装饰器1被启动')
        fun()
        print('装饰器1被结束')
        pass
    return inner
    pass
def second(fun):
    def inner():
        print('装饰器2被启动)
        fun()
        print('装饰器2被结束')
        pass
    return inner
    pass
@first
@second
def func():
    print('i am a fun')
    pass

* 如果有两个装饰器被引用了，则运行顺序是：先运行第一个，然后运行第二个，再运行函数，再运行第二个，再运行第一个

-------------------------------------------------------------------

# 迭代器
* 判断迭代器
from collections import Iterable
l = [1,2,3,4]
s = {1,2,3,4}
d = {1:2,3:4}
t = (1,2,3,4)
print(isinstance(l,Iterable))
print(isinstance(s,Iterable))
print(isinstance(d,Iterable))
print(isinstance(t,Iterable))


* 迭代器迭代(一个一个的取提取)
l = [1,2,3,4]
l_iter = l.__iter__()
item = l_iter.__next__()
item1 = l_iter.__next__()
item2 = l_iter.__next__()
item3 = l_iter.__next__()
print(item)

* 异常捕获(try)
l = [1,2,3,4]
l_iter = l.__iter__()
while True:
    try:
        item = l_iter.__next__()
        print(item)
    except:
        print('捕获异常，break')
        break
* 如果try捕获异常就结束


# 标准python编写
# -*- coding=utf-8 -*-
def main()
    pass
if __name__ = '__main__'
    main()

-----------------------------------------------

# 生成器(yield,next())
* yield 把函数中断，再将结果return出去
def a_fun():
    a = 1
    print('将a赋值')
    yield a   # 将函数在这里中断，然后将a return 出来
    b = 2
    print('将b赋值')
    yield b
    pass

def main():
    a1 = a_fun()
    print(a1,next(a1))    将A打印出来
    print(next(a1))
    pass

if__name__=='__main__':
    main()


#### 包子生产线
def produce():
    for i in range (1,100):
        yield "生产了%s个包子"%i
    pass
def mian():
    p = produce()
    num = 0
    for i in P:
        print(i)
        num += 1
        if num == 10:
            break
    pass


#### yield 传参(g.send())
def gen():
    print(123)
    canshu = yield 1
    print('****',canshu)
    print(456)
    yield 2
    pass
def main():
    g = gen()
    ret1 = g.__next__()
    print(ret1)
    ret2 = g.send('haha,wo shi canshu')
    print(ret2)
    pass
if __name__ == __main__:
    main()

--------------------------------------------------------------

# 列表推导式 （尽量用一条线的式子表达出来）
#### 30以内可以被3整除
def mian():
    mul = [i for i in range(30) if i % 3 == 0]
    print(mul)
    pass
if __name__ == '__main__':
    main()

#### 利用函数列表推导式
* 30以内能被3整除数的平方
def squard(x):
    return x*x
    pass
def main():
    mul = [squard(i) for i in range(30) if i % 3 == 0]
    pass
if __name__ == '__main__'
    main()

# almond--杏仁，chestnut--栗子，date--红枣，coconut--椰子，
# fig--无花果，hazelnut--榛子，greengage--青梅，haw--山楂，kumquat--金桔
def main():
    fruits = [['apple','banana','orange',almond','chestnut','date','coconut'],['fig','hazelnut','grape','greengage','haw','kumquat']]
    print(name for lst in fruits for name in lst if name.count('a')>=2)
    pass
if __name__ == __main__:
    main()

# *********************
# 字典推导式(经典面试题)
# 将字典中的键值对对调
def main():
    dic1 = {'a':1,'b':2}
    dic2 = {dic1[k]:k for k in dic1}
    print(dic2)
    pass
if __name__ == '__main__:
    main()



# 集合推导式
def main():
    li = [1,2,3,4,-1,-2]
    s = {x*x for x in li}
    print(s)
    pass
if __name__ == '__main__'
    main()

-------------------------------------------------------------------------------


# python的内置函数(eval()、exec())

`eval`:执行字符串所代表的代码，并返回结果

* eval会打传入的字符串当作python的代码执行，有一定的安全风险
def main():
    a = input('Please input your name: ')
    print('Your name is: ',a)
    eval(a)    
    # 当输入的字符串为python可以执行的代码时，会直接执行该代码，例如(os.system('dir'))
    pass
if __name__ == '__main__'
    main()

**********************************************************************************

`exec`：所展示的效果和eval差不多
import os
def main():
    s = 'os.system('dir')
    print(s)
    exec(s)
    pass
if __name__ == '__main__':
    main()

#### 在Windows计算系统中添加新用户
import os
def main():
    s = 'os.system("net User 用户 密码 /add")'  # 在User下创建一个用户
    s2 = 'os.system("net localgroup Administrator 用户 /add")'  #将该用户给予最高权限
    exec(s)
    pass
if __name__ == '__main__'
    main()




# python的WEB框架 开发：1、django；2、flask
# www.stack overflow.com  编程问题社区


# 模块
* 每一个py文件都是一个模块
* 对于py文件的命名，必须避开关键字
* 在同目录下新建一个py文件

```
import test123  #引入外部的py文件
# import test123 as nn    # 取别名，调用nn.fun2()
# from test123 import fun1() # 只导入test123文件中的fun1（）函数
# from test123 import fun1(),fun2()  # 用逗号只导入fun1（）和fun2（）函数 
# from test123 import * # 导入test123文件中的所有，并且函数直接写(不严谨) 
def main():
    test123.fun2()  #使用引入的文件名，方法名调用
    #money = 1
    #print(money)  #先会去本地找，再去其它地方
    pass

if __name__ == '__main__'
    main()
```
* 如果调用函数和本地函数重名，则会先调用本地函数

* 在被引用的py文件里，考虑增加这个，限制对方访问某些方法
(这个操作只针对from test123 import *,其它引入方式不限制)
`__all__ = ['fun1','fun2']  # 在被引用的时候，只能用fun1和fun2`
(可以用来对付费和免费内容的应用)



# 包（packet）
* 新建一个目录（dir）pa，文件夹里面必须包含名字为__int__.py的文件
* 引入包
`import pa.test123`
* 使用包内的模块的函数
`pa.test123.fun1()
import pa.test123
def main():
    pa.test123.fun1()
    pass
if __name__ == __main__:
    main()


# **********************************************************************
# python自带的模块
* api(接口)  api.help.bj.cn/api/
#### json(传输数据)

```
import json
def main():
    dic1 = {'k1':'v1','k2':'v2','k3':'v3'}
    str = json.dumps(dic1)    #将字典进行序列化
    print(str)
    print(type(str))
    dic2 = json.loads(str)  #进行反序列化
    print(dic2)
    print(type(dic2))
    pass
if __name__ == __main__:
    main()

```

* 实列(从网上导入json字符串，并将之转化为字典)：
```
import json
def main():
    str1 = '{"status": "0","citye":"zhenjiang","city":"镇江","citycode":"101190301","aqi":"52","data": [{"add": "镇江","aqi": "52","pm25": "29","per": "良","lv": "2"},{"add": "新区办事处","aqi": "50","pm25": "28","per": "优","lv": "1"},{"add": "职教中心","aqi": "53","pm25": "37","per": "良","lv": "2"},{"add": "丹徒区监测站","aqi": "54","pm25": "31","per": "良","lv": "2"},{"add": "市疾控中心","aqi": "51","pm25": "20","per": "良","lv": "2"}]}'
    dic = json.loads(str1)
    print(dic)
    print(type(dic))
    for k in dic:
        print(k,'--->',dic[k])
    pass
if __name__ == '__main__':
    main()

```


# hashlib （摘要加密算法）
```
import hashlib
def main():
    md5 = hashlib.md5()    #使用MD5对以后的数据进行摘要加密操作
    md5.update('nihao xiaoguo'.encode('utf-8')) #对目标进行操作
    print(md5.hexdigest()) #结果是nihao xiaoguo的信息摘要加密的结果
    pass
if __name__ == '__main__':
    main()

```
* CMD5 BAES64


# configparser  (生成配置文件)
```
import configparser
def main():
    conf = configparser.ConfigParser()  #初始化
    conf['default'] = {'money':100,'go':'yes','weapon':'no'}
    conf['home'] = {'life':99}

    with open('./config','w') as f:
        conf.write(f)     #配置文件写入

    print('home' in conf)  #判断是否在配置文件中
    print(conf.options('default'))    #获取所有的键
    print(conf.get('default','money')) #获取值
    print(conf.items('default'))   #获取default下所有的键值对(列表中的元组)
    for k in conf['default']:
        print(k,'---',conf['defaut'][k])
    pass
if __name__ == '__main__':
    main()

```


#### 增、删、改、查 (应用与存储游戏数据)
```
import configparser
def main():
    conf = configparser.ConfigParser()  #初始化
    conf.read('config')  #读取配置文件
    
    conf.add_section('tank')   #增加section

    conf.remove_section('home')  #删除section

    conf.set('default','money','999')  #修改section下的值
    conf.set('default','weapon','tank') 

    conf.write(open('config','a'))   #存储
    pass
if __name__ == __main__:
    main()
```



# 定义坐标系
* namedtuple  (坐标，应用于游戏中人物的位置)
```
import collections import namedtuple

def main():
    pos = namedtuple('posi',['x','y'])   #定义名为pos的坐标 x，y
    p = pos(20,30)  #给坐标赋值
    print(p.x)    #访问坐标
    pass 
if __name__ == __main__:
    main()
```

# 简短列表
```
from collections import deque

def main():
    q = deque(['a','b','c','d'])
    print(q)
    q.append('e')   #在列表右边append
    q.appendleft('g')  #在列表左边append
    print(q)
    pass
if __name__ == __main__:
    main()
```


# time
```
import time
def main():
    print('hahah1')
    time.sleep(2)         #睡2秒
    print('hahah2')
    print(time.time())    #输出当前的时间戳（从1970开始到现在的时间）
    print(time.strftime('%Y-%m-%d %X'))    #输出当前的时间（24小时制）
    print(time.strftime('%Y-%m-%d %I'))    #12小时制
    print(time.strftime('%Y-%m-%d %H:%M:%S'))   #精确输出时间
    # 中间的字符可以随意改变（- , :）
    # Y=年份；m=月份；d=天；H=小时；M=分钟；S=秒钟
    print(time.strftime('%Z'))     #中国标准时间
    pass
if __name__ == '__main__':
    main()
```


# datetime   (可以用来计算会员的到期时间)
```
import time
import datetime
def main():
    now = datetime.datetime.now()      #精确到毫秒
    print(now)
    print(datetime.datetime.now() + datetime.timedelta(weeks = 3))  #3周之后
    print(datetime.datetime.now()+datetime.timedelta(weeks=-3))  #3周之前
    print(datetime.datetime.now()+datetime.timedelta(days=3)) #3天后
    print(datetime.datetime.now()+datetime.timedelta(seconds=3))  #3秒后
    print(now.replace(year=1970,month=2,day=12))
    tstamp = time.time()    #时间戳
    print(tstamp)
    print(datetime.date.fromtimestamp(tstamp))   #将时间戳转化为当前时间
    pass
if __name__ == '__main__':
    main()
```


# random （产生随机数）
```
import random
def main():
    print(random.random())         #产生一个0-1的随机数
    print(random.uniform(0,4))    #随机产生一个0-4（包含4.0000000）的数（包含小数）
    print(random.randint(1,5))    #随机产生一个1-5（包含5）的整数
    print(random.randrange(1,10,2))   #随机生成一个1-10之间的奇数
    ret = random.choice(['大王','黑桃A','方块K'])     #随机选定列表中的一个字符
    print(ret)
    # 在样本列表中随机选择2个样本
    a,b = random.sample(['梅花A','方块A','黑桃A','红桃A','大王','小王'],2)
    print(a,b)


    # 打乱顺序 (洗牌)
    item = ['梅花A','方块A','黑桃A','红桃A','大王','小王']
    random.shuffle(item)
    print(item)
    pass
if __name__ == '__main__':
    main()
```

#### 验证码
``` 
import random

def v_code():
    code = ''
    for i in range(5):
        num = random.randint(0,9)         #去整数
        alf = chr(random.randint(65,90))    #取大写字母
        lit = chr(random.randint(97,122))   #取小写字母
        add = random.choice([num,alf,lit])  #使用choice随机取一个
        code = "".join([code,str(add)])     #将取到的放入code字符串中
    return code
    pass

def main():
    print(v_code())
    pass
if __name__ == '__main__':
    main()
```




# os  sys  (系统模块)
```
import os
import sys
def main():
    print(os.getcwd())    #打印当前的工作目录
    #os.mkdir('mkdir_test')    #在当前目录创建文件夹
    #os.rmdir('mkdir_test')    #删除当前目录里的该文件夹
    ##使用系统的cmd命令
    #os.system('ipconfig')    #执行系统命令
    #print(os.popen('ipconfig').read())    #执行系统命令，用read读出后print出来（支持中文）
    print(sys.platform)      #打印目前操作系统平台
    print(sys.version)       #查看自己的python的版本
    pass
if __name__ == '__main__':
    main()
```





# 正则表达式 （re）

* '.'                 表示匹配任意字符一次;
* re.findall()        查找字符串中匹配条件的内容
* re.match().group()  完全的匹配这些内容
* re.search           匹配第一次匹配到的东西;
* re.match            完全的匹配(从开头就开始匹配一条)
* re.sub              替换匹配之后的数据
* re.complie          使用变量对正则表达式进行编译
* re.finditer         把正则表达式匹配的东西变成迭代器


` 匹配邮箱 ----- r'[a-zA-Z0-9]{4,20}@(163|126|qq|sohu)\.com$' `
` 匹配HTML ----- r'<(\w+)>\w+</\1>' `


```
import re    # 导入正则表达式模块

def main():
    s1 = r'abc'     #正则表达式
    #在字符转中寻找符合正则表达式表达的东西
    print(re.findall(s1,"afefegasdabcfsadfawefabcasfweafabfew"))

    s2 = r't[oi]p'     #匹配字符串中的top或者tip
    print(re.findall(s2, "afefegastopdabcfsadfatipwefabcasfweatopfabfew"))

    s3 = r'^abc'    #查找以abc开头的 (行首)
    print(re.findall(s3,"abcabcfaaef abwef faweac acbfea"))

    s4 = r'abc$'        #查找以abc结尾的
    print(re.findall(s4,'feawfajfjweagpabc'))

    s5 = r'abc\$'      #查找abc$，此时的$为一个转义字符，不会被执行，\为转义字符
    print(re.findall(s5,'faefawabc$vargarefarabc'))

    s6 = r'\d'       #匹配所有数字，\+d是匹配数字
    ##找到后以list输出
    print(re.findall(s6,'fafseafe13rfveg4f3g434g342g2'))

    s7 = r'\D'    #匹配所有的非数字
    print(re.findall(s7,'afefae2.32324g2g,2g24gfvv'))

    s8 = r'\s'    #匹配所有的空字符
    print(re.findall(s8,'fea faef fjae gaerg gea j'))

    s9 = r'\S'     #匹配所有非空字符
    print(re.findall(s9, 'fea faef fj32aev 322 gaerg gea j'))

    s10 = r'\w'    #匹配所有的字母和数字
    print(re.findall(s10,'fea23rf23%5rf.43t,42g()fewf!'))

    s11 = r'\W'   #匹配所有的符号
    print(re.findall(s11, 'fea23rf23%5rf.43t,42g()fewf!'))

    pass
if __name__ == '__main__':
    main()
```

#### 进阶正则表达式
* re.findall()    查找字符串中匹配条件的内容
* re.match().group() 完全的匹配这些内容
```
import re
def main():
    # sphone = r'^010-\d{8}'     #匹配以010-开头的后面有8位数字的电话号码
    # print(re.findall(sphone,'010-24987639 010-39825067'))
    # s1 = r'ab*'   #a,abb,abbbbbb,*代表多次
    # s2 = r'ab+'    #ab,abbbbb   +代表1到多次
    # s3 = r'ab?'    #a,ab    ?代表0或1次
    # s4 = r'ab{1,3}'   #ab,b(1-3)次
    # s5 = r'ab\d{1,3}'   #ab开头，后面是1-3个数字
    # print(re.findall(s5,'a ab dfa abbbb abb dager abbbbbbb ab1 ab12432 ab123 ab12'))
    s6 = r'[a-zA-Z0-9]{4,20}@(163|126|qq|sohu)\.com$'    #匹配邮箱
    ## match().group()匹配邮箱
    print(re.match(s6,'aBds123R@qq.com').group())
    pass
if __name__ == '__main__':
    main()
```


#### 高级版  (re.search().group()、re.sub())
```
import re
def main():
    # str = '阅读数：9991'
    # s1 = r'\d+'
    # # print(re.search(s1,str).group())    #提取文章的阅读数量
    # # print(re.sub(s1,'100',str))           #将提取出的数据替换成100
    str1 = 'afeawf<h1>hafewf</h1>faefage<div>nihao</div>safewaf'
    # s2 = r'<\w*>.*</\w*>'                   #html代码的匹配,.
    s3 = r'<(\w*)>.*</\1>'        #\1表示匹配与前面()里的内容一样的,匹配html
    print(re.search(s3,str1).group())
    pass
if __name__ == '__main__':
    main()
```



* '.'      表示匹配任意字符一次;
* re.findall  匹配所以
* re.search   匹配第一次匹配到的东西;
* re.match    完全的匹配(从开头就开始匹配一条)
* re.sub      替换匹配之后的数据
```
import re
def main():
    # print(re.findall('a.b','ab aab acb a*b ab aabbb a2b a.b asg ahb'))
    # print(re.search('a.b','ab aab acb a*b ab aabbb a2b a.b asg ahb').group())
    #print(re.match('a.b','aab acb a*b ab aabbb a2b a.b asg ahb').group())
    print(re.sub('abc','ABC','ffaefabcfaef afeabc afafebccewabc'))
    pass
if __name__ == '__main__':
    main()
```

* re.complie    使用变量对正则表达式进行编译
* re.finditer   把正则表达式匹配的东西变成迭代器
```
import re
def main():
    # obj = re.compile('\d{2}')
    # ## 以下内容用obj代替正则表达式
    # print(obj.search('abc323feafhahaha').group())

    ret = re.finditer('\d','abc123cde456')   #把正则表达式匹配的东西变成迭代器
    print(ret)
    print('first:',next(ret).group())
    print([i.group() for i in ret])
    pass
if __name__ == '__main__':
    main()
```

* 匹配html中的代码
```
import re

def main():
    str = 'feawf<h1>haha</h1>faefae<div>nihaoxiaoguo</div>faefaw'
    s1 = r'<(\w+)>\w+</\1>'       # 匹配html的代码
    ret = re.finditer(s1,str)     # 变成迭代器
    print(next(ret).group())
    print([i.group() for i in ret])
    pass
if __name__ == '__main__':
    main()
```





![image-20200622205431153](C:\Users\31650\AppData\Roaming\Typora\typora-user-images\image-20200622205431153.png)



![image-20200622211753668](C:\Users\31650\AppData\Roaming\Typora\typora-user-images\image-20200622211753668.png)
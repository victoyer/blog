# while循环

## <1>while循环的格式

```python
    while 条件:
        条件满足时，做的事情1
        条件满足时，做的事情2
        条件满足时，做的事情3
        ...(省略)...

```

demo

```python
    i = 0
    while i<5:
        print("当前是第%d次执行循环"%(i+1))
        print("i=%d"%i)
        i+=1

```

结果:python

```python
    当前是第1次执行循环
    i=0
    当前是第2次执行循环
    i=1
    当前是第3次执行循环
    i=2
    当前是第4次执行循环
    i=3
    当前是第5次执行循环
    i=4
```

# while循环应用

## 1. 计算1~100的累积和（包含1和100）

参考代码如下:

```python
#encoding=utf-8

i = 1
sum = 0
while i<=100:
    sum = sum + i
    i += 1

print("1~100的累积和为:%d"%sum)

```

## 2. 计算1~100之间偶数的累积和（包含1和100）

参考代码如下:

```python
#encoding=utf-8

i = 1
sum = 0
while i<=100:
    if i%2 == 0:
        sum = sum + i
    i+=1

print("1~100的累积和为:%d"%sum)
```

# while循环嵌套

- 前面学习过if的嵌套了，想一想if嵌套是什么样子的？
- 类似if的嵌套，while嵌套就是：while里面还有while

## <1>while嵌套的格式

```python
    while 条件1:

        条件1满足时，做的事情1
        条件1满足时，做的事情2
        条件1满足时，做的事情3
        ...(省略)...

        while 条件2:
            条件2满足时，做的事情1
            条件2满足时，做的事情2
            条件2满足时，做的事情3
            ...(省略)...

```

## <2>while嵌套应用一

要求：打印如下图形：

```python
    *
    * *
    * * *
    * * * *
    * * * * *

```

参考代码：

```python
    i = 1
    while i<=5:

        j = 1
        while j<=i:
            print("* ",end='')
            j+=1

        print("\n")
        i+=1

```

## <3>while嵌套应用二：九九乘法表

![img](/Img/Snip20161017_87.png)

参考代码：

```python
    i = 1
    while i<=9:
        j=1
        while j<=i:
            print("%d*%d=%-2d "%(j,i,i*j),end='')
            j+=1
        print('\n')
        i+=1
```
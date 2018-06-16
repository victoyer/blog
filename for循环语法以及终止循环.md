---
title:for循环语法以及终止循环
---

# for循环语法以及终止循环

像while循环一样，for可以完成循环的功能。

在Python中 for循环可以遍历任何序列的项目，如一个列表或者一个字符串等。

## for循环的格式

```
    for 临时变量 in 列表或者字符串等:
        循环满足条件时执行的代码
    else:
        循环不满足条件时执行的代码

```

## demo1

```
    name = 'dongGe'

    for x in name:
        print(x)

```

运行结果如下:

![img](/Img/Snip20161017_89.png)

## demo2

```
    name = ''

    for x in name:
        print(x)
    else:
        print("没有数据")

```

运行结果如下:

![img](/Img/Snip20161017_90.png)



# break和continue

## 1. break

### <1> for循环

- 普通的循环示例如下：

  ```
    name = 'dongGe'

    for x in name:
        print('----')
        print(x)

  ```

  运行结果:

  ![img](/Img/Snip20161017_92.png)

- 带有break的循环示例如下:

  ```
    name = 'dongGe'

    for x in name:
        print('----')
        if x == 'g': 
            break
        print(x)

  ```

  运行结果:

  ![img](/Img/Snip20161017_91.png)

### <2> while循环

- 普通的循环示例如下：

  ```
    i = 0

    while i<10:
        i = i+1
        print('----')
        print(i)

  ```

  运行结果:

  ![img](/Img/Snip20161017_94.png)

- 带有break的循环示例如下:

  ```
    i = 0

    while i<10:
        i = i+1
        print('----')
        if i==5:
            break
        print(i)

  ```

  运行结果:

  ![img](/Img/Snip20161017_93.png)

### **小总结:**

- break的作用：用来结束整个循环

## 2. continue

### <1> for循环

- 带有continue的循环示例如下:

  ```
    name = 'dongGe'

    for x in name:
        print('----')
        if x == 'g': 
            continue
        print(x)

  ```

  运行结果:

  ![img](/Img/Snip20161017_95.png)

### <2> while循环

- 带有continue的循环示例如下:

  ```
    i = 0

    while i<10:
        i = i+1
        print('----')
        if i==5:
            continue
        print(i)

  ```

  运行结果:

  ![img](/Img/Snip20161017_96.png)


- 小总结:
  - continue的作用：用来结束本次循环，紧接着执行下一次的循环

## 3. 注意点

- break/continue只能用在循环中，除此以外不能单独使用
- break/continue在嵌套循环中，只对最近的一层循环起作用

# 总结

- if往往用来对条件是否满足进行判断

- if有4中基本的使用方法：

  1. 基本方法

     ```
         if 条件:
             满足时做的事情

     ```

  2. 满足与否执行不同的事情

     ```
         if 条件:
             满足时做的事情
         else:
             不满足时做的事情

     ```

  3. 多个条件的判断

     ```
         if 条件:
             满足时做的事情
         elif 条件2:
             满足条件2时做的事情
         elif 条件3:
             满足条件3时做的事情
         else:
             条件都不满足时做的事情

     ```

  4. 嵌套

     ```
         if 条件:
             满足时做的事情

             这里还可以放入其他任何形式的if判断语句

     ```

- while循环一般通过数值是否满足来确定循环的条件

  ```
        i = 0
        while i<10:
            print("hello")
            i+=1

  ```

- for循环一般是对能保存多个数据的变量，进行便利

  ```
        name = 'dongGe'

        for x in name:
            print(x)

  ```

- if、while、for等其他语句可以随意组合，这样往往就完成了复杂的功能
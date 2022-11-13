### 输出指定范围内的素数
```python
lower = int(input('输入最小值: '))
upper = int(input('输入最大值: '))

for num in range(lower, upper+1):
    if num > 1:
        for i in range(2, num):
            if (num % i) == 0:
                break
        else:
            print(num)
```

### 阶乘
```python
num = int(input("输入一个数字: "))
factorial = 1

if num < 0:
    print('nagtive number')
elif num == 0:
    print('!0 = 1')
else:
    for i in range(1, num + 1):
        factorial = factorial * i
    print('%d 的阶乘为 %d' %(num, factorial))
```

### 99乘法表
单行
```python
print('\n'.join([" ".join([f'{j}*{i}={i * j}' for j in range(1, i + 1)]) for i in range(1, 10)]))
```

双循环:
```python
for i in range(1, 10):
    for j in range(1, i+1):
        print('{}x{}={}\t'.format(j, i, i*j), end= '')
```

### fib
```python
num=int(input("请输入要输出多少项："))
print("-------递归-------");
def Count_Function(n):
    if(n<3):
        return(n)
    else:
       return(Count_Function(n-1)+Count_Function(n-2))

i=1
while(i<=num):
    print(Count_Function(i),end="\t")
    i+=1
print()

#计算斐波那契数列，通过循环来实现
num=int(input("请输入您要显示的项数："))
print("-------循环-------");
n=3
a=[1,2]
if(num==1):
    print(a[0],end=" ")
elif(num==2):
    print(a[num-2],a[num-1],end=" ")
else:
    while(n<=num):
        temp=a[n-2]+a[n-3]
        a.append(temp)
        n+=1
    for i in a:
        print(i,end=' ')
print()
```


### 最大公约数
```python

# 定义一个函数
def hcf(x, y):
   """该函数返回两个数的最大公约数"""
 
   # 获取最小值
   if x > y:
       smaller = y
   else:
       smaller = x
 
   for i in range(1,smaller + 1):
       if((x % i == 0) and (y % i == 0)):
           hcf = i
 
   return hcf
 
 
# 用户输入两个数字
num1 = int(input("输入第一个数字: "))
num2 = int(input("输入第二个数字: "))
 
print( num1,"和", num2,"的最大公约数为", hcf(num1, num2))
```

### 最小公倍数
```python
def lcm(x, y):
 
   #  获取最大的数
   if x > y:
       greater = x
   else:
       greater = y
 
   while(True):
       if((greater % x == 0) and (greater % y == 0)):
           lcm = greater
           break
       greater += 1
 
   return lcm
 
 
# 获取用户输入
num1 = int(input("输入第一个数字: "))
num2 = int(input("输入第二个数字: "))
 
print( num1,"和", num2,"的最小公倍数为", lcm(num1, num2))
```

### 五人分鱼

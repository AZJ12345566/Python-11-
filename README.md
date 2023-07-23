# Python-11-
Python学习笔记(11)
# p38 while练习题_1到100之间的偶数和
‘’‘计算1到100之间的偶数和’‘’
‘’‘初始化变量’‘’
a=1
sum=0
'''条件判断'''
while a<=100:
    '''条件执行体(求和)'''
    #条件判断是否为偶数
    if a%2==0:  #这里也可以写成if not bool(a%2)
      sum+=a
    '''改变变量'''
    a+=1



# p39 for_in循环
#in表达从(字符串、序列等)中一次取值，称为遍历
#for-in的语法结构
for自定义变量 in可迭代对象：
   循环体

for item in 'Python':  #第一次取出来P，将P赋值给item，将item的值输出
    print(item)

#range()产生一个整数序列，->也是一个可迭代对象
for i in range(10):
    print(i)

#如果在这个循环体中不需要使用到自定义变量，可以定义自定义变量写为"_"
for _ in range(5):
    print('balabala')

print('使用for循环1计算1到100之间的偶数和')
sum=0  #用于存储偶数和
for item in range(1,101):
    if item %2==0:
        sum+=item
print('1到100之间的偶数和为',sum)



# p40 for_in练习题_100到999之间的水仙花数
for item in range(100,1000):
    ge=item%10
    shi=item//10%10  #//在Python里面是取整，这里拿153为例，十位要拿5，实现先取整10得出15，然后在取模得出5
    bai=item//100
    
    #判断
    if ge**3+shi**3+bai**3==item:
      print(item)

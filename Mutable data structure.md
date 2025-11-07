# Creation of list


```python
t=(0,10,20)
t[1]=30
print(t)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-1-6258a2793be9> in <module>
          1 t=(0,10,20)
    ----> 2 t[1]=30
          3 print(t)
    

    TypeError: 'tuple' object does not support item assignment



```python
t=[0,10,20]
t[1]=30
print(t)
```

    [0, 30, 20]
    


```python
l=[]
print(l)
print(type(l))
```

    []
    <class 'list'>
    


```python
l=eval(input("enter:"))
print(l)
print(type(l))
```

    enter:{1:'a'}
    {1: 'a'}
    <class 'dict'>
    

# creation of list by using list()


```python
l=list(range(0,3))
print(l)
```

    [0, 1, 2]
    


```python
s='python'
l=list(s)
print(l)
```

    ['p', 'y', 't', 'h', 'o', 'n']
    


```python
#creation of list by using split function
s="20-02-2025"
l=s.split('2')
print(l)
```

    ['', '0-0', '-', '0', '5']
    


```python
#access element of list
l=[10,30,40,50,10,60]
l[4]
#l[-8]
#l[10]
l[-4]
l[::1]
l[:7:1]
l[-1:-4:-1]
l[-1:-4:1]
```




    []




```python
l=[10,20,30,40,50,10,90]
print(l.count(10))

print(l.count(60))
print(l.index(10))
print(l.index(60))
```

    2
    0
    0
    


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-26-59cd37e62083> in <module>
          4 print(l.count(60))
          5 print(l.index(10))
    ----> 6 print(l.index(60))
    

    ValueError: 60 is not in list



```python
l=[1,2,3]
l.insert(9,100)
l.append(30)
print(len(l))
print(l)
```

    5
    [1, 2, 3, 100, 30]
    


```python
l1=[1,2,3]
l2=[4,5,6]
print(l1+l2)
```

    [1, 2, 3, 4, 5, 6]
    


```python
l1=[1,2,3,4]
l1.remove(4)
print(l1)

l1.clear()
print(l1)
```

    [1, 2, 3]
    []
    


```python
l1=[1,2,3,4]
l1.reverse()
print(l1)
```

    [4, 3, 2, 1]
    


```python
l1=[1,3,4,2]
l1.sort(reverse=True)
print(l1)
```

    [4, 3, 2, 1]
    


```python
l1=[1,3,4,2,'a',True,2.01]
l1.sort(reverse=True)
print(l1)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-27-f164186683a0> in <module>
          1 l1=[1,3,4,2,'a',True,2.01]
    ----> 2 l1.sort(reverse=True)
          3 print(l1)
    

    TypeError: '<' not supported between instances of 'str' and 'bool'



```python
l=[1,2,3,4,5]
for i in l:
    print(i)
```

    1
    2
    3
    4
    5
    


```python
l=[1,2,3,4,5]
i=0
while i<len(l):
    print(l[i])
    i+=1
```

    1
    2
    3
    4
    5
    


```python
l=['a','b','1','c']
l.sort()
print(l)
```

    ['1', 'a', 'b', 'c']
    


```python
l=[1,2,3,4]
l1=[4,5,6,7,8,9]
print(l+l1)
print(l*3)
```

    [1, 2, 3, 4, 4, 5, 6, 7, 8, 9]
    [1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4]
    


```python
l=[1,2,3,4]
print(4 in l)
```

    True
    


```python
l=[1,2,3,4]
print(5 not in l)
```

    True
    


```python
l=[1,2,3,4]
print(3 not in l)
```

    False
    


```python
l1=[1,2,3,4]
l2=[4,5,6,7]
l3=[8,9,10,11]
print(l1<l3)
print(l3>l2)
print(l2<l3)

```

    True
    True
    True
    


```python
l=['aa','lkwj','owik']
l1=['jehw','kskmsd','ioubgv']
print(l1<l)
```

    False
    


```python
l=[1,2,3]
temp=l
temp.insert(3,10)
temp[2]=100
print(temp)
print(l)
```

    [1, 2, 100, 10]
    [1, 2, 100, 10]
    


```python
#cloning by using slice and copy function
l=[1,2,3]
temp=l[:]
temp.insert(3,10)
temp[2]=100
print(temp)
print(l)
```

    [1, 2, 100, 10]
    [1, 2, 3]
    


```python
l=[1,2,3]
temp=l.copy()
temp.insert(3,10)
temp[2]=100
print(temp)
print(l)
```

    [1, 2, 100, 10]
    [1, 2, 3]
    


```python
l=[1,2,[3,5],6]
print(l)
print(l[2][1])
```

    [1, 2, [3, 5], 6]
    5
    


```python
l=dict(x:x**2 for x in range(0,10))
print(l)
```


      File "<ipython-input-52-c33bafef5c66>", line 1
        l=dict(x:x**2 for x in range(0,10))
                ^
    SyntaxError: invalid syntax
    



```python
l=dict{x:x**2 for x in range(0,10)}
print(l)
```


      File "<ipython-input-54-6ffe44638322>", line 1
        l=dict{x:x**2 for x in range(0,10)}
              ^
    SyntaxError: invalid syntax
    



```python
fruit=['apple','kivy','banana','ananas','blue berry']
l=[i for i in fruit if 'a' in i]
print(l)
```

    ['apple', 'banana', 'ananas']
    


```python
l=[1,2,3,4,5,6,7,8,9]
s=[x**2 for x in l]
print(s)
d=[i for i in s if i%2==0]
print(d)
```

    [1, 4, 9, 16, 25, 36, 49, 64, 81]
    [4, 16, 36, 64]
    


```python
l={1,2,3,4,5,6,7,8,9}
s={x**2 for x in l}
print(s)
print(type(s))
```

    {64, 1, 4, 36, 9, 16, 49, 81, 25}
    <class 'set'>
    


```python
l={1,2,3,4,5,6,7,8,9}
s={x:x**2 for x in l}
print(s)
print(type(s))
```

    {1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81}
    <class 'dict'>
    


```python
l=(1,2,3,4,5,6,7,8,9)
s=tuple(x**2 for x in l)
print(s)
print(type(s))
```

    (1, 4, 9, 16, 25, 36, 49, 64, 81)
    <class 'tuple'>
    


```python
s=['apple','kivy','banana','ananas','blue berry']
s.sort()
```


```python
a=[1,-1,3,5,-9,39,45]
a.sort(key=abs)
print(a)
```

    [1, -1, 3, 5, -9, 39, 45]
    


```python
d={10:"puppy",20:'c',30:'c'}
print(d)
```

    {10: 'puppy', 20: 'c', 30: 'c'}
    


```python
d.get(10)
```




    'puppy'




```python
d={10:"puppy",20:'c',30:'c'}
d[20]='d'
print(d)
```

    {10: 'puppy', 20: 'd', 30: 'c'}
    


```python
d[40]='e'
print(d)
```

    {10: 'puppy', 20: 'd', 30: 'c', 40: 'e'}
    


```python
d={10:"puppy",20:'c',30:'c'}
del d
print(d)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-20-e004ce4fec47> in <module>
          1 d={10:"puppy",20:'c',30:'c'}
          2 del d
    ----> 3 print(d)
    

    NameError: name 'd' is not defined



```python
d={10:"puppy",20:'c',30:'c'}
s=d.copy()
s[20]='e'
print(s)
```

    {10: 'puppy', 20: 'e', 30: 'c'}
    


```python
d.update(s)
print(d)
```

    {10: 'puppy', 20: 'e', 30: 'c'}
    


```python
print(d.values())
```

    dict_values(['puppy', 'e', 'c'])
    


```python
print(d.setdefault(40,'Ramesh'))
```

    Ramesh
    


```python
l=[1,2,3]
print(set(l))
```

    {1, 2, 3}
    


```python
s1={1,2,3}
s2={3,4,5}
print(s1.intersection(s2))
```

    {3}
    


```python

```

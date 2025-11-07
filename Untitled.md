# ch4 immutable data structure


```python
s="b9 is back"
print(id(s))
```

    2645483668720
    


```python
s="ramesh"
s1="suresh"
s3=3
s4="4"
print(s1+s)
print(s1+s3)
print(s1*s3)
print(s1*s3)
print(s1*s)
```

    sureshramesh
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-3-c13f8fab340b> in <module>
          4 s4="4"
          5 print(s1+s)
    ----> 6 print(s1+s3)
          7 print(s1*s3)
          8 print(s1*s3)
    

    TypeError: can only concatenate str (not "int") to str



```python
s="Armaan"
s1="armaan"
s2="arib"
s3="arman"
print(s>s1)
print(s<s3)
print(s==s1)
print(s!=s3)
print(s2<s)
```

    False
    True
    False
    True
    False
    


```python
s="learning python is very easy"
print(s[5])
print(s[-6])
s[15]
print(s[-30])
```

    i
    y
    


    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    <ipython-input-10-90ade50a9c8f> in <module>
          3 print(s[-6])
          4 s[15]
    ----> 5 print(s[-30])
    

    IndexError: string index out of range



```python
s="learning python is very easy"
print(s[6:])
print(s[0:7])
print(s[:7])
print(s[-1:-15:-2])#print(s[start:end:step])
```

    ng python is very easy
    learnin
    learnin
    ya rvs 
    


```python
s="akshat joshi"
s1="b9"
'#'.join(s1)
s2=['1','2','3']
'/'.join(s2)
```




    '1/2/3'



## imp functions of string


```python
#remove space
s="akshat joshi"
a=s.strip()
print(a)
```

    akshat joshi
    


```python
s="   akshat joshi"
print(s)
a=s.lstrip()
print(a)
```

       akshat joshi
    akshat joshi
    


```python
s="akshat joshi    "
a=s.rstrip()
print(a)
```

    akshat joshi
    


```python
s="akshat joshiiiii"
a=s.strip('i')
print(a)
```

    akshat josh
    


```python
s="   akshat joshi    "
print(s)
a=s.strip()
print(a)
```

       akshat joshi    
    akshat joshi
    


```python
s="akshat"
print(s.upper())
```

    AKSHAT
    


```python
s="AKSHAT"
print(s.lower())
```

    akshat
    


```python
s="akshat joshi"
print(s.title())
```

    Akshat Joshi
    


```python
s="akshat joshi"
print(s.capitalize())
```

    Akshat joshi
    


```python
s="Akshat JOSHI"
print(s.casefold())
```

    akshat joshi
    


```python
s="AkShAt"
print(s.swapcase())
```

    aKsHaT
    

## to check type of characters pesent in the string


```python
s="akshat"
s.isalpha()
```




    True




```python
s="akshat1"
s.isdigit()
```




    False




```python
s="akshat123"
s.isalnum()
```




    True




```python
s="akshat 123"
s.isalnum()
```




    False




```python
s="akshat joshi"
s.isalpha()
```




    False




```python
s="akshatjoshi"
s.isalpha()
```




    True




```python
s='     '
s.isspace()
```




    True




```python
s='ABC 1234'
s.isupper()
```




    True




```python
s='abc 1234'
s.islower()
```




    True




```python
s="Abc Efg 2345"
s.istitle()
```




    True




```python
s='int'
s.isidentifier()
```




    True




```python
s="__a"
s.isidentifier()
```




    True




```python
s="_ _a"
s.isidentifier()
```




    False




```python
s='-_-'
s.isidentifier()
```




    False




```python
s="o_o"
s.isidentifier()
```




    True




```python
import string
dir(string)
```




    ['Formatter',
     'Template',
     '_ChainMap',
     '_TemplateMetaclass',
     '__all__',
     '__builtins__',
     '__cached__',
     '__doc__',
     '__file__',
     '__loader__',
     '__name__',
     '__package__',
     '__spec__',
     '_re',
     '_sentinel_dict',
     '_string',
     'ascii_letters',
     'ascii_lowercase',
     'ascii_uppercase',
     'capwords',
     'digits',
     'hexdigits',
     'octdigits',
     'printable',
     'punctuation',
     'whitespace']




```python
print(string.punctuation)
```

    !"#$%&'()*+,-./:;<=>?@[\]^_`{|}~
    


```python
txt="welcome to python"
print(txt.find("to"))
```

    8
    


```python
txt="welcome to python"
print(txt.find("Python"))
```

    -1
    


```python
txt="welcome to python"
txt.find('e',0,3)
```




    1




```python
txt="welcome to python"
txt.count("e")
```




    2




```python
txt="welcome to python"
txt.count("a")
```




    0




```python
txt="welcome to python"
txt.count("o",0,10)
```




    2



# replace


```python
txt="welcome"
print(txt.replace("e","a",1))
print(txt.replace("o","c"))
print(txt.replace("E","A"))
```

    walcome
    welccme
    welcome
    

# split


```python
txt="welcome everybody"
s=txt.split("o",1)
print(s)
print(len(s))
```

    ['welc', 'me everybody']
    2
    


```python
# translate with make trans function
import string
print(len(string.punctuation))
a=str.maketrans('','',string.punctuation)
print(a)

```

    32
    {33: None, 34: None, 35: None, 36: None, 37: None, 38: None, 39: None, 40: None, 41: None, 42: None, 43: None, 44: None, 45: None, 46: None, 47: None, 58: None, 59: None, 60: None, 61: None, 62: None, 63: None, 64: None, 91: None, 92: None, 93: None, 94: None, 95: None, 96: None, 123: None, 124: None, 125: None, 126: None}
    


```python
s="gee@ks f@#r Ge_eks i$s ver_ imp"
s=s.translate(str.maketrans('G','%',string.punctuation))
print(s)
```

    geeks fr %eeks is ver imp
    

# Tuple


```python
t=(1,2,3,4,5,6,6,7,7)
print(type(t))
print(t)
```

    <class 'tuple'>
    (1, 2, 3, 4, 5, 6, 6, 7, 7)
    


```python
t=(1,2,3,4,5,6,6,7,7)
t[]
t[3:8]
```




    (4, 5, 6, 6, 7)




```python
t=(10,40,30,20,60,90)
t[1:-4:1]
```




    (40,)




```python
t=(10,40,30,20,60,90)
t[1:-4:-1]
```




    ()




```python
t=(10,40,30,20,60,90)
t[-1:-4:-1]
```




    (90, 60, 20)




```python
t=(10,40,30,20,60,90)
t[4:100:1]
```




    (60, 90)




```python
t=(10,40,30,20,60,90)
t[1:6:2]
```




    (40, 20, 90)




```python
t=(10,40,30,20,60,90)
t[2::]
```




    (30, 20, 60, 90)



# Mathematical operator in Tuple


```python
t1=(10,20,30)
t2=(40,50,60)
print(t1+t2)
print(t1*3)
```

    (10, 20, 30, 40, 50, 60)
    (10, 20, 30, 10, 20, 30, 10, 20, 30)
    

# main functions of tuple


```python
t=(10,90,60,20,40,30,10,10)
print(len(t))
t1=(10,60,40,30,10,60,30)
print(t1.count(60))
print(t1.count(20))
t1.index(30,4,6)
```

    8
    2
    0
    


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-73-91009ea5699e> in <module>
          4 print(t1.count(60))
          5 print(t1.count(20))
    ----> 6 t1.index(30,4,6)
    

    ValueError: tuple.index(x): x not in tuple



```python
t=(50,40,10,20,60,90)
sorted(t)
```




    [10, 20, 40, 50, 60, 90]




```python
t=(50,40,10,20,60,90)
sorted(t,reverse=True)
```




    [90, 60, 50, 40, 20, 10]




```python
t=(50,40,10,20,60,90)
min(t)
```




    10




```python
t=(50,40,10,20,60,90)
max(t)
```




    90



# tuple packaging and tupel unpackaging


```python
a,b,c,d=10,20,30,40
t=a,c,d,b
print(t)
```

    (10, 30, 40, 20)
    


```python
t1=(10,90,60,40)
a,b,c,d=t1
print(a)
```

    10
    


```python
t1=(10,90,60,40)

list(reversed(t1))
```




    [40, 60, 90, 10]




```python
t1=(10,90,60,40)

tuple(reversed(t1))
```




    (40, 60, 90, 10)




```python
t1=(10,90,60,40)

set(reversed(t1))
```




    {10, 40, 60, 90}




```python
t1=(10,40,60,40)

set(reversed(t1))
```




    {10, 40, 60}




```python
t1=(10,90,60,40)

(reversed(t1))
```




    <reversed at 0x24890aaaa00>




```python
#enumerate function
t1=(10,90,60,40)
enumerate(t1)
```




    <enumerate at 0x248902e16c0>




```python
#enumerate function
t1=(10,90,60,40)
list(enumerate(t1))
```




    [(0, 10), (1, 90), (2, 60), (3, 40)]




```python
#enumerate function
t1=(10,90,60,40)
print(enumerate(t1))
```

    <enumerate object at 0x00000248902E9480>
    


```python
#enumerate function
t1=(10,90,60,40)
list(enumerate(t1,2))
```




    [(2, 10), (3, 90), (4, 60), (5, 40)]




```python
#wap to find out length of string without using len function
s=input("enter your name:")
count=0
for i in s:
    print(i)
    count+=1
print("count:",count)
    
```

    enter your name:akshat
    a
    k
    s
    h
    a
    t
    count: 6
    


```python
#wap to check whether the given string is palindrome or not using function
def pali(s):
    if s == s[::-1]:
        print("palidrome")
    else:
        return s
pali(input("enter string:"))
        
```

    enter string:akshat
    




    'akshat'




```python
str=input("enter string:")
u=0
sy=0
s=0
d=0
for i in str:
    match str:
        case 1:i == (/s):
                s+=1
                print(s)
        case 2: i == ("A-Z")
                u+=1
                print(u)
        case 3:i == (0-9):
                d+=1
                print(d)
        case 4:i == (str.puctuation):
                sy+=1
                print(sy)

                
```


      File "<ipython-input-12-bb1eaf53e843>", line 7
        match str:
              ^
    SyntaxError: invalid syntax
    



```python
str=input("enter string:")
count = 0
sum=0
div=0
for i in str:
    if i.isdigit():
        count+=1
        sum=sum+count
        div=sum/5
print(div)

```

    enter string:ak12345
    3.0
    


```python
s="akshat"
sub="a"
if s.find(sub) == -1:
    print("not found")
```


```python
str=input("enter string:")
output=""
a=0
for i in str:
    a=len(str)/2
    output=(str[int(a)])
print(str[0],output,str[-1])
```

    enter string:shlok
    s l k
    


```python
str="ak"
print(str[-1])
```

    k
    


```python
"""s1=input("enter string:")
s2=input("enter string:")
output=""
if len(s1) == len(s2):
#bane string add thavi joie akshat aksht hoy to aa kk ss evi rite"""
```




    's1=input("enter string:")\ns2=input("enter string:")\noutput=""\nif len(s1) == len(s2):\n#bane string add thavi joie akshat aksht hoy to aa kk ss evi rite'




```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

str=input("enter string:")
d=""
a=""
b=""
for i in str:
    if i.isalpha():
        a+=i
    elif i.isdigit():
        b+=i
    else:
        d+=i
fs=a+b+d
print(sorted(fs))
```

    enter string:ak@1
    ['1', '@', 'a', 'k']
    


```python
"""wap to check the validity of password (primary requirement for password validation is as below:)
lenght of pass is greater or equal to 8,the alphabet must be between small a-z,atleast one alphabet should be in uppercase,atleast 1 digit,atleast 1 character from @,#,_"""
a=input("enter password:")
b=len(a)
l,u,d,s=0
if len(a)== 8:
    for i in a:
        if i.isupper():
            u+=1
        elif i.isdigit():
            d+=1
        elif i == '@' or i=='_' or i=='#':
            s+=1
    if l>=1 and u>=1 and d>=1 and s>=1:
        print(a)
else:
    print("invalid")
        
    
```

    enter password:AKi@1234
    AKi@1234
    


```python
s=input("enter string:")
output =''
previous=''
for i in s:
    if i.isalpha():
        output=output+i
        previous=i
    else:
        output=output+(previous*int(i-1))
print(output)
```

    enter string:a2c3
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-25-75e581fff3a4> in <module>
          7         previous=i
          8     else:
    ----> 9         output=output+(previous*int(i-1))
         10 print(output)
    

    TypeError: unsupported operand type(s) for -: 'str' and 'int'



```python
#Wap find out minimum and maximum number from the tuple given by user without using inbuilt function

```


```python

```

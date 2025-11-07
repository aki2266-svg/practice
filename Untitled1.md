```python
S="hello world this is python"
o=" "
for i in S:
    if i!=" ":
        o+=i
print(o)
```

     helloworldthisispython
    


```python
for i in S:
    if i==" ":
        continue
    else:
        print(i,end='')
```

    helloworldthisispython


```python
#WAP TO COUNT NUMBER OF WORDS IN A STRING
count=0
for i in S:
    if i==" ":
        count+=1
print(count)
```

    4
    


```python
#WAP TO REMOVE PUNCTUATION FROM A STRING 
st="Hello,python is . fun,!"
p=".,!\():;"
for i in st:
    if i in p:
        continue
    else:
        print(i,end="")
print("\n another method : ")
for i in st:
    if i not in p:
        print(i,end="")
```

    Hellopython is  fun
     another method : 
    Hellopython is  fun


```python
#WAP TO COUNT WORD FREQUENCY 
A="hello i like apple fruit but my frnd likes , also i dont like orange fruit , he like mango along with apple "
words=A.split()
print(words)
print(type(words))
a=0
b=0
c=0
d=0
for i in words:
    if i=="apple":
        a+=1
    if i=="banana":
        b+=1
    if i=="orange":
        c+=1
    if i=="fruit":
        d+=1
print("apples : ",a)
print("banana : ",b)
print("orange : ",c)
print("fruits : ",d)
```

    ['hello', 'i', 'like', 'apple', 'fruit', 'but', 'my', 'frnd', 'likes', ',', 'also', 'i', 'dont', 'like', 'orange', 'fruit', ',', 'he', 'like', 'mango', 'along', 'with', 'apple']
    <class 'list'>
    apples :  2
    banana :  0
    orange :  1
    fruits :  2
    


```python
A=input("enter a string : ")
words=A.split()
o=[]
for i in range(len(words)):
    if words[i] not in o:
        count=1
        for j in range(i+1, len(words)):
            if words[i]==words[j]:
                count+=1
        o.append(words[i])
        print(words[i],":",count)
```

    enter a string : hello world 
    hello : 1
    world : 1
    


```python
A=input("enter a string : ")
words=A.split()
o=[]
for i in range(len(A)):
    if A[i] not in o:
        count=1
        for j in range(i+1, len(A)):
            if A[i]==A[j]:
                count+=1
        o.append(A[i])
        print(A[i],":",count)
```

    enter a string : hello hello
    h : 2
    e : 2
    l : 4
    o : 2
      : 1
    


```python
#WAP TO FIND THE LONGEST WORD FROM A STRING 
A=input("enter a string : ")
words=A.split()
print(words)
longest=words[0]
for i in words:
    if len(longest)<len(i):
        longest=i
print(longest)
print("\nAnother method\n")
longest=max(A.split(), key=len)
print(longest)
```

    enter a string : 
    []
    


    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    <ipython-input-24-db9256397f9c> in <module>
          3 words=A.split()
          4 print(words)
    ----> 5 longest=words[0]
          6 for i in words:
          7     if len(longest)<len(i):
    

    IndexError: list index out of range



```python
#WAP TO REPLACE A WORD WITHOUT USING REPLACE FUNCTION
STR=input("enter a string: ")
h=input("enter a word to replace: ")
k=input("enter the word to store: ")
STR.replace("can","cann")
x=STR.split()
for i in range(len(x)):
    if x[i]==h:
        x[i]=k
O=" ".join(x)        
print(O)
```

    enter a string: hello worls
    enter a word to replace: worls
    enter the word to store: world
    hello world
    


```python
#WAP TO FIND REPEATING CHR
A=input("enter a string : ")
words=A.split()
o=[]
for i in range(len(A)):
    if A[i] not in o:
        count=1
        for j in range(i+1, len(A)):
            if A[i]==A[j]:
                if s[i]>s[j]
                    count+=1
                    o.append(A[i])
                    print(A[i],":",count)
```


```python


```

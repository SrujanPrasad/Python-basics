# Python Programming Basics

## First program
```python
print("Hello srujan")
```
## To gather input from user
```python
x=input("Enter your name ")
print('Hi ' +x)

name=input("Enter your name :")
color=input("Enter your favourite color :")
print(name + ' likes ' + color)
```
## Typecasting- converting from one datatype to another
```python
birthyear=input("Enter your birthyear ")
print(type(birthyear))  #denotes the type of the datatype
age=2025-int(birthyear)
print(type(age))
print(age)

weight=input('Enter your weight is kilograms')
weight_grams=float(weight)*1000
print(weight_grams)

height=input('Enter your height in cm');
height_in_m=float(height)*100
print(height_in_m)
```

## String
```python
course='Python for all beginners'
print(course[12] + course[15] + course[-2]) # -2 returns
# second character from the end

course_new=course[:] # copying the string
print(course_new)

name='Jennifer'
print(name[1:-1])

```
## Formatted strings
```python
first='Srujan'
last='Prasad'
message=f'{first} [{last}] is a student'
print(message)
```
## To print length of a string
```python
name="ABCDEFGHIJKLMOPQRSTUVWXYZ"
print(len(name))
```
## To convert string to upper and lowercase
```python
name='India is a large country'
print(name.upper())         #upper() for converting to uppercase
print(name.lower())   #lower() for converting to lowercase
print(name.replace('large','very large')) #replace words
print(name.replace('i','I'))
print('IS' in name)  #for checking whether the word is present in the variable
```
## Arithmetic operators
```python
a=10
b=5
print(a+b)
print(a-b)
print(a*b)
print(a/b) #floating point
print(a//b) #integer value
print(a%b)
print(a**b) #exponent operator
```
## Assignment operators - += -= *= /= %=
```python
a=10
a+=a    #a=a+a
print(a)
a-=a    #a=a+a
print(a)
```
## Operator precedence - exponentiation , multiplication or division ,  addition or subtraction
```python
a=10+16//4
print(a)
x=(2+3) * 10-3
print(x)
```

## Math functions - round(),abs()
```python
import math
x=2.9
print(round(x))
print(abs(x))
print(math.ceil(x))
print(math.floor(x))
```

## Conditional statements -if,elif,else
```python
is_hot=True
is_cold=False
if is_hot:
    print('Its a hot day \nDrink plenty of water')
elif is_cold:
    print('Its a cold day \nWear warm clothes')
else :
    print('Its a lovely day')

price=1000000
is_goodcredit=False
if is_goodcredit:
    price=price*(10/100)
else :
    price=price*(20/100)
print(f"Downpayment is ${price}")
```

## Logical operators - and,or,not
```python
highincome=False
goodcredit=True
if highincome and not goodcredit:
    print('Eligible for loan')
elif highincome or goodcredit:
    print('not eligible for loan')
else:
    print('Thank you')
```

## Comparison operators - >,<,>=,<=,=,!=
```python
temperature=35
if temperature>35:
    print('Its very hot day')
else:
    print('Its not a hot day')
    
name=input("Enter your name ")
x=len(name)
if x<3:
    print('Name must be atleast 3 characters long')
elif x>50:
    print('Name can be a maximum of 50 characters')
else:
    print('Name looks good!')
```

## Weight converter game
```python
weight=input('Enter your weight :')
choice=input("(L)lbs or (K) kg ? :")
if choice=='l' or choice=='L' :
    your_weight=float(weight)/2.2
    print(f"Your weight in kg is {your_weight}")
elif choice=='k' or choice=='K':
    your_weight=float(weight)*2.2
    print(f"Your weight in pounds is {your_weight}")
else:
    print('Incorrect choice')
```

## Loop statements - while , do while , for
```python
i=0
while(i<5):
    print('*'*i)
    i+=1
print("Printed")
```

## Guess game using while loops
```python
secret=9;
Guess=0
guess_limit=3
while Guess<guess_limit:
    guess=int(input('Guess :'))
    Guess += 1
    if guess==secret:
        print('You won ')
        break
else:
    print('You lose')
```
## Multi line string
```python
print("""Hi ABCD
Welcome to our python tutorial
hope you gave fun""");      #multiline string 
```
## For loops
```python
for x in "Helloworld" : #print all the letters
    print(x)

for y in range(8,10):        #to print certain range of numbers we use the range function
    print(y)

total=0
for prices in [10,20,30]:
    total+=prices
print(f"The total price is {total}")

#sum of first 10 natural numbers
sum=0
for i in range(10):
    sum+=i
print(f"the sum is {sum}")

#sum of first 10 even numbers
sum=0
for i in range(10):
    if i%2==0:
        sum+=i
print(f"the sum is {sum}")

#sum of first 10 odd numbers
sum=0
for i in range(10):
    if i%2!=0:
        sum+=i
print(f"the sum is {sum}")
'''

#nested for loops
#generate coordinates
'''
for x in range(4):
    for y in range(3):
        print(f"({x},{y})")

numbers=[2,2,2,2,6]
for x in numbers:
    output=''
    for y in range(x):
        output+='x'
    print(output)

#star pattern
stars=[1,2,3,4]
for x in stars:
    output=''
    for y in range(x):
        output+='*'
    print(output)
#inverted star
stars=[4,3,2,1]
for x in stars:
    output=''
    for y in range(x):
        output+='*'
    print(output)
```
## Lists
```python
names=['A','B','C','D']         # []
print(names[2:])

#to find largest of numbers
numbers=[10,12,15,1]
max=numbers[0]
for x in numbers:
    if x>max:
        max=x
print(max)

#to find smallest of numbers
numbers1=[10,20,24,32]
min=numbers1[0]
for y in numbers1:
    if y<min:
        min=y
print(min)
```
## 2d lists
```python
matrix = [
    [1,2,3],
    [4,5,6],
    [7,8,9]
]
matrix[0][1]=20
matrix[1][2]=40
print(matrix[0][1])
print(matrix[1][2])

numbers1=[209,15,24,322]
numbers1.sort()         #to sort the numbers
print(numbers1)

#program to remove duplicates in a list
numbers2=[10,12,10,100]
uniques=[]
for x in numbers2:
    if x not in uniques:
        uniques.append(x)
print(uniques)
```

## Tuples
```python
numbers=(1,2,3)
numbers[0]=10   #we cannot change the contents of a tuple 'tuple' object does not support item assignment
print(numbers[0])
```

## Dictionaries
```python
customer={
    "name":"ABC",
    "age":12,
    "is_verified":True,
    "DOB":"7 JAN 1900"
}
print(customer.get("age"))      # to get the information from a dictionary we use get()
print(customer.get("DOB"))
```





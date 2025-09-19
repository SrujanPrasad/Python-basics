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





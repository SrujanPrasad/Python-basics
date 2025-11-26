# Python Programming Basics

## First program
```python
print("Hello srujan")
```
## To gather input from the user
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

a=input('Enter first number : ')
b=input('Enter the second number :')
sum=int(a)+int(b) #typecasting from string to int
print("The sum is :" + str(sum))
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

name="Tony Stark"
print(name.find('K'))    # returns the index of the letter to find if found else returns -1
print(name.replace('Tony Stark','Iron Man'))
print('S' in name) #returns either true or false

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
a*=a    #a=a+a
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

## Conditional statements -if,elif, else 
Here, indendations are given instead of the curly braces.
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

## Mini Calculator
```python
a=input('Enter the first number :')
b=input('Enter the second number :')
ch=input("Enter the choice from 1-5 :");
if ch=='1':
    print(int(a)+int(b))
elif ch=='2':
    print(int(a)-int(b))
elif ch=='3':
    print(int(a)*int(b))
elif ch=='4':
    print(int(a)/int(b))
elif ch=='5':
    print(int(a)%int(b))
else:
    print('Enter valid choice')
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

## Comparison operators - >,<,>=,<=,==,!=
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

i=10  #print reverse
while(i>0) 
    print("*" *i)
    i-=1
print("Printed")

name="srujan prasad"
vowels="aeiouAEIOU"
count=0
for ch in name :
    if ch in vowels:
        count+=1
print(count)
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

marks=[98,99,100]
print(marks[0:2])

marks.append(90)
print(marks)

marks.insert(1,89)
print(marks)

marks.clear()        # deletes the contents of the list
print(marks)

students=['A','B','C','D','E','F']
for i in students:
    if i=="D":
        break
    print(i)

students=['A','B','C','D','E','F']
for i in students:
    if i=="C":
        continue
    print(i)
    
    
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
numbers[0]=10   #we cannot change the contents of a tuple 'tuple' object does not support item assignment, they are immutable
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

student={"name" :"A" , "age" : 21}
print(student["age"])
```
## Functions
```python
def first_fun():            #def function_name() :
    print("Hello World")
    print("This is the first function")
first_fun()     #function can be called only after the function has been defined

#calculator using functions
def calculator(a,b):            #the variables inside the function are called as the parameters
    print(a+b)  #sum
    print(a-b)  #difference
    print(a*b)  #product
    print(a//b) #divide
    print(a%b)  #remainder
    print(a*a)  #square
print("The results are :")
calculator(10,5)

def names(first_name,last_name):
    print("The first name is :"+first_name)
    print("The last name is :"+last_name)
names("ABC","DEF")

def printSum(a,b):
    print(int(a)+int(b))
printSum(1,2)
```

## Exceptions -try and except
```python
try:                                        #try block executes the normal statements
    age=int(input(">Enter your age:"))
    print(age)
except ValueError:                          #exception tells what to do when an error occurs
    print("Invalid value")

#division by 0
try:
    a=int(input("Enter num1:"))
    b=int(input("Enter num2:"))
    div=a/b
    print(div)
except ZeroDivisionError:
    print('Cannot divide by 0')
```

## Comments
#followed by the text

## Class
```python
class new:                  #class class_name
    def move(self):
        print("move")
    def draw(self):         #methods of a particular class
        print("draw")
new1=new()
new1.move()
new1.draw()
```

## Constructors
```python
class Person:
    def __init__(self,name):        #this is a constructor
        self.name=name
    def talk(self):
        print("talk")
x=Person("ABC")
x.talk()
print(x.name)
```
## Inheritance
```python
class Mammal:
    def walk(self):
        print("walk")
class Dog(Mammal):
    pass

class Cat:
    def walk(self):         #this is a function in the cat class
        print("Cats meows")
dog1=Dog()
dog1.walk()
cat1=Cat()
cat1.walk()
```

## Modules
```python
import convertors           #this is another Python file
from convertors import pounds_to_kg     #importing only required function
print(pounds_to_kg(100))


import utilis           #utilis is a separate file for minimizing complexity
numbers=[10,20,2,189]
print(utilis.find_max(numbers))
print(utilis.find_min(numbers))

import math
from math import sqrt
print(sqrt(25))
```

## packages
```python
from ecommerce import shipping
shipping.calc_shipping()    #second way
#ecommerce.shipping.calc_shipping()
```

## To generate random numbers
```python
import random               #predefined function
for i in range(4):
    print(random.randint(1,10))
members=['A','B','C','D','E']
leader=random.choice(members)       #choice is a predefined method in random
print(leader)
```

## To roll a die using random module
```python
import random
class Dice:
    def roll(self):
        first=random.randint(1,6)
        second=random.randint(1,6)
        return first,second

dice=Dice()
print(dice.roll())
```

## To toss a coin using random module
```python
import random
class Coin:
    def result(self):
        choice=['Heads','Tails']
        result=random.choice(choice)
        return result
coin=Coin()
print(coin.result())
```




### Function Structure and Values

#### Structure and Value

###### basic function with no argument
```
def simple():
    print("this is a function")
```
###### calling function
simple()

output -> this is function

###### watch out for function that don't return values
```
result = simple()
print("the value of result is:", result)
```

output ->
this is a function
The value of result is: None


#### if you need a value from a function, function must return
```
def produce():
    return "This value!"
```

#### calling it allows capturing the result product
```
result = produce()
print("This result value is:", result)
```
output -> The result value is: This value!


##### a function definition with required arguments
```
def squared(number):
    return number**2
```
squared(4)

output -> 16

#### 'keyword argument' 
```
def greeting(full_name="john doe"):
    print("Greeting ", full_name)

greeting()
greeting("Superman!")
```
output ->
Greeting john doe <br>
Greeting Superman!


##### arguments always go before keyword arguments
```
def format_greeting(name, title="Dr,"):
    print("Greetings", title, name)
format_greeting("Jenkins", title="Sr.")
```
output -> Greeting Sr. Jenkins

### Variable arguments and keyword arguments

#### this function can take 0 or more arguments

```
def family_members(*args):
    for name in args:
        print(name)

family_members("Lucy", "Matt", "Bob")
```

Output ->

Lucy
Matt
Bob

#### define a function that takes 0 or more keyword arguments
```
def stats(**kwargs):
    # kwargs is now a dictionary
    for key, value in kwargs.items():
        print(key, "--->", value)

stats(quick="slow", active=False, weight=210)
```

## Introduction to Class

#### the most basic class
```
class Basic:
    pass
basic = Basic()
```

### use dir() to find about what is available in class
```
dir(basic)
```

#### class in general are good when grouping code and behaviour 

```
class Dog():
    is_animal = True

    def bark(self):
        print("woof")
dog = Dog()

dog.bark()
dog.is_animal
```

#### you can create many instances
ruful = Dog()
ruful.bark()

### class attri
Dog.is_animal = False
print("Is ruful an animal", ruful.is_animal)


##### What is self? 

pass self statement in the method

### Using a constructor
##### The constructor in python is with __init__

```
class Dog:
    def __init__(self):
        self.is_animal = True

dog = Dog()
dog.is_animal

```

#### two instances variables are only for the object and you can't affect other objects

```
ruful = Dog()
sparky = Dog()

print("Ruful is an animal?", ruful.is_animal())
print("Sparky is an animal?", sparky.is_animal())

```

output ->
Ruful is an animal? True
Sparky is an animal? True


### State
##### pass arguments, keywords argument to a class

```

class Animal():
    def __init__(self, name, legs=4, barks=True):
        self.name = name
        self.legs = legs
        self.barks = barks

    def info(self):
        print(f"This is an animal {self.name}, has {self.legs} legs")
        if barks:
            print("Add this bark here")
        else:
            print("No bark")
            
bunny = Animal("buster", barks=False)
bunny.info()

print(bunny.name)
print(bunny.legs)
print(bunny.barks)

```
output ->
buster
4
False


### Adding Methods

### class with two methods
```
class Budget():
    def __init__(self, budget):
        self.budget = budget
    
    def expense(self, amount):
        self.budget = self.budget - amount
        print(f"Budget left: {self.budget} ")

    def report(self, currency="$"):
        print(f"Budget is: {currency}{self.budget}")
april_budget = Budget(100)
april_budget.expense(34)
```

### Class Inheritance

##### create a base class
```
class Pet:
    def eat(self):
        self.found = self.food - self.appetite
        print(f"Ate {self.appetite} of food, have {self.food} left")

```
##### create a child class for other house pets 
```
class Parakeet(Pet):
    def __init__(self):
        self.food = 100
        self.appetite = 1

class Dog(Pet):
    def __init__(self):
        self.food = 100
        self.appetite = 2

perry = Parakeet()
rufus = Dog()
```
output ->
Ate 1 of food, have 99 left
Ate 2 of food, have 98 left


#### Demo other classes have method
```
for attribute in dir(rufus):
    if attribute.startswith('_'):
        continue
    print(attribute)
    
```
output ->
appetite
eat
food

#### Use of unittest
```
import unittest

class Testing(unittest.Test(case)):
    pass
test = Testing()


for attribute in dir(test):
    if attribute.startswith('_'):
        continue
    print(attribute)
```
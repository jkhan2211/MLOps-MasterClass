### Function Structure and Values

#### Structure and Value

###### basic function with no argument

def simple():
    print("this is a function")

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


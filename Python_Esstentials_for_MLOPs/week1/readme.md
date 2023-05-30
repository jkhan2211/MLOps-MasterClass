# Week 1

1- Working with Variables and Types

2- Intro to Python Data Structures
Introduction to Python: lists

#### list are containers of items
```[1, 2, 3, 4, 5]```

##### lists can contain different types of tems
```[1, "two", False, 12.4]```

#### built-in count item in a list
```len([3, 4, "red", "car"])```


#### each item has a position called "index"
```items = ["carrots", "pasta", "lasagna"]```
#### retriving an item is done with index
```items[1] -> pasta```

#### you can retrieve last item
```items[-1] -> lasagna```


Creating and Iterating over Lists
```
items = []
items
```
```
items = lists()
items
```

#### data can be pre-seeded
```
colors = ["red", "blue", "green"]
colors
```

##### Iterating over Lists
```
for color in colors:
    print(color)
```
-> prints every colour in list above



##### List Comprehensions 
```
numbers = [2, 3, 4, 12, 5, 3, 4]

low_numbers = [n for n in numbers ]
```



## Introduction to dictionaries 

#### dictionary is a mapping of item

```{} - phone book```

#### you always map a key to a value 
```{"key": "value"}```

#### can be other type 
```{"key": True}```

#### has to be unique cant be duplicates

#### you cant have a list or a dict as a key however
```{[1,2]: False} -> type error```

#### Creating and Iterating over Dictionaries

with curly brackers
```contact_info = dict()```

with dict()
```data = [("name","alfredo"),("lName","kh")]```


```
contact_info = {

"name": "Alfredo"
"lastN": "Data"
"age" : "20"
}
```
```
for key in contact_info:
    print(key)

```

##### retrieve only values
```
for value in contact_info.value():
    print(value)
```

#### Retrieve both keys and values

```
for key, value in contact_info.items():
    print(f"{key} -> {value}")
```

## Tuples and Sets 

## Tuples
Should be treated as "read only" lists, difference is subtle

```
ro_items = ('first', 'second', 'third')
print("first item in the tuple is: %s" % ro_items.index('first'))
print(ro_items[-1])
for item in ro_items:
    print(item)
```

Output: 
first item in the tuple is: 0
third
first
second
third

### find out what methods are available in tuple
```
for method in dir(tuple()):
    if method.startswith('__'):
        continue
    print(method)
```

## Sets
### Create an empty set
look like dictionary, allow us to keep unique items
```unique = set()```

```unique.add("one")```
unique

output -> {'one'}

You can pop items, unlike list, does not take arguments
```unique.pop()```
unique
output -> set{}

3- Adding and Extracting Data from Data Structure 

#### Adding Data to Lists 
```fruits = []```
```
fruits.append("orange")
fruits.append("apple")
```
output -> ['orange', 'apple']

```fruits.insert(0, 'melon')```

output -> ['melon', 'orange', 'apple']


#### You can add one list to another one
```
vegetables = ["cucumber", "carrots"]
fruits + vegetables
```
output -> ['melon', 'orange', 'apple', 'cucumber', 'carrots']

#### Watch out when appending list to an existing list
```
shopping_list = fruits + vegetables
shopping_list.append(["sugar", "salt"])
shopping_list
```
output -> ['melon', 'orange', 'apple', 'cucumber', 'carrots', ['sugar', 'salt']]

#### Watch out when appending list to an existing list
```
shopping_list = fruits + vegetables
shopping_list.extend(["sugar", "salt"])
shopping_list
```
output -> ['melon', 'orange', 'apple', 'cucumber', 'carrots', 'sugar', 'salt']


##### Extracting data from lists
```
colors = ["red", "green", "blue", "purple"]
colors[0] => red
```
###### slicing for the first two items
```colors[:2]```

output -> red, green

##### slicing for last two
```colors[-2:]```
output -> blue, purple

##### slicing for range
```colors[1:3]```
output -> green, blue

##### use an existing index to pop correct
```
pop_item = colors.pop(1)
pop_item
```
output -> red, blue, purple

```
colors.remove('red')
```
output -> blue, purple


##### Retrieve data from Dictionary
##### using a try/except block
```
try:
    contact_info["height"]
except KeyError:
    print("6ft")
```

##### using .get()
```
result = contact_info.get("height")
print("Height is", result)
```
output -> none

##### falling back there is no key
```
result = contact_info.get["height", "5ft 9in"]
print("Height is ", result)
```
```
contact_info["age"] = 31
print("Age is", contact_info.pop("age"))
print(contact_info)
```
output -> Age is 31


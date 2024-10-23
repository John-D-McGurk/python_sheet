# Python Sheet
## Variables
### int
This type of variable can only hold integers (numbers with no decimal place). This type of variable can be used to do mathematical operations.

#### Example
```
number_of_cats = 4
```
#### Methods
If a valid int is contained by another variable type (for example a string or a float), the <span style="color: yellow; font-weight: bold;">int(<variable_of_other_type>)</span> function can be called to convert into an int. If this function is used on an invalid variable (for example, containing letters), a ValueError will be thrown. If used on a float it will convert the float to an int by removing everything after the decimal (rounding down).

#### Examples
```
string = "cat"
integer = int(string)
```
<span style="font-family: monospace;">ValueError: invalid literal for int() with base 10: 'cat'</span>

```
string = "2"
integer = int(string)
print(integer)
```
<span style="font-family: monospace;">2</span>

```
float = 2.9
integer = int(float)
print(integer)
```
<span style="font-family: monospace;">2</span>

### float
This variable type can floating point numbers (numbers with decimal places). This type of variable can be used to do mathematical operations.

#### Example
```
rainfall_mm = 2.2
```

#### Methods
If a valid float is contained by another variable type (for example a string or an int), the <span style="color: yellow; font-weight: bold;">float(<variable_of_other_type>)</span> function can be called to convert into an int. If this function is used on an invalid variable (for example, containing letters), a <span style="color: yellow; font-weight: bold;">ValueError</span> will be thrown.

#### Examples
```
string = "cat"
integer = float(string)
```
<span style="font-family: monospace;">ValueError: invalid literal for float() with base 10: 'cat'</span>

```
string = "2.4"
integer = float(string)
print(integer)
```
<span style="font-family: monospace;">2.4</span>

```
integer = 3
float = float(integer)
print(float)
```
<span style="font-family: monospace;">3.0</span>

### str
This variable type contains a string of characters. It can contain any character, including numbers and special characters.

#### Methods
Calling the <span style="color: yellow; font-weight: bold;">str(another_variable_type)</span> will return a stringified version of the variable.

#### Example
```
cats = 4
string_cats = str(cats)
print(string_cats)
```
<span style="font-family: monospace;">"4"</span>

#### Operations
Using the addition oparator (<span style="color: yellow; font-weight: bold;">+</span>) on 2 strings will not perform a mathematical addition, but will instead combine the strings together (even if the strings contain only numbers!). If performed on a string and another variable type it will throw a <span style="color: yellow; font-weight: bold;">ValueError</span>.
#### Examples
```
string_1 = "cats"
string_2 = " and dogs"
print(string_1 + string_2)
```
<span style="font-weight: bold;">"cats and dogs"</span>

```
string_1 = "2"
string_2 = "1"
print(string_1 + string_2)
```
<span style="font-weight: bold;">"21"</span>

## Functions
```
def <function_name>(<arguments>):
   <indented_code>
   <return_value>
```
Creates a function that can be executed wherever you need in the script. Functions can also be called by other scripts if they are <span style="color: yellow; font-weight: bold;">imported</span>. To call the function use ,<span style="color: yellow; font-weight: bold;"><function_name>(\<arguments>)</span>. Functions can return a value (like the example below), or not, depending on the use case (function may print, for example, instead of returning a value)

#### Example
Take 2 numbers and return the sum
```
def add_numbers(num_1, num_2):
    sum = num_1 + num_2
    return sum
```


## For loops
### List loops
```
for <item_variable> in <list>:
    <indented code>
```
Loops through each item in the given list. On each loop an item of the list can be accessed through whatever the <span style="color: yellow; font-weight: bold;"><item_variable></span> is called.

#### Example
Print the names of each person in a staff list
```
for person in staff_list:
    print(person)
```

### Other loops
```
for <number_variable> in range(<selected_range>):
    <indented_code>
```
Loops a given number of times based on the range given inside the <span style="color: yellow; font-weight: bold;">range()</span> function. This is useful when we don't want to loop through a list, but rather do something a given number of times. 
Note: the range function starts at the first argument given and runs until but not including the second argument. Meaning <span style="color: yellow; font-weight: bold;">range(1,11)</span> will give [1,2,3,4,5,6,7,8,9,10], but not 11.

#### Example
Prints the "#" character 5 times.
```
for i in range(1,6):
    print('#')
```
### Loops special syntax
To exit a loop early the <span style="color: yellow; font-weight: bold;">break</span> command can be called. This is useful if you want to save looping through an entire list, for example, if you already found the item you were looking for.


## While loops
```
while <boolean>:
    <indented_code>
```
Keeps looping through the indented code until <span style="color: yellow; font-weight: bold;">\<boolean></span> is not <span style="color: yellow; font-weight: bold;">True</span>.


### Loops special syntax
To exit a loop early the <span style="color: yellow; font-weight: bold;">break</span> command can be called. This is useful if you want to save looping through an entire list, for example, if you already found the item you were looking for
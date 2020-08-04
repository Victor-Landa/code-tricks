Variables
```python
# Dynamic typing
x = 100
random = 'Python'
```
Data Types
```python
# Integers
x = 4
# Floats
z = 3.1415
# Strings
name = 'Victor'
# Booleans
a = True
b = False
```

Casting -- Type Conversion
```python
current_year = "2020"
current_year = int(current_year)
current_year = str(current_year)
current_year = float(current_year)
```

Invalid Casting
```python
my_name = "Victor"
my_name = int(my_name) # => ValueError: invalid literal for int() with base 10: 'Victor'
```

Operators 
```python
a = 'Basic'
b = 'String'
a + b # BasicString

c = 'Victor'
c * 5 # => VictorVictorVictorVictorVictor
```

Reassinging values
```python
# Reassingning values
d = 18
d = d + 1 # => 19

e = 20
e += 1 # => 21
```

Output
```python
name = 'Name'
country = 'Country'
print(name, country, 'Age') # => Name Country Age
```

Libraries
```python
# Import library name => Usage lib_name.lib_function
import random
random.randint(1, 5)

# Import a function
from random import randint
randint(1, 100)

# Import all library functions
from random import *
randint(1, 10)
```

User input
```python
x = input("Convert °C to °F: ")
user_input = float(x)
result = user_input * 1.8000 + 32.00
print('°F:', result)
```

Conditionals
```python
x = 44
y = 50

x > y # False
x < y # True
x >= y # False
x <= y # True
x == y # False
x != y # True

x <= y and y >= x # True
x > y or y > x # True
```

If / Elif / Else
```python
import random

a = random.randint(1, 5)
if a == 1:
  print('Random number is one')
elif a == 2:
  print('Random number is two')
else:
  print('Random number between 3 and 5')
print(a)
```

Loops
```python
# Forloop
import random

x = 0

for i in range(10):
	x += random.randint(1, 3)
  
# While
x = random.randint(1, 50)

while x != 6:
	x = random.randint(1, 49)
  # continue
  # break
```

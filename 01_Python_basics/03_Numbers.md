## Python Numbers  
There are three numeric types in Python:  
1. `int`
2. `float`
3. `complex`
Example
```python   
x = 1    # int
y = 2.8  # float
z = 1j   # complex
```
To verify the type of any object in Python, use the `type()` function:
```python
print(type(x))
print(type(y))
print(type(z))
```
out:
```
<class 'int'>
<class 'float'>
<class 'complex'>
```
## Int
`Int` or integer, is a whole number, positive or negative, without decimals, of unlimited length.
```python
x = 1
y = 35656222554887711
z = -3255522

print(type(x)) # <class 'int'>
print(type(y)) # <class 'int'>
print(type(z)) # <class 'int'>
```
## Float
`Float` or "floating point number" is a number, positive or negative, containing one or more decimals.  
```python
x = 1.10
y = 1.0
z = -35.59

print(type(x)) # <class 'float'>
print(type(y)) # <class 'float'>
print(type(z)) # <class 'float'>
```
`Float` can also be scientific numbers with an "e" to indicate the power of 10.
```python
x = 35e3
y = 12E4
z = -87.7e100

print(type(x)) # <class 'float'>
print(type(y)) # <class 'float'>
print(type(z)) # <class 'float'>
```
## Complex
`Complex` numbers are written with a "j" as the imaginary part
```python
x = 3+5j
y = 5j
z = -5j

print(type(x)) # <class 'complex'>
print(type(y)) # <class 'complex'>
print(type(z)) # <class 'complex'>
```
## Type Conversion  
You can convert from one type to another with the `int()`, `float()`, and `complex()` methods
```python
x = 1    # int
#convert from int to float:
a = float(x)
print(a)          #  1.0
print(type(a))    #  <class 'float'>
```
## Random Number
Python has a built-in module called `random` that can be used to make random numbers
```python
import random

print(random.randrange(1, 10)) # 1/2/3/4/5/6/7/8/9 
```
out:
`````
5
`````




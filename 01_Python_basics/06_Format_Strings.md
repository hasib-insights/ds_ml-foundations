## String Formatting Methods Table  
where 
```python
name = Hasib
```
| Method        |  Syntax                                  | Example (print `My name is Hasib`)                              | Output                                  |
|---------------|------------------------------------------| ----------------------------------------------------------------|:---------------------------------------:|
| concatenation | `"text" + variable`                      | `print("My name is " + name)`                                   | `My name is Hasib`                      | 
| str.format()  | `"text {}".format(variable)`             | `print("My name is {}".format(name))`                           | `My name is Hasib`                      | 
| f-string      | `f"text {variable}"`                     | `print(f"My name is {name}")`                                   | `My name is Hasib`                      |
| % formatting  | `"text %s" % variable`                   | `print("My name is %s" % name)`                                 | `My name is Hasib`                      |
| join()        | `"{Separator}".join(["text", variable])` | `",".join("My name is" , name` <br> `"-".join(("My name is" - name)` | `My name is Hasib` <br> `My name is - Hasib` |

## Concatenation 
Use a comma `+` between a string and a variable inside the `print()` function.
```python
name = "Hasib"
print("My name is " + name) H#output: My name isasib
```
## str.format()
 S.format(*args, **kwargs) -> str  
 
 |      Return a formatted version of S, using substitutions from args and kwargs.  
 |      The substitutions are identified by braces ('{' and '}').
 ```python
price = 59
"The price is {} dollars".format(price) #output: 'The price is 59 dollars'
```
```python
name = "Hasib"
age = 22
"My name is {}, I am {}".format(name, age) #output:'My name is Hasib, I am 22'
```

## F-Strings  
To specify a string as an f-string, simply put an `f` in front of the string literal, and add curly brackets `{}` as placeholders for variables and other operations.
```python
price = 59
txt = f"The price is {price} dollars"
print(txt) #output: The price is 59 dollars
```

Display the price with 2 decimals:  
A modifier is included by adding a colon : followed by a legal formatting type, like `.2f` which means fixed point number with 2 decimals:
```python
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt) #output: The price is 59.00 dollars
```
##  % formatting   
`% formatting` lets you embed values into a string using `%` placeholders like `%s`, `%d`, `%f`.
```python
name = "Hasib"
age = 21

print("My name is %s" % name) #out: My name is Hasib
print("My name is %s and I am %d years old." % (name, age)) #out: My name is Hasib and I am 21 years old.
```
## join() Method  
`.join(Variable)` joins each character of the string with `,` as the separator.
```python
name = "Hasib"
print(','.join(name)) #out: H,a,s,i,b
```
`.join()` combines items of a list into one string with a chosen separator.
```python
lst = ["Hello", "world" ] 
print(' '.join(lst)) #out: Hello world
```

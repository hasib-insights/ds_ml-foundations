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

## F-Strings  
To specify a string as an f-string, simply put an `f` in front of the string literal, and add curly brackets `{}` as placeholders for variables and other operations.
```python
price = 59
txt = f"The price is {price} dollars"
print(txt)
```
output:
```
The price is 59 dollars
```
Display the price with 2 decimals:  
A modifier is included by adding a colon : followed by a legal formatting type, like `.2f` which means fixed point number with 2 decimals:
```python
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt)
```
output:
```
The price is 59.00 dollars

```

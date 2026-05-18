## Strings
Strings in python are surrounded by either single quotation marks(''), or double quotation marks("").  
Examle
```
'hello'
"hello"
"It's alright"
```
Display a string literal with the **print()** function:
```python
print("Hello")
print('Hello')
print("It's alright")
```
out:
```
Hello
Hello
It's alright
```
## Multiline Strings
```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)
```
out:
```
Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.
```
## Slicing
Slice From the Start
```python
b = "Hello, World!"
print(b[:5]) # Hello
```
Slice To the End
```python
b = "Hello, World!"
print(b[2:]) # llo, World!
```
Use negative indexes to start the slice from the end of the string:  
From: "o" in "World!" (position -5)  
To, but not included: "d" in "World!" (position -2)
```python
b = "Hello, World!"
print(b[-5:-2]) # orl
```
## Modify Strings
### Upper Case
The **upper()** method returns the string in upper case:
```python
a = "Hello, World!"
print(a.upper())
```
out:
```
HELLO, WORLD!
```
#### Lower Case
The lower() method returns the string in lower case:
```python
a = "Hello, World!"
print(a.lower())
```
out:
```
hello, world!
```
## Replace String
The **replace()** method replaces a string with another string:
```python
a = "Hello, World!"
print(a.replace("H", "J")) #(Old, new)
```
out:
```
Jello, World!
```
* old → the text you want to change  
* new → the text you want to put instead  
* count (optional → how many times to replace (if not given, it replaces all)
```python
a = "Hello, World!"
print(a.replace("0", "d", 2)) #(Old, new, count)
```
out:
```
Helld, Wdrld!
```
## Split String
The split() method in Python is used to break a string into smaller parts (called a list of substrings).
```python
a = "Hello, World!"
print(a.split(","))
```
out:
```
['Hello', ' World!']
```
## multiply strings
It means repeating the string a certain number of times.
```python
word = "Hi "
print(word * 3)
```
out:
```
Hi Hi Hi
```






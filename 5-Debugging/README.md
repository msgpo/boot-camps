#Types of Errors and Exceptions and Try and Except

```python
#TypeError
print 's'/3.0
```

```python
#ZeroDivisionError
print 5.0/0.0
```

```python
#NameError
print flux
```

```python
#Syntax Error
print, 'a'
```

```python
#ValueError
a,b = 's'
```


**Output**:

```python
#If you expect an error try and except
l = ['a1', 'b2', 'c0', 'd3', 'ee', 'f5']
for pair in l:
    n, m = pair
    x =  5.0/float(m)

```


**Output**:

```python
#If you expect an error try and except
l = ['a1', 'b2', 'c0', 'd3', 'ee', 'f5']
for pair in l:
    try:
        n, m = pairs
        x = 5.0/float(m)
    except:
        print 'exception for '+ pair
```


**Output**:

```
exception for a1
exception for b2
exception for c0
exception for d3
exception for ee
exception for f5
```

```python
l = ['a1', 'b2', 'c0', 'd3', 'ee', 'f5']
for pair in l:
    try:
        n, m = pair
        x = 5.0/float(m)
    except ZeroDivisionError:
        print 'exception for '+ pair
```


**Output**:

```
exception for c0
```

```python
l = ['a1', 'b2', 'c0', 'd3', 'ee', 'f5']
for pair in l:
    try:
        n, m = pair
        x = 5.0/float(m)
    except (ZeroDivisionError, ValueError):
        print 'exception for '+ pair
```


**Output**:

```
exception for c0
exception for ee
```

```python
#Exercise:
#fix the following snippit of code:
l = ['a4', ['b', 2], ['c', 'c'], 'd4', '0e']
for pair in l:
    n, m = pair
    x = n*int(m)
```


**Output**:

```python
#Exercise:
#fix the following snippit of code:
l = ['a4', ['b', 2], ['c', 'c'], 'd4', '0f']
for pair in l:
    n, m = pair
    try:
        x = n*int(m)
    except ValueError:
        print 'skipped ', n, m
```


**Output**:

```
skipped  c c
skipped  0 f
```

#Tracebacks

```python
def add_two(x):
    return x+2.0

def multiply_by_5(x):
    return x*5.0

def divide_by_4(x):
    return x/4.0

def run_equation(x):
    return add_two(divide_by_4(multiply_by_5(x)))
```

```python
run_equation(3)
```


**Output**:

```
5.75
```

```python
run_equation(5.5)
```


**Output**:

```
8.875
```

```python
run_equation([1,2])
```


**Output**:

```python
#Exercise:
#Where is the following statement erroring and why?
run_equation('s')
```


**Output**:

```python
#What if there is no traceback?
```

```python
#pdb.set_trace()
import numpy as np
def find_where_1(x):
    indx = np.where(x == 1)
    mx = 5.0*x[indx] + 3.0
    return mx
```

```python
n = [1, 2, 3, 1, 4, 1, 5]
indx = find_where_1(n)
```


**Output**:

```python
#pdb.set_trace()
import pdb
def find_where_1(x):
    pdb.set_trace()
    indx = np.where(x == 1)
    mx = 5.0*x[indx] + 3.0
    return mx
```


**Output**:

```
(array([], dtype=int64),)
```

```python
y = find_where_1(n)
#in pdb
print indx
print type(x)
x = np.array(x)
indx = np.where(x == 1)
cont

```


**Output**:

```
[1, 2, 3, 1, 4, 1, 5]
```

```python
def pdb_exercise(x, y, z):
    a = [x, y, z]
    b = array(x, y, z)
    c = {'m':x, 'n':y, 'p':z}


#Fix the above function

```

```python
pdb_exercise('s', 3, 1)
```


**Output**:

```python
```


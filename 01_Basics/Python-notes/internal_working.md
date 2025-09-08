#Internal Working of Python with copies

```python

```


```python

import sys
# 24601 random number as input
sys. getrefcount(24601) # Output : 3

sys.getrefcount("Sayan") # output : 4294967295 ( Random large number . Because of internal compiler optimization loop)
```


```python
mylistOne = [1,2,3]
mylistTwo = mylistOne

mylistOne = "Sayan"
mylistTwo # Output : [1,2,3] , Reference does not changed

```

```python
listOne = [1,2,3]
listTwo = listOne
listOne # Output : [1,2,3]
listTwo # Output : [1,2,3]
# Because using same ref

listOne[0] = 99
listTwo #[99,2,3]


```


```python
listOne = [1,2,3]
listTwo = listOne
listTwo = [1,2,3] # New ref creating here in memory
listOne[0] = 55
listOne # [55,2,3] , Because list is mutable so its changing here
listTwo # [1,2,3]

```


```python
listOne = [1,2,3]
listTwo = listOne

listOne == listTwo # True

listOne is listTwo # True



listTwo = [1,2,3]

listOne == listTwo # True

listOne is listTwo # False , Because of diffrent memory ref



```


```python
h1 = [1,2,3]
h2 = h1[0:2] # Slice operation . index[0] to index[2]-1 = index[1] . Output : [1,2] 

x = [2,3,4]
y = x[:] # Deep Copy

```


```python
import copy

h1 = [1,2,3,[2,3,[4,5],6,[7,8,[9,10]]]]
# h2 = copy.copy(h1)
h2 = copy.deepcopy(h1)
h2

```


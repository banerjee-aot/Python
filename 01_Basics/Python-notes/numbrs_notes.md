# Number Notes

```python
x = 40
y = 2.35

float(x) # Use same datatypes always
x+y
```


```python
x = 4
y = 2
z = 4

# x+y*z is wrong approch
(x+y)*z # Use this

```


```python
'Sayan' + 'Banerjee' # operator overloading. + will detect datatypes of both side of it

```


```python
x = 4
y = 2
z = 7

x,y,z # (4,2,7)---> Tuple

m = x,y,z
m[0] # 4 , 'tuple' object does not support item assignment because of immutable

```


```python
1 == 2<3 #---> False because python interpriter treat as 1 == 2 and 2<3 . so here 1==2 is false . Using "and" operator if any of them is false so output will be false

1==(2<3) #---> True because 1 is truthy value and (2<3) is true so python treat it as True and True . 
```

```python
0o20 # Octal for 0o
0xFF # Hexadecimal for 0x
0b1001 # Binary for 0b

oct()
hex()
bin()

int('64',8) # number and base
int('10000',2)

```

```python
import random
random.random()
random.randint(1,10) # Range 1 to 10

l1 = ['A','B','C','D']
random.choice(l1)

random.shuffle(l1)

```


```python
0.1 + 0.1 + 0.1 # 0.30000000000000004


0.1 + 0.1 + 0.1 - 0.3 # 5.551115123125783e-17
(0.1 + 0.1 + 0.1) - 0.3 # 5.551115123125783e-17


from decimal import Decimal # Decimal Context manager library module and Fraction also there we and import it
# from fractions import Fraction 
# Fraction(2,7)

Decimal('0.1') + Decimal('0.1') + Decimal('0.1') # Decimal('0.3')
Decimal('0.1') + Decimal('0.1') + Decimal('0.1') - Decimal('0.3') # Decimal('0.0')


```


```python
setone = {1,2,3,4}
setone & {1,3} # intersection

setone | {1,3,7} # union

setone - {1,2,3,4} # set() , Output will not empty {}, because {} is dictionary
```

```python
True # Python treat as 1
False # Python treat as 0
True == 1 # True
True is 1 # False

True + 4 # 5
```

### Finite Field Addition and Subtraction

Remember that we need to define Finite Field addition in a way as to make sure that the result is still in the set. That is, we want to make sure that addition in a Finite Field is closed.

The % operator does the actual modulo operation. Also remember that + and - need to be in () because in the order of operations % comes before + and -.

This should be somewhat intuitive. We take any two numbers in the set, add and "wrap around" the end to get the sum. We are creating our own addition operator here and it’s a bit unintuitive. After all $11+~f~17=9$ just doesn’t look right for most people because they’re not used to Finite Field addition.

Solve these equations in \\(F_{31}\\):

```
2+15=?
17+21=?
29-4=?
15-30=?
```


```python
# remember that % is the modulo operator
prime = 31
# 2+15=?
# 17+21=?
# 29-4=?
# 15-30=?
```

## Exercise

Create the `__add__` and `__sub__` methods to your library:


```python
from ecc import FieldElement

class FieldElement(FieldElement):

    def __add__(self, other):
        if self.prime != other.prime:
            raise RuntimeError('Primes must be the same')
        # self.num and other.num are the actual values
        # self.prime is what you'll need to mod against
        # You need to return an element of the same class
        # use: self.__class__(num, prime)
        pass

    def __sub__(self, other):
        if self.prime != other.prime:
            raise RuntimeError('Primes must be the same')
        # self.num and other.num are the actual values
        # self.prime is what you'll need to mod against
        # You need to return an element of the same class
        # use: self.__class__(num, prime)
        pass
```

# Mapping

Consider the following algorithm:

```python
def squares(ns):
    result = []
    for n in ns:
        result.append(n**2)
    return result


>>> squares([0, 1, 2, 3, 4])
[0, 1, 4, 9, 16]
```

While it may not be the most useful code, it follows a certain pattern: given a list of values, it applies an operation on each of them and collects the results in a new list.
Here, the operation is squaring.

This pattern occurs quite often, typically as part of a bigger whole:

* Given a list of items, get the price of each item (and take the sum to get the total cost).
* Given a list of enemies, check if any one of them touches the player (and if so, the player is dead).
* Given a list of exam questions, grade each of them (and compute the final grade).

This pattern is called _mapping_: it _maps_ each value from an input list to corresponding value which is stored in an output list.
Python provides a special syntax for this mapping operation.
We can rewrite the function above as

```python
def squares(ns):
    return [n**2 for n in ns]
```

This is called a _list comprehension_ and is a more concise (and readable) way to perform mappings.
They also have performance benefits.
Running the provided script `benchmark.py` shows this:

```bash
$ py benchmark.py
squares_loop used 0.764 seconds
squares_loop2 used 0.867 seconds
squares_comprehension used 0.642 seconds
```

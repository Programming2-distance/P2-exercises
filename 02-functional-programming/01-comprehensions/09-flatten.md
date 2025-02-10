# Flatten

Consider the following list comprehension:

```python
>>> [[(x, y) for x in range(3)] for y in range(3)]
[
    [(0, 0), (1, 0), (2, 0)],
    [(0, 1), (1, 1), (2, 1)],
    [(0, 2), (1, 2), (2, 2)]
]
```

As you can see, nothing prevents you from using comprehensions within comprehensions.
In the example above, the result is a list of lists of coordinates.
However, what if we didn't want this nested structure, this list of lists, but instead
wished for just one list of coordinates?

We want to "flatten" the list of lists into a list.
We can achieve this by rewriting the comprehension above as follows:

```python
>>> [(x, y) for x in range(3) for y in range(3)]
[(0, 0), (0, 1), (0, 2), (1, 0), (1, 1), (1, 2), (2, 0), (2, 1), (2, 2)]
```

You can combine as many `if`s and `for`s as you wish in this way.

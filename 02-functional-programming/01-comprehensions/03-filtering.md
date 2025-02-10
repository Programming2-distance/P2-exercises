# Filtering

```python
def select_adults(people):
    result = []
    for person in people:
        if person.age >= 18:
            result.append(person)
    return result
```

This little function selects `Person`s whose age is at least `18`.
Or, more generally, given a list `lst` of values, it returns a new list that contains all items from `lst` that satisfy a certain condition.
This is typically called _filtering_.

As with mapping, Python also has a special syntax for it.
Fortunately, it fits in with the already existing syntax for list comprehensions:

```python
def select_adults(people):
    return [person for person in people if person.age >= 18]
```

It is of course possible to combine mapping with filtering.
Say you want the names of all adults:

```python
def select_adult_names(people):
    return [person.name for person in people if person.age >= 18]
```

For the sake of readability, you might want to spread it over multiple lines:

```python
def select_adult_names(people):
    return [
        person.name
        for person in people
        if person.age >= 18
    ]
```

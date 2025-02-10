# Min and Max

We can find the maximum of a series of numbers:

```python
max(numbers)
```

This way we can also find the maximum age of a bunch of `Person`s:

```python
max([person.age for person in people])
```

However, how can we easily find the `Person`s with the maximum age?
`max`, like `sort`, relies on `__lt__`.
This means we could have `Person`'s `__lt__` method compare ages, but that would be very limiting: what if we want the heaviest person, the tallest person, etc.?

We could work in two steps:

```python
max_age = max([person.age for person in people])
oldest_people = [person for person in people if person.age == max_age]
```

However, we'd rather not go through the `Person`s twice (in some cases, this might actually not even be possible, as you'll see later.)
Fortunately, there is a way to tell `max` what we want to maximize.
Like `sort`, it takes a (keyword) parameter `key`.
This should be a function that, given an element of the list, returns the value that should be used for comparisons.

```python
oldest_person = max(people, key=lambda person: person.age)
tallest_person = max(people, key=lambda person: person.height)
heaviest_person = max(people, key=lambda person: person.weight)
```

And of course, the same is true for `min`.

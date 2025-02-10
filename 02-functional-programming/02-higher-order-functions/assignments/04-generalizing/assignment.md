## Task

Generalize the following function:

```python
def find_first_book_by_author(books, author):
    for book in books:
        if book.author == author:
            return book
    return None
```

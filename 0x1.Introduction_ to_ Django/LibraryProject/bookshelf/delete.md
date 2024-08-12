
### `delete.md`


```python 
from bookshelf.models import Book
book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()

# Confirm deletion by trying to retrieve all books
all_books = Book.objects.all()
print(list(all_books))

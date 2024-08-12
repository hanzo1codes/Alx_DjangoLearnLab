## CRUD Operations Summary

### Create
```python
from bookshelf.models import Book

book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
book.save()

output was an empty string


book = Book.objects.get(title="1984")
print(book.title, book.author, book.publication_year)


book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()

updated_book = Book.objects.get(id=book.id)
print(updated_book.title)


book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()

all_books = Book.objects.all()
print(list(all_books))



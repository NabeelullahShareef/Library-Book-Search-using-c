# Library Book Search in C

A library book search program written in C. It stores a small book catalog in a **Binary Search Tree (BST)** keyed on book ID and looks up books by their numeric ID.

## Features

- Stores books (ID, title, author) in a binary search tree, ordered by book ID
- Searches the catalog for a book by its ID and reports whether it was found
- Prints the entire catalog sorted by ID using in-order tree traversal
- Ships with a built-in sample catalog of 5 books, so the program runs out of the box

## How to compile

```bash
gcc "Library book search" -o library_search
```

> Tip: rename `Library book search` to something ending in `.c` (e.g. `library_search.c`) for a more conventional build command:
>
> ```bash
> gcc library_search.c -o library_search
> ```

## How to run

```bash
./library_search
```

## Example usage

The program first prints the catalog sorted by ID, then demonstrates two searches — one that finds a book and one that doesn't:

```text
## All Books in the Library (Sorted by ID):
--------------------------------------------------------------------------
ID: 55    | Title: Let Us C                      | Author: Yashavant Kanetkar
ID: 89    | Title: Clean Code                    | Author: Robert C. Martin
ID: 101   | Title: The C Programming Language   | Author: Kernighan & Ritchie
ID: 205   | Title: Data Structures Using C      | Author: Reema Thareja
ID: 310   | Title: Introduction to Algorithms   | Author: Cormen et al.
--------------------------------------------------------------------------

## Searching for book with ID: 205
✅ Book Found!
   ID: 205
   Title: Data Structures Using C
   Author: Reema Thareja

--------------------------------------------------------------------------
## Searching for book with ID: 999
❌ Book with ID 999 not found in the library.
```

## How it works

- `createNode` / `insertBook` — build the BST, keyed on book ID
- `searchBook` — recursively searches the BST for a given ID
- `inOrderTraversal` — prints the books in ascending ID order
- `main` — inserts the 5 sample books, lists the catalog, and runs the two demo searches

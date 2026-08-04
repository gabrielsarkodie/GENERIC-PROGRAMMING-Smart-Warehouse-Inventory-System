# Smart Warehouse Inventory System (Generic Programming)

## Overview
This repository implements a reusable, generic warehouse inventory management system using Python's `typing.Generic` and `TypeVar`. 

The system allows a logistics company to store, retrieve, and display items of any data type (e.g., electronic devices, books, food products, spare parts) while preserving type consistency without creating separate storage classes for each category.

---

## Features & Implementation

### `Inventory[T]` Generic Class
The core component is the `Inventory[T]` generic class, which supports:
- **Type Safety**: Enforces type consistency across items stored in a specific inventory instance.
- **Single & Multi-Item Storage**: Allows storing individual items upon initialization and adding multiple items dynamically.
- **Retrieval**: Provides access to specific items or the entire list of stored items.
- **Type & Value Inspection**: Formats and prints each stored item along with its Python type name (`type(item).__name__`).

---

## Code Example

```python
from typing import Generic, TypeVar, List

T = TypeVar('T')

class Inventory(Generic[T]):
    def __init__(self, initial_item: T = None):
        self.items: List[T] = []
        if initial_item is not None:
            self.items.append(initial_item)

    def add_item(self, item: T) -> None:
        self.items.append(item)

    def get_item(self, index: int = 0) -> T:
        return self.items[index]

    def get_all_items(self) -> List[T]:
        return self.items

    def display(self) -> None:
        for item in self.items:
            print(f"Type: {type(item).__name__}, Value: {item}")

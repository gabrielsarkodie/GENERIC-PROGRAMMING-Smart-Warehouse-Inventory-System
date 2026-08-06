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

# Generic Programming – Smart Warehouse Inventory System

## Overview
This project demonstrates the application of **Generic Programming** in Python using the `typing` module (`Generic` and `TypeVar`). It provides a foundational, reusable container class designed to securely handle single items of arbitrary data types while maintaining type clarity and hint support.

---

## Technical Features

### `Storage[T]` Class
A generic single-item storage container engineered to accommodate dynamic data types.
* **`store(item: T) -> None`**: Takes an item of parameterized type `T` and stores it internally.
* **`retrieve() -> T | None`**: Accesses and returns the currently stored item.

---

## Demonstrations & Test Cases

The implementation is validated across three primary data structures:

1. **Integer Storage (`Storage[int]`)**: Demonstrates primitive numerical data handling.
2. **String Storage (`Storage[str]`)**: Manages textual descriptors such as stock codes or warehouse labels.
3. **List Storage (`Storage[list]`)**: Handles complex structured data collections containing multiple elements.

---

## Project Artifacts

* **Notebook**: `trial-warehouse-inventory-system.ipynb` — Full source code, inline type hints, execution outputs, and test cases.
* **Repository**: `GENERIC-PROGRAMMING–Smart-Warehouse-Inventory-System`

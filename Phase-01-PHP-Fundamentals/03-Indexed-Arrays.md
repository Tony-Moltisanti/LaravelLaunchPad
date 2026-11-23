# Lesson 3 — Indexed Arrays

**Status:** Completed

## What is an array?
An array stores multiple values under one variable name. It is useful when several related values belong together, such as a list of clinic services.

```php
$services = [
    "General Consultation",
    "Skin Check",
    "Dental Check",
    "Eye Examination"
];
```

## What is an indexed array?
An indexed array uses numeric indexes to identify its elements. PHP's automatically assigned numeric indexes normally begin at zero.

| Index | Value |
|---:|---|
| 0 | General Consultation |
| 1 | Skin Check |
| 2 | Dental Check |
| 3 | Eye Examination |

The index is a position label, not a count that begins at one.

## Syntax explained
- `$services` is the variable holding the array.
- `=` assigns the array to the variable.
- `[` and `]` delimit the array.
- Quoted values are strings.
- Commas separate elements.
- `;` ends the assignment statement.

## Accessing an element
```php
echo $services[1];
```
This displays `Skin Check`, because index `1` identifies the second element.

```php
echo $services[3];
```
This displays `Eye Examination`.

## Why indexes begin at zero
PHP uses zero-based numeric indexes for ordinary indexed arrays. The first element is at index `0`, the next at `1`, and so on. Remember this when selecting an element.

## Common mistakes
- Using `[1]` when you mean the first item.
- Forgetting square brackets around the index.
- Accessing an index that does not exist.
- Confusing an index with the value stored there.

## Practice
Given the `$services` array above:
1. Identify the index of `General Consultation`.
2. Identify the index of `Dental Check`.
3. Display `Eye Examination`.
4. Explain why the second item uses index `1`.

## Completion checklist
- [x] Explain what an array is.
- [x] Explain what an indexed array is.
- [x] Understand zero-based indexes.
- [x] Access values using indexes.
- [x] Complete index and retrieval exercises independently.

**Lesson result:** Completed.

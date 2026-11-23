# Lesson 1 — PHP Variables

**Status:** Completed

## What is a variable?
A variable is a named place in a program where a value can be stored. Its name lets the program refer to that value later. In an appointment application, variables can hold a patient's name, appointment identifier, or service price.

```php
$patientName = 'John';
$appointmentId = 25;
$servicePrice = 50;

echo $appointmentId;
```

## Why variables exist
Variables give information meaningful names, make code easier to read, and allow values to be reused or changed without rewriting every use of a literal value.

## Syntax explained
- `$` begins a PHP variable name.
- `patientName` is the chosen descriptive name.
- `=` is the assignment operator: it assigns the right-hand value to the variable on the left.
- `'John'` is a string. Quotes tell PHP to interpret it as text.
- `25` and `50` are numeric values, not text.
- `;` ends a PHP statement.
- `echo` displays a value; assignment alone does not display it.

## Why quote text?
`'John'` is text, so it is enclosed in quotes. A numeric value intended for arithmetic, such as `25`, is written without quotes. `"25"` is a string, not an integer.

## Common mistakes
- Forgetting `$` before a variable name.
- Forgetting quotes around text.
- Confusing assignment (`=`) with display (`echo`).
- Forgetting the semicolon.
- Using inconsistent variable names.

## Practice
1. Store `Dr Ada` in `$doctorName`.
2. Store `25` in `$appointmentId`.
3. Display both values.
4. Explain the difference between `=` and `echo`.

## Completion checklist
- [x] Explain what a variable stores.
- [x] Recognise `$` as the variable prefix.
- [x] Understand assignment with `=`.
- [x] Distinguish text from numeric values.
- [x] Display a stored value with `echo`.
- [x] Write a simple variable example independently.

**Lesson result:** Completed.

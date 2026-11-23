# Lesson 5 — Associative Arrays

**Status:** Completed

## What is an associative array?
An associative array stores values using named keys rather than relying only on numeric indexes. Named keys are useful when each value has a clear meaning.

```php
$doctor = [
    "name" => "Dr Ada Obi",
    "specialty" => "General Medicine",
    "price" => 75.50,
    "available" => true
];
```

## Why use named keys?
A numeric position does not explain what information it represents. A key such as `"specialty"` makes the purpose of the value clear and makes the code easier to read.

## Understanding `=>`
The `=>` symbol connects a key to its value inside an array.

```php
"name" => "Dr Ada Obi"
```
- `"name"` is the key.
- `"Dr Ada Obi"` is the value.
- `=>` associates the key with that value.

## Accessing a value
```php
echo $doctor["name"];
```
The array variable identifies the array, and `["name"]` selects the value associated with that key.

Other examples:
```php
echo $doctor["specialty"];
echo $doctor["price"];
echo $doctor["available"];
```

## Different data types can be stored
```php
$patient = [
    "name" => "John",
    "age" => 28,
    "email" => "john@example.com",
    "registered" => true
];
```
The key describes the field; the value has its own data type.

## Common mistakes
- Using a key that does not exist.
- Confusing the key with its value.
- Forgetting quotes around string keys.
- Confusing `=>` inside an array with `=` used for assignment.

## Practice
Given the `$patient` array above:
1. Identify the key that stores the age.
2. Display the email.
3. State the value stored under `"name"`.
4. Explain what `=>` does.

## Completion checklist
- [x] Explain associative arrays.
- [x] Distinguish keys from values.
- [x] Explain `=>`.
- [x] Access values using named keys.
- [x] Work with different data types in one array.

**Lesson result:** Completed.

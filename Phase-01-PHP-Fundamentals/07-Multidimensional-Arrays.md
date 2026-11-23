# Lesson 7 — Multidimensional Arrays

**Status:** Completed

## What is a multidimensional array?
A multidimensional array is an array that contains one or more arrays. It is useful when each item in a collection needs several related pieces of information.

```php
$doctors = [
    [
        "name" => "Dr James",
        "specialty" => "General Physician",
        "available" => true
    ],
    [
        "name" => "Dr John",
        "specialty" => "Dentist",
        "available" => true
    ],
    [
        "name" => "Dr Stephanie",
        "specialty" => "Optometrist",
        "available" => true
    ]
];
```

`$doctors` is the outer or main array. Each array inside it is an inner array representing one doctor. The keys describe that doctor's fields.

## Why use this structure?
An indexed array can store a list of names. An associative array can store details for one doctor. A multidimensional array combines these ideas: the outer array stores a collection, while each inner associative array stores one doctor's details.

## Indexes and keys
There are two levels of access:
1. The **index** selects an inner array from the outer array.
2. The **key** selects a value inside that inner array.

```php
$doctors[1]["specialty"];
```
- `$doctors[1]` selects the second inner array.
- `["specialty"]` selects the specialty value inside it.

Indexes normally begin at zero: `0` is first, `1` is second, and `2` is third.

Remember: **Index = which doctor? Key = which detail about that doctor?**

## Accessing nested values
```php
echo $doctors[0]["name"];
echo $doctors[1]["specialty"];
echo $doctors[2]["available"];
```

The general pattern is `$mainArray[index]["key"]`.

## Updating a nested value
```php
$doctors[1]["available"] = false;
```
The index selects the second doctor's inner array. The key selects its availability field. Assignment changes that field without replacing the doctor's other details.

## Appending a new inner array
```php
$doctors[] = [
    "name" => "Dr Bright",
    "specialty" => "General Physician",
    "available" => true
];
```
The empty `[]` after `$doctors` tells PHP to append the new inner array at the end of the main array.

## Complete example
```php
$doctors = [
    [
        "name" => "Dr James",
        "specialty" => "General Physician",
        "available" => true
    ],
    [
        "name" => "Dr John",
        "specialty" => "Dentist",
        "available" => true
    ],
    [
        "name" => "Dr Stephanie",
        "specialty" => "Optometrist",
        "available" => true
    ]
];

$doctors[1]["available"] = true;

$doctors[] = [
    "name" => "Dr Bright",
    "specialty" => "General Physician",
    "available" => true
];

echo $doctors[2]["specialty"];
```
Output: `Optometrist`

## Common mistakes
- Using the wrong index: index `1` is the second item.
- Confusing the index with the key.
- Spelling a key incorrectly.
- Forgetting the semicolon after the assignment.
- Replacing the whole array instead of appending an inner array.

Compare:
```php
$doctors = ["name" => "Dr Bright"]; // assigns a new array
$doctors[] = ["name" => "Dr Bright"]; // appends an item
```

## Appointment-booking example
```php
$services = [
    [
        "name" => "General Consultation",
        "price" => 50.00,
        "duration" => 30
    ],
    [
        "name" => "Skin Check",
        "price" => 40.00,
        "duration" => 20
    ]
];

echo $services[1]["price"];
```
This is an in-memory PHP array example, not a replacement for database models and relationships in Laravel. Later lessons will explain how Laravel represents application data using database records and Eloquent relationships.

## Practice
1. Create a `$services` array with three inner arrays, each containing `name`, `price`, and `duration`.
2. Display the first service's name.
3. Display the second service's price.
4. Change the second service's price.
5. Append a fourth service.
6. Display the fourth service's name.
7. Explain the outer array, inner array, index, and key.

## Completion checklist
- [x] Explain multidimensional arrays.
- [x] Identify outer and inner arrays.
- [x] Distinguish indexes and keys.
- [x] Access nested values.
- [x] Update nested values.
- [x] Append an inner array.
- [x] Independently create and modify a doctors array.
- [x] Explain the code and correct a mismatch between code and explanation.

**Lesson result:** Completed.

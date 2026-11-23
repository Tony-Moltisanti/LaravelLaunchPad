# Lesson 6 — Modifying Associative Arrays

**Status:** Completed

## Why modify an associative array?
Application data changes. A patient's phone number may be added, an age updated, or a field removed. Associative arrays let you make these changes using keys.

```php
$patient = [
    "name" => "John",
    "age" => 28,
    "email" => "john@example.com"
];
```

## Adding a new key and value
```php
$patient["phone"] = "08012345678";
```
If `"phone"` does not exist, this adds the key and value. Phone numbers are commonly stored as strings because they are identifiers, may begin with zero, and are not normally used for arithmetic.

## Updating an existing value
```php
$patient["age"] = 29;
```
Because `"age"` already exists, this assigns a new value to that key. Other array elements remain.

The same key-assignment syntax can add a key or update an existing key. PHP determines which occurs by whether the key already exists.

## Removing a key
```php
unset($patient["phone"]);
```
`unset()` removes the selected element. Other elements remain in the array.

## Updating one element versus replacing the array
Update one element:
```php
$patient["age"] = 29;
```

Replace the array value:
```php
$patient = [
    "status" => "confirmed"
];
```
The second assignment gives `$patient` a new array containing the new `"status"` element. The previous contents are no longer in that variable.

## Practical doctor example
```php
$doctor = [
    "name" => "Dr Bola",
    "specialty" => "Dermatology",
    "price" => 60.00,
    "available" => false
];

$doctor["price"] = 65.00;
$doctor["available"] = true;
$doctor["experience"] = 5;
unset($doctor["specialty"]);
```
This updates the price, changes availability, adds experience, and removes the specialty field.

## Common mistakes
- Reassigning the whole array when intending to update one key.
- Using the wrong key spelling.
- Forgetting that `unset()` removes the selected element.
- Storing a phone number as a number when its formatting matters.

## Practice
1. Add a `"phone"` key.
2. Update the patient's age.
3. Remove the phone key.
4. Explain the difference between `$patient["age"] = 29;` and `$patient = ["status" => "confirmed"];`.

## Completion checklist
- [x] Add a key and value.
- [x] Update an existing value.
- [x] Remove a key with `unset()`.
- [x] Explain updating one element versus replacing the array.
- [x] Independently modify a doctor array.

**Lesson result:** Completed.

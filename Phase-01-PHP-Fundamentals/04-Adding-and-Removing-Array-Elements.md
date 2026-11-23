# Lesson 4 — Adding and Removing Array Elements

**Status:** Completed

## Why add or remove array elements?
Application information changes. A clinic may add a service or remove one that is no longer offered. Arrays provide operations for changing a collection.

```php
$services = [
    "General Consultation",
    "Skin Check"
];
```

## Adding with `array_push()`
```php
array_push($services, "Dental Check");
```
`array_push()` adds one or more values to the end of an array. In this example, the new value receives index `2`.

## Adding with empty square brackets
```php
$services[] = "Eye Examination";
```
The empty `[]` means append this value to the end of the array. This is a concise way to append one item.

## Removing with `unset()`
```php
unset($services[1]);
```
`unset()` removes the element at index `1`. It does not automatically renumber the remaining numeric keys. A remaining element may still have index `2`.

## Reindexing with `array_values()`
```php
$services = array_values($services);
```
`array_values()` returns an array containing the values with new numeric indexes starting from zero. Assigning the result back to `$services` makes that variable hold the reindexed array.

## Why removal and reindexing are separate
`unset()` removes a selected element. `array_values()` reindexes the remaining values. Keeping these operations separate lets you choose whether to preserve the remaining keys or create consecutive numeric indexes.

## Common mistakes
- Assuming `unset()` automatically closes an index gap.
- Forgetting to assign the result of `array_values()` when you want the original variable reindexed.
- Continuing to use an old index after reindexing without checking the new positions.

## Practice
1. Add `Dental Check` using `array_push()`.
2. Append `Eye Examination` using `$services[]`.
3. Remove the element at index `1`.
4. Explain what happens to the remaining keys.
5. Reindex using `array_values()`.

## Completion checklist
- [x] Add with `array_push()`.
- [x] Append with `$array[]`.
- [x] Remove with `unset()`.
- [x] Explain index gaps after removal.
- [x] Reindex with `array_values()`.

**Lesson result:** Completed.

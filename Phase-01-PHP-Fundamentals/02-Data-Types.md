# Lesson 2 — PHP Data Types

**Status:** Completed

## What is a data type?
A data type describes the kind of value a variable contains. PHP needs to distinguish text, numbers, true/false values, and the absence of a value because they are used differently.

## The five types covered

### String
Text, for example:
```php
$patientName = "John";
```

### Integer
A whole number without a decimal part:
```php
$patientAge = 28;
```

### Float
A number that can have a fractional/decimal part:
```php
$consultationPrice = 75.50;
```
`var_dump()` identifies this as a float. `gettype()` commonly returns `double` as the type name for a floating-point value.

### Boolean
One of two values, `true` or `false`:
```php
$appointmentConfirmed = true;
```
These are Boolean values, not strings. Do not quote them when you intend Boolean values.

### Null
Represents the absence of a value:
```php
$selectedDoctor = null;
```

## Why data types matter
The type affects how PHP interprets and uses a value. Adding numbers is different from joining text. A Boolean represents a yes/no state; `null` represents an absent value.

## Inspecting values with `var_dump()`
```php
$patientName = "John";
$patientAge = 28;
$consultationPrice = 75.50;
$appointmentConfirmed = true;
$selectedDoctor = null;

var_dump($patientName);
var_dump($patientAge);
var_dump($consultationPrice);
var_dump($appointmentConfirmed);
var_dump($selectedDoctor);
```
`var_dump()` displays type and value information, making it useful for learning and debugging. Example forms include `string(3) "Ada"`, `int(100)`, `float(75.5)`, `bool(false)`, and `NULL`.

## `gettype()`
```php
echo gettype($consultationPrice);
```
`gettype()` returns a string naming the type. For a floating-point number it commonly returns `double`; for null it returns `NULL`.

Difference:
- `var_dump()` displays type and value information.
- `gettype()` returns the type name.

## Boolean values and `echo`
When directly echoed in PHP, `true` displays as `1`, while `false` displays as an empty string. This is why conditions are useful when displaying readable availability labels.

## Common mistakes
- Quoting `true` or `false`, which makes them strings.
- Assuming `gettype()` and `var_dump()` produce the same output.
- Treating a decimal number as an integer.
- Confusing `null` with the string `"null"`.

## Practice
1. Create one variable of each of the five types.
2. Inspect each with `var_dump()`.
3. Use `gettype()` on a float and a Boolean.
4. Explain why `true` and `"true"` are different.

## Completion checklist
- [x] Identify string, integer, float, Boolean, and null.
- [x] Recognise the syntax for each type.
- [x] Use `var_dump()` and `gettype()`.
- [x] Explain direct `echo` behaviour for Boolean values.

**Lesson result:** Completed.

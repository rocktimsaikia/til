On this guide, I am skipping noting down any syntax and behaviour that I find
similar to Javascript.

## Basic Data Types

```
int - %d
Stores whole numbers, without decimals

float - %f
Stores fractional numbers. 6-7 decimals digits

double - %lf
Same as float. 15 decimals digits

char - %c
Stores a single character/letter/number or ASCII values.
Wrapped with single quote.
```

> [!NOTE]
> `float` vs`double`
> The precision of a floating point value indicates how many digits the value
> can hold after the decimal point. The precision of `float` is six or seven decimal
> digits, while `double` variables have precision of about 15 digits. Therefore, it
> is is often safer to use `double` for most calculations - but note that it takes
> 2x memory as `float` (8 bytes vs. 4 bytes)

## Check the size of a varibale using `sizeof` operator

```c
int myInt;
float myFloat;
char myChar;

print("%lu", sizeof(myInt));
print("%lu", sizeof(myFloat));
print("%lu", sizeof(myChar));
```

> [!NOTE]
> The `lu` format specifier is used to print the size of variable, because the
> compiler expect the `sizeof` operator to return a `long unsigned int (%lu)`.

## Type conversions

There are two type conversions:

1. Implicit Conversion (Automatically done via the compiler)
2. Explicit Conversion (Manually done)

```
// Manual conversion of int to float
float sum = (float) 5 / 2;

print("%.1f", sum)
```

## Boolean

C has `bool` data type with two possible values `true` or `false`. \
The boolean values are retuned as integers only at end. `1 >=` represents true
ad `0` represents false.


Unlike `int` or `char`, the `bool` type is not builtin, so needs to be imported
with the following header:

```c
#incude <stdbool.h>

bool isLoading = true;
```

## Arrays

```c
int numbers[] = {12, 32, 43, 56};

// Pre-define the size of an array
int numbers[4];
```

Find out the length of an array with `sizeof`. Divide the total size of the array
by the size of an item.

```c
// Find the length of an array using `sizeof`
int length = sizeof(numbers) / sizeof(numbers[0]);
```
### Multi-dimensional Arrays

To define a Multi-dimensional array, we must pre-define it's row number and column numbers:

```
// Here there are 2 items (rows) and 4 items (columnns) on each of them.
let matrix[2][4] = { { 1,2,3,4 }, { 11,22,33,44 } };
```

## Strings

C does not have a String data type. Instead, we need to use `char` type with an

```c
// Double quotes must be used in String definations
char greets[] = "Hello World!";
print("%s", greets);
```


### String functions

```c
#include <string.h>

// Get length of the string
char name[] = "Rocktim";
printf("%d", strlen(name));

// Concatenate lastname to name (result is stored in name)
char lastname[] = " Saikia";
strcat(name, lastname);

// Copy the value of name to fullname
char fullname[20];
strcpy(fullname, name);

// Compare strings | returns 0 (true) or -4 (false)
strcmp(name, fullname);
```

## Pointers

We can get the memory address/location of a variable with the "reference operator `&`".
This process is also called "Reference".

```c
int age = 43;

printf("%d", age); // Outputs the value of age
printf("%p", &age); // Outputs the memory address of age

int *ptr = &age;
printf("%p", ptr);
```

> [!NOTE]
> A pointer variable simply stores the memory location of another variable.

We can also get the actual value of a pointer variable by using the same `*` operator.
This process is also known as "Dereference".

```c
// prints 43
printf("%d", *ptr);
```

> [!NOTE]
> 1. When `*` is used in declaration (`int *ptr`), it creates a pointer variable.
> 2. When not used in declaration, it acts as a **deference operator**.

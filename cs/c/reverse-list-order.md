## Reverse an given array

```c
int *reverse_list(const int *array, size_t length) {
    int *reversed = malloc(length * sizeof(int))
    for (size_t i=0; i<length; i++){
        reversed[i] = array[length-i-1]
    }
    return reversed
}
```

## Learnings:

1. The function `*reverse_list` returns a "pointer to integer" denoted by the
`int *`. Meaning the function will return a memory address where an integer or
in case of arrays, the first of a series of integers is stored.

2. In C, the return type comes before the function name or variable name.

3. `malloc` is part of the standard C library (`#include <stdlib.h>`). It stands
for "memory allocation". It's purpose is to dynamically allocate a contiguous block
of memory on the heap. It returns a void pointer (`void*`) to the beginning of the
allocated memory block.

> [!NOTE]
> "Dynamic allocation": Dynamic means occurring at runtime, as opposed to compile time.
> `malloc` allocates memory while the program is running, not when it's compiled. This
> is flexible and efficient since the size of the array is not predetermine when you write the code
and is only allocated when requested, allowing efficient use of resources. The program
can decide how much memory to allocate based on user input or other runtime factors.

4. `length * sizeof(int)`:
Here are determine the size of the reversed array. `int` is typically 4 bytes on most
modern systems, but it can vary. Using `sizeof(int)` instead of hard-coded value makes
the code more portable and less error prone. By multiplying the size of int to `length`
we get the total size to reserve for our array.

5. The reason to use `size_t` for `i` is that we can be sure that `i` will be always
unsigned/positive (`size_t` is always unsigned) and there will no implicit type conversions since length is also
of `size_t` type.

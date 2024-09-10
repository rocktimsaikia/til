```c
// Function Declaration
const char* greet(){
    return "hello world!"
}

int main(){
    // Function Consumption
    const char* greeting = greet()
    printf("%s", greeting)
}
```

## Learnings:
1. In C, sting literals are usually declared as `const char*`.
2. When printing a pointer, "%s" should be used to print a string value, instead of "%p"
which prints the address of the pointer.

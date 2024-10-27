# Chapter 6

## Pointer and References

### In C :

Pointers in C 

```
#include <stdio.h>

int main(void)
{
        int x = 123;
        printf("The value before the change: %d\n", x);
        int* p = &x;
        *p = 456;
        printf("The value after the change: %d\n", x);
}


```

When passing to function

```
#include <stdio.h>

// Double the number passed in as 'x'.
int double_number_a(int x) {
    return 2 * x;
}

// Double the number pointed to by 'x'.
void double_number_b(int* x) {
    *x *= 2;
}

int main() {
    int num = 5;
    
    printf("%d\n", double_number_a(num));
    printf("%d\n", num);

    double_number_b(&num);
    printf("%d\n", num);
    
    return 0;
}

```

### In C++ :

Pointers in C++ remain same as in C.

```
#include <iostream>

int main()
{
        int x = 123;
        std::cout << "The value before the change: " << x;
        int* p = &x;
        *p = 456;
        std::cout << "The value after the change: " << x;
}
```

However we prefer to use references in C++ rather than raw pointers.


```
#include <iostream>

int main()
{
        int x = 123;
        int& y = x;
        x = 456;
        // both x and y now hold the value of 456
        y = 789;
        // both x and y now hold the value of 789
}

```

When passing to function

```
#include <iostream>

// Double the number passed in as 'x'.
int double_number_a(int x) {
    return 2 * x;
}

// Double the number pointed to by 'x'.
void double_number_b(int* x) {
    *x *= 2;
}

// Double the number pointed to by 'x'.
void double_number_c(int& x) {
    x *= 2;
}

int main() {
    auto num = 5;
    
    std::cout << double_number_a(num) << std::endl;
    std::cout << num << std::endl;
    
    double_number_b(&num);
    std::cout << num << std::endl;
    
    double_number_c(num);
    std::cout << num << std::endl;

    return 0;
}

```
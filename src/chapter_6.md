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

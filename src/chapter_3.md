# Chapter 3

## Printing different values of int

### In C :

```
#include <stdio.h>

int main(void)
{
        int x = 123;
        int y = -256;
        printf("The value of an unsigned integer is: %d, %d", x, y);
}

```

However also provides support for unsigned int.

```
#include <stdio.h>

int main(void)
{
        unsigned int x = 123;
        unsigned int y = -256;
        printf("The value of an unsigned integer is: %u, %u", x, y);
}

```

### In C++ :


```
#include <iostream>

int main()
{
        int x = 123;
        int y = -256;
        std::cout << "The value of x is: " << x << ", the value of y is: " << y;
}



```

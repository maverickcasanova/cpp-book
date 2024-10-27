# Chapter 7

## Array

### In C :

```
#include <stdio.h>

int main() {
    int my_array[5];

    size_t len = sizeof(my_array) / sizeof(my_array[0]);
    for(size_t i = 0; i < len; i++) {
        my_array[i] = i;
    }

    printf("%d\n", my_array[2]);
    return 0;
}

```

### In C++ :

```
#include <iostream>
#include <array>

int main() {
    std::array<int, 5> my_array;

    for(size_t i = 0; i < my_array.size(); i++) {
        my_array[i] = i;
    }

    std::cout << my_array[2] << std::endl;
    return 0;
}

```
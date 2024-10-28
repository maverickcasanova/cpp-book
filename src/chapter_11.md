# Chapter 11

## Struct

### In C :

```
#include <stdio.h>

struct my_struct {
    int x;
    int y;
};

int main() {
    struct my_struct object1;
    object1.x = 1;
    printf("%d\n", object1.x);
    return 0;
}

```

### In C++ :

```
#include <iostream>

struct my_struct {
    int x;
    int y;
};

int main() {
    struct my_struct object1;
    object1.x = 1;
    std::cout << object1.x << std::endl;
    return 0;
}

```

## Classes (In C++ Only) :

```

#include <iostream>

class human {
public:
    int height;
    int weight;
};

int main() {
    human john;
    john.height = 180;
    john.weight = 220;

    std::cout << john.height << std::endl;

    return 0;
}

```

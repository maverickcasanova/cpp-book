# Chapter 8

## Loops

### In C :

```
#include <stdio.h>

int main() {
    int a[] = {4, 5, 6, 7};
    for(int i = 1; i <= 3; i++)
    {
        printf("%d\n", a[i]);
    }
    return 0;
}

```

### In C++ :

```
#include <iostream>

int main() {
    int a[] = {4, 5, 6, 7};

    for(auto i : a)
    {
        std::cout << i << std::endl;
    }
    return 0;
}

```


```

#include <iostream>
#include <vector>
 
int main() {
    std::vector<int> v = {0, 1, 2, 3};
    for(auto i : v) { // access using const reference
        std::cout << i << std::endl;
    }
    return 0;
}

```
# Chapter 10

## Lambda Functions (Only in C++)

```
#include <iostream>

auto add = [] (int a, int b) {
   std::cout << "Sum = " << a + b;
};

int main() {

  add(10, 8);

  return 0;
}
```

```
#include <iostream>

auto multiply = [](int y)->int {
    return 2*y;
};


int main() {
    
    int x = 1;
    std::cout << multiply(x) << std::endl;
    
    x = 2;
    std::cout << multiply(x) << std::endl;

    return 0;
}
```
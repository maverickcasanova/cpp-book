# Chapter 5

## Printing strings

### In C :


```
#include <stdio.h>

int main(void)
{
        char* p = "Hello World!";
        printf("%s", p);
}
```

```
#include <stdio.h>

int main(void)
{
        char* p = "Hello World!";
        printf("%c", *p);
}

```





### In C++ :

```
#include <iostream>
#include <string>

int main()
{
        std::string s = "Hello World.";
        std::cout << s;
}

```
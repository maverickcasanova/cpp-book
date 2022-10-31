# Chapter 2

## Printing different values of char

### In C :
Printing decimal value.

```
#include <stdio.h>

int main(void)
{
  char mychar;
  mychar = 'a';
  printf("Decimal: %d Octal: %o Hexadecimal: %X", mychar, mychar, mychar);
}
```
Priting ASCII value

```
#include <stdio.h>

int main(void)
{
  char mychar;
  mychar = 'a';
  printf("%c", mychar);
}
```

### In C++ :
cout automatically prints ASCII value
```
#include <iostream>

int main()
{
  char mychar;
  mychar = 'a';
  std::cout << mychar;
}
```

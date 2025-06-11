# PCL Playground (Python-C Linked)

This is the **online playground** for [PCL](https://github.com/hejhdiss/pcl) – a minimal experimental compiler that lets you write and execute both Python and C code in a single `.pcl` file.

## Example Code

```pcl
%c name=mathmod export=add,g_counter
#include <stdio.h>

int g_counter = 0;

int add(int a, int b) {
    return a + b;
}
%endc

%py requires=mathmod
print("Sum 3 + 4 =", add(3, 4))
print("Counter before increment:", g_counter.value)
g_counter.value += 1
print("Counter after increment:", g_counter.value)
%endpy
```

## License

MIT License
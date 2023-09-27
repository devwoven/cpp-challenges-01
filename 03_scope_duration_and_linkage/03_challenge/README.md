# 課題 3

ヘッダーファイル`math_operations.h`で名前空間`MathOps`に基本的な算術演算(`addition`、`subtraction`、`multiplication`、`division`)の関数を宣言し、このヘッダーファイルをインクルードする C++プログラムを作成してください。これらの関数は別のファイル`math_operations.cpp`で実装し、メインプログラムファイル`main.cpp`で使用してください。このプログラムでは、ユーザーに 2 つの数値と、実行する演算の入力を求め、結果を表示するものとします。

### 例 1

入力:

```
Enter a calculation: 4 / 5
```

出力:

```
Result: 0.8
```

### 例 2

入力:

```
Enter a calculation: 24 - 6
```

出力:

```
Result: 18
```

---

**math_operations.h:**

```cpp
namespace MathOps {
    int add(int a, int b);
    int subtract(int a, int b);
    int multiply(int a, int b);
    double divide(int a, int b);
}
```

**math_operations.cpp:**

```cpp
#include "math_operations.h"

namespace MathOps {
    int add(int a, int b) {
        return a + b;
    }

    int subtract(int a, int b) {
        return a - b;
    }

    int multiply(int a, int b) {
        return a * b;
    }

    double divide(int a, int b) {
        return double(a) / double(b);
    }
}
```

**main.cpp:**

```cpp
#include <iostream>
#include "math_operations.h"

int main() {
    int a {};
    int b {};
    char operation {};

    for (;;) {
        std::cout << "Enter a calculation: ";
        std::cin >> a >> operation >> b;

        if (operation == '+') {
            std::cout << "Result: " << MathOps::add(a, b) << std::endl;
        } else if (operation == '-') {
            std::cout << "Result: " << MathOps::subtract(a, b) << std::endl;
        } else if (operation == '*') {
            std::cout << "Result: " << MathOps::multiply(a, b) << std::endl;
        } else if (operation == '/') {
            std::cout << "Result: " << MathOps::divide(a, b) << std::endl;
        } else {
            std::cout << "Invalid operation." << std::endl;
        }
    }

    return 0;
}
```

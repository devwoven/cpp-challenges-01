# 課題 1

ユーザーに数値の入力を求め、その値が正、負、ゼロのどれであるかを表示するプログラムを作成します。

---

```cpp
#include <iostream>

int main() {
    int number {};
    std::cout << "Enter a number: ";
    std::cin >> number;

    if (number > 0) {
        std::cout << "The number is positive." << std::endl;
    } else if (number < 0) {
        std::cout << "The number is negative." << std::endl;
    } else {
        std::cout << "The number is zero." << std::endl;
    }

    return 0;
}
```

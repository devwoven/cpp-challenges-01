# 課題 4

引数に`double`をとり、その数の平方根を返す関数`safe_sqrt`を作成します。引数が負の場合、"Cannot compute the square root of a negative number"というメッセージとともに`std::domain_error`をスローするようにします。main 関数で正の数と負の数の両方を指定して`safe_sqrt`を呼び出し、例外を適切に処理してください。

```cpp
#include <cmath>
#include <iostream>
#include <stdexcept>

// コードを入力してください

int main() {
    double positive_number { 9.0 };
    double negative_number { -4.0 };

    // コードを入力してください
}
```

---

```cpp
#include <cmath>
#include <iostream>
#include <stdexcept>

double safe_sqrt(double x) {
    if (x < 0) {
        throw std::domain_error("Cannot compute the square root of a negative number");
    }
    return std::sqrt(x);
}

int main() {
    double positive_number { 9.0 };
    double negative_number { -4.0 };

    try {
        std::cout << "Sqrt of " << positive_number << " is: " << safe_sqrt(positive_number) << std::endl;

        std::cout << "Sqrt of " << negative_number << " is: " << safe_sqrt(negative_number) << std::endl;
    } catch (const std::domain_error &e) {
        std::cout << "Error: " << e.what() << std::endl;
    }
}
```

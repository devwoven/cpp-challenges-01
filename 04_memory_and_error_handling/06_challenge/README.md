# 課題 6

`std::vector<int>`と整数型のインデックスを引数にとる関数`element_at`を作成します。この関数では、指定したインデックスにある vector の要素を返し、インデックスが範囲外の場合は適切なエラーメッセージとともに`std::out_of_range`例外をスローするようにします。main 関数で有効なインデックスと無効なインデックスの両方を指定して`element_at`を呼び出し、例外を適切に処理してください。

```cpp
#include <iostream>
#include <stdexcept>
#include <vector>

// コードを入力してください

int main() {
    std::vector<int> numbers = {1, 3, 5, 7, 9};

    // コードを入力してください
}
```

---

```cpp
int element_at(const std::vector<int> &numbers, int index) {
    if (index < 0 || index >= static_cast<int>(numbers.size())) {
        throw std::out_of_range("Index is out of bounds");
    }
    return numbers[index];
}

int main() {
    std::vector<int> numbers = {1, 3, 5, 7, 9};

    try {
        int valid_index = 2;
        std::cout << "Element at index " << valid_index << " is: " << element_at(numbers, valid_index) << std::endl;

        int invalid_index = 10;
        std::cout << "Element at index " << invalid_index << " is: " << element_at(numbers, invalid_index) << std::endl;
    } catch (const std::out_of_range &e) {
        std::cout << "Error: " << e.what() << std::endl;
    }
}
```

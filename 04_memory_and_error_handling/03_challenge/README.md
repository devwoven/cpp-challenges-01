# 課題 3

`std::vector<int>`を引数にとり、各要素の値を 2 倍にした新しい`std::vector<int>`を返す関数`double_elements`を作成します。次に、範囲ベースの for ループを使用して、元の vector と新しい vector の両方の要素を表示します。

```cpp
#include <iostream>
#include <vector>

// コードを入力してください

int main() {
    std::vector<int> numbers = {1, 2, 3, 4, 5};

    // コードを入力してください
}
```

---

```cpp
#include <iostream>
#include <vector>

std::vector<int> double_elements(const std::vector<int> &input) {
    std::vector<int> output;
    output.reserve(input.size());

    for (int element : input) {
        output.push_back(element * 2);
    }

    return output;
}

int main() {
    std::vector<int> numbers = {1, 2, 3, 4, 5};
    std::vector<int> doubled_numbers = double_elements(numbers);

    std::cout << "Original vector: ";
    for (int element : numbers) {
        std::cout << element << ' ';
    }
    std::cout << std::endl;

    std::cout << "Doubled vector: ";
    for (int element : doubled_numbers) {
        std::cout << element << ' ';
    }
    std::cout << std::endl;
}
```

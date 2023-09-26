# 課題 7

必要に応じて cppreference.com にある`std::vector`のドキュメントを確認し、この質問に答えてください。次のコードの出力はどのようになりますか。

```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> numbers;

    std::cout << "Initial size: " << numbers.size() << ", capacity: " << numbers.capacity() << std::endl;

    numbers.push_back(1);
    numbers.push_back(2);
    numbers.push_back(3);
    std::cout << "After adding elements: size: " << numbers.size() << ", capacity: " << numbers.capacity() << std::endl;

    numbers.reserve(10);
    std::cout << "After reserving space: size: " << numbers.size() << ", capacity: " << numbers.capacity() << std::endl;
}
```

---

```
Initial size: 0, capacity: 0
After adding elements: size: 3, capacity: 4
After reserving space: size: 3, capacity: 10
```

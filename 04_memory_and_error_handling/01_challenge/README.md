# 課題 1

整数型の変数`x`があります。この変数のメモリアドレスを表示するコードスニペットを書いてください。次に、`x`のアドレスを指す整数型ポインタ`p`を作成し、`p`が指すアドレスに格納されている値を出力します。

```cpp
#include <iostream>

int main() {
    int x = 42;

    // コードを入力してください
}
```

---

```cpp
#include <iostream>

int main() {
    int x = 42;

    std::cout << "Address of x: " << &x << std::endl;
    int *p = &x;
    std::cout << "Value pointed by p: " << *p << std::endl;
}
```

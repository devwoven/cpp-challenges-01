# 課題 3

ユーザーが入力した 3 つの数値の平均を計算するプログラムがあります。さまざまな値を入力してこのプログラムをテストしてください。プログラムは適切に動作しますか。適切に動作しない場合は、想定どおりの出力になるようにプログラムを修正してください。

```cpp
#include <iostream>

int main() {
    int num1;
    int num2;
    int num3;
    float average;

    std::cout << "Enter three numbers: ";
    std::cin >> num1 >> num2 >> num3;

    average = (num1 + num2 + num3) / 3;

    std::cout << "Average is: " << average << std::endl;

    return 0;
}
```

---

このプログラムは整数を入力すると適切に動作しますが、小数を入力すると正しい結果になりません。`num1`、`num2`、`num3`がすべて`int`型であることが原因です。これらの変数を`float`型に変更する必要があります。

```cpp
#include <iostream>

int main() {
    float num1;
    float num2;
    float num3;
    float average;

    std::cout << "Enter three numbers: ";
    std::cin >> num1 >> num2 >> num3;

    average = (num1 + num2 + num3) / 3;

    std::cout << "Average is: " << average << std::endl;

    return 0;
}
```

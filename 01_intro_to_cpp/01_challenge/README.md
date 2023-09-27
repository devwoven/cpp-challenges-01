# 課題 1
この課題では、C++の基本的な技術とキーワードの使い方を練習します。

## 必要な作業
- 以下のコードをコピーして新しい`.cpp`ファイルに貼り付けます。
- コード内のコメントを読み、その指示に沿ってタスクを完了します。
- コードをコンパイルして実行します。

エラーが表示されることなくコードをコンパイルして実行できれば、この課題は完了です。

```cpp
#include <iostream>
#include <string>


int main() {
    // このプログラムに書かれているすべての指示を完了してください。
    // プログラムをコンパイルして実行してください(エラーのない状態にしてください)。

    // データに適した型を使用して、以下の変数の宣言と初期化を完成させてください。
    pizzaSlices = 12;
    pi = 3.14159f;
    starsInTheUniverse = 1234567890LL;
    aLetter = 'k';
    aWord = "kaleidescope";
    veryPrecisePi = 3.14159265358979;
    thisIsTrue = true;
    thisIsAlsoTrue = thisIsTrue;


    // 新しい変数を3つ宣言して初期化してください(3行で記述、1行につき1つの変数)。各変数のデータ型が異なるようにしてください。
    // ここに変数1を記述
    // ここに変数2を記述
    // ここに変数3を記述


    // 正しいデータ型を指定して以下の配列を完成させてください。
    myArray[] = {1, 2, 3, 4}
    anotherArray[] = {3.5, 1.2, 6.7}


    // 独自の配列を作成し(1行で記述)、配列に5個以上の数値を格納します。数値のデータ型はどれでもかまいませんが、すべて同じデータ型にしてください。
    

    // この配列には大きな数値を格納するので、int型は適していません。どのデータ型が適切ですか。
    bigNumbers[] = {500000, 700000, 800000}


    // static_castを使用して、sizeOfCesiumAtomをint型に変更してください。static_castは、sizeOfCesiumAtomの次の行に記述してください。
    double sizeOfCesiumAtom = 0.267


    // 3つの定数変数を作成してください。データ型はどれでもかまいませんが、各変数のデータ型が異なるようにしてください。
    // ここに定数変数1を記述
    // ここに定数変数2を記述
    // ここに定数変数3を記述


    // オプションの課題: std::coutを使用して、static_castで作成した新しい変数を出力してください(1行で記述)。


    // 以下の行を変更する必要はありません。これらはプログラムの出力をチェックするためのものです。
    std::cout << pizzaSlices << std::endl;
    std::cout << pi << std::endl;
    std::cout << starsInTheUniverse << std::endl;
    std::cout << aLetter << std::endl;
    std::cout << aWord << std::endl;
    std::cout << veryPrecisePi << std::endl;
    std::cout << thisIsTrue << std::endl;
    std::cout << thisIsAlsoTrue << std::endl;
    std::cout << "The size of a Cesium atom in nanometers is: " << sizeOfCesiumAtom << std::endl;

    return 0;
}
```
# 課題 1

以下のコードについて考えてみましょう。

**temp_sensor.h**

```cpp
namespace Sensor {
    float readTemperature();
}
```

**temp_sensor.cpp**

```cpp
#include "temp_sensor.h"

float readTemperature() {
    return 25.5;
}
```

**main.cpp**

```cpp
#include <iostream>
#include "temp_sensor.h"

int main() {
    std::cout << "Temperature reading: " << readTemperature() << std::endl;
    return 0;
}
```

このプログラムをコンパイルして実行し、このエラーの原因となっているコードを修正してください。その際、コードを削除するのではなく、コードを追加して修正してください。

---

このコードの問題は、名前空間の使用に関連しています。関数`readTemperature()`は、`temp_sensor.h`で`Sensor`名前空間に宣言されていますが、`temp_sensor.cpp`ではグローバル名前空間で定義されています。同様に、`main.cpp`では、グローバル名前空間にあるものとして使用されています。

正しいコードは以下のようになります。

**temp_sensor.cpp**

```cpp
#include "temp_sensor.h"

namespace Sensor {
    float readTemperature() {
        return 25.5;
    }
}
```

**main.cpp**

```cpp
#include <iostream>
#include "temp_sensor.h"

int main() {
    std::cout << "Temperature reading: " << Sensor::readTemperature() << std::endl;
    return 0;
}
```

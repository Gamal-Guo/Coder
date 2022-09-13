# C++ Primer第五版

1. 小问题：cin的整个全过程？

2. 读取数量不定的输入数据代码：
   
   ```c++
   # include <iostream>
   int main() {
     int sum = 0, value = 0;
     while (std::cin >> value)
       sum += value;
     std::cout << "Sum is: " << sum << std::endl;
     return 0;
   }
   ```

3. 有符号数隐式转化为无符号数导致问题：
   
   ```c++
   unsigned u = 10;
   int i = -42;
   std::cout<<i+i<<std::endl;  //输出-84
   std: :cout << u + i << std: :endl; // 如果 int 占 32 位, 输出 4294967264
   ```

4. C++11中使用花括号完成初始化，被称为列表初始化：
   
   ```c++
   int units_sold{0};
   long double ld = 3.1415926536;
   int a{ld}, b = {ld}; //列表初始化会提醒出错，因为可能会丢失信息。
   ```

5. 默认初始化，任何函数体之外的变量被初始化为0；定义在函数体内部的内置类型变量将不被初始化。建议初始化每一个内置类型的变量。

6. 如果声明一个变量而非定义它，使用关键字extern，而且不要显示地初始化变量:
   
   ```c++
   extern int i; // 声明i而非定义i
   int j; // 声明并定义j
   extern double pi = 3.14; //定义，同时如果在函数体内这样做将出错
   ```
   
   ```变量能且只能被定义一次，但可以被多次声明。```
   
   如果想要在多个文件中使用同一个变量，就必须将声明和定义分离。

7. 

8. 

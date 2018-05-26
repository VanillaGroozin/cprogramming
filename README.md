# Программирование на языке Си
Гитхап репозиторий курса "Программирование на языке С"

[Домашние Задания](./homeworks/)

## Контент курса

### Модуль 2
1. Типы данных
    * С точки зрения языка программирования С данные в памяти имеют тип
    * Тип данных определяет диапазон значений, размер данных в байтах и что мы можем делать с этими данными, а также внутреннее представление данных в компьютере.
    * [Типы данных в С](https://ru.wikipedia.org/wiki/Типы_данных_в_C)
    * основные типы:
      * целые со знаком и без: `short`, `int`, `long`, `long long`, `unsigned short`,`unsigned int`,  и т.д.
      * символы `char`, как ни странно тоже бывают со знаком и без, `signed char`, `unsigned char`
      * вещественные `float`, `double`, `long double`
      * логический (булевый) тип, `bool`
      
2. Переменная
    * Переменная - имя кусочка памяти определенного типа.
    * Синтаксис объявления переменной: `type name;`
      - пример: `int a;`, `int a, b;`
    * Инициализация переменной - задание первого значения.
      - пример: `int a = 5;`, `int a=5, b=7;`
3. Ввод/вывод с консоли. [Скомпилировать и запустить.](http://cpp.sh/37plb)
```C++
   // ввод и вывод с консоли
   #include <iostream>
   using namespace std;
   int main(){
      int a,b;
      cout << "Enter a and b : "; // вывод строки запроса
      cin >> a >> b; // ввод a и b
      cout << "a = " << a << endl; // вывод a
      cout << "b = " << b << endl; // вывод b

      // замечательно входят и выходят ;)
   }
```

4. Константы и литералы
   * Константны с именем, это переменные защищенные словом `const` от перемен (парадокс!).
   ```cpp
   const int a = 6;
   a = 7; // здесь компилятор будет ругаться
   ```
   * Литералы - константы без имени, но которые тоже хранятся в памяти и имеют тип. В простонародье их называют просто "значениями".
   ```cpp
   int a = 5; // 5 - литерал типа int
   unsigned int b = 5u; // 5u или 5U - литерал типа unsigned int
   double d = 1.5; // 1.5 - литерал типа double
   float f = 1.5F; // 1.5F или 1.5f - литерал типа float
   char c = 'A'; // 'A' - литерал типа char
   ```

5. Операторы
   * оператор это символ или констуркция в языке С, которая говорит компилятору выполнит какие-либо арифметические, логические или други манипуляции...
   * арифметические операторы над числовыми и символьными типами
      * `+` `-`  `*` `/` `%`
   * логические операторы над булевыми типами
      * `>` `<` `>=` `<=` `==` `!=`
      * `&&`, `||`, `!`
   * операторы ветвлений
   ```cpp
   if (логическое выражение) выражение_1;
   
   if (логическое выражение) выражение_1; else выражение_2;
   
   if (логическое выражение) {
      выражение_1;
      выражение_2;
      ...
      выражение_n;
   }
   
   if (логическое выражение) {
      выражение_1;
      выражение_2;
      ...
      выражение_n;
   } else
   {
      выражение_1;
      выражение_2;
      ...
      выражение_m;
   }
   
   ```
   * по количеству **операндов** операторы бывают *унарные*, *бинарные*, и *тернарные*;
      * `(логическое_выражение ? if_true_выражение: if_false_выражение)` - тернарный оператор
   * оператор присваивания
      * сперва вычисляется значение правой стороны, затем оно копируется в переменную слева
      ```cpp
      a = 5;
      a = a + 1;
      ```
   * инкремент `++`
      * постфиксная форма
      ```cpp
      int a = 5;
      cout << ++a << endl; // сперва a станет 6, потом распечатается
      ```
      * префиксная форма
      
      ```cpp
      int a = 5;
      cout << a++ << endl; // сперва распечатается значение a, т.е. 5, затем a станет 6
      ```
   * декремент `--`, аналогичен инкременту
   * сокращенные формы присваивания
   ```cpp
   int a = 2;
   a += 5; // a = a + 5;
   a -= 7; // a = a - 7;
   a *= 2; // a = a * 2;
   a /= 4; // a = a / 4;
   a %= 3; // a = a % 3;
   ```
   * [более подробно про операторы](https://ru.wikipedia.org/wiki/Операторы_в_C_и_C%2B%2B)
    
6. Блок-схема -> прогамма

### Модуль 1

1. [Введение](./module01/введение.md)
2. [Алгоритм](https://ru.wikipedia.org/wiki/Алгоритм)
3. [Блок-схемы](https://ru.wikipedia.org/wiki/Блок-схема)
4. [Среда разработки MS Visual Studio 2015/2017](./module01/вижуал_студио.md)
5. [Первая программа](./module01/первая_программа.md)
6. [Классификация символов языка, лексемы и т.д.](http://cpp-cpp.blogspot.com/2013/10/c.html)
8. Библиотеки
9. [Компилятор, линковщик, интерпретатор](./module01/компиляция.md)
10. [Вывод данных в консоль](./module01/вывод_данных.md)
   ```cpp
   cout << "Hello World\n";
   ```
11. ESCAPE-последовательности
   * `\n` `\t` `\b` `\a` `\\` `\"`
12. RAW-строки
   * простая строка `"C:\\Program Files\\tablet\\amd64\\bin>"`
   * RAW-строка `R"(C:\Program Files\tablet\amd64\bin>)"`
13. Комментарии
   ```cpp
   // однострочные комментарии
   /*
      многострочные
      комментарии
   */
   ```

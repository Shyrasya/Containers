# Containers

## Содержание

1. [О проекте](#о-проекте)
2. [Особенности проекта](#особенности-проекта)
3. [Makefile](#makefile)
4. [Участники проекта](#участники-проекта)

## О проекте

В данном учебном проекте "Школы 21" была реализована собственная библиотека s21_containers.h и s21_containersplus.h, состоящая из основных контейнерных классов языка C++:
* List;
* Stack;
* Queue;
* Map;
* Set;
* Multiset;
* Vector;
* Array.

Контейнеры содержат набор стандартных методов и атрибутов для удобной работы с элементами, а также поддерживают проверку заполненности и итерацию по элементам.

### Список возможностей библиотеки:

* **List**: список, который позволяет эффективно вставлять и удалять элементы в произвольной позиции, но не обеспечивает быстрого доступа к элементам по индексу.
* **Stack**: контейнер, который реализуется с одним концом top по принципу LIFO (добавляет элементы в вершину стека и удаляет их оттуда).
* **Queue**: контейнер, который реализует очередь с двумя концами front и back по принципу FIFO ( позволяет добавлять элементы в конец очереди и удалять их из начала).
* **Map**: ассоциативный контейнер, который хранит отсортированные по возрастанию ключа пары ключ-значение и обеспечивает быстрый доступ к значениям по ключу.
* **Set**: контейнер, который хранит уникальные элементы в отсортированном порядке. Позволяет быстро проверять наличие элемента в контейнере и выполнять операции объединения и пересечения множеств.
* **Multiset**: контейнер, который хранит неуникальные элементы в отсортированном порядке. Позволяет быстро проверять наличие элемента в контейнере и выполнять операции объединения и пересечения множеств.
* **Vector**: динамический массив, который позволяет эффективно добавлять и удалять элементы в конец массива, а также обеспечивает быстрый доступ к элементам по индексу.
* **Array**: статический массив, который имеет фиксированный размер и обеспечивает быстрый доступ к элементам по индексу.


## Особенности проекта

В рамках учебного проекта неоходимо было соответствовать следующим требованиям:

* Программа разработана на языке C++ (стандарт 17), используется компилятор gcc;
* При написании кода необходимо придерживаться Google Style;
* Итераторы используются обязательно;
* Шаблонные классы реализованы с namespace "s21";
* Методы контейнерных классов полностью покрываются unit-тестами (используется GTest);
* Копирование оригинальной библиотеки STL запрещено. Однако логика работы с библиотекой (память, проверки, поведение в исключительных ситауциях) соблюдается.

## Makefile

Makefile проекта содержит следующие цели:

&nbsp;&nbsp;&nbsp;&nbsp;``all`` - включает в себя цели check, cppcheck, start_tests;

&nbsp;&nbsp;&nbsp;&nbsp;``test``, ``start_test`` - Запускает unit-тесты на проверку методов контейнерных классов с помощью библиотеки GTest;

&nbsp;&nbsp;&nbsp;&nbsp;``gcov_report`` - генерация html-отчета с помощью lcov для измерения покрытия кода тестами;

&nbsp;&nbsp;&nbsp;&nbsp;``check`` - анализирует код на стилистические нормы;

&nbsp;&nbsp;&nbsp;&nbsp;``cpp_check`` - проверка кода на ошибки, уязвимости, неправильное использование переменных, операторов;

&nbsp;&nbsp;&nbsp;&nbsp;``valgrind`` - проверка файла с тестами на возможные утечки;

&nbsp;&nbsp;&nbsp;&nbsp;``clean`` - удаляет файлы, созданные во время прохождения тестов, отчеты о покрытии.

## Участники проекта

| Участник      |            |
| ------------- | ------------------ |
| [lesleyle](https://github.com/IvanVito) | Map, Set, Multiset + tests |
| [karleenr](https://github.com/Karleenr) | List, Queue, Stack + tests |
| [lemongrb](https://github.com/Shyrasya) | Vector, Array + tests, Makefile |

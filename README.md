# ЯПЗТ Лабораторна №6

## Опис проєкту

Цей репозиторій містить проєкт Михайла Стецюка (Б-121-22-1-ПІ) для лабораторної №6 з
дисципліни «Якість програмного забезпечення та тестування» — застосунок для управління
задачами за підходом Kanban-дошки. Програма написана мовою C++ з використанням фреймворку
Qt 6. Встановлюється та використовується локально, тому дані зберігаються на компʼютері
у вигляді CSV файлу. Виконано та протестовано в інтегрованому середовищі розробки Qt
Creator на Fedora 41 із середовищем стільниці KDE Plasma 6.

### Структура каталогів

| Файл | Вміст |
|:----:|:-----:|
| .github/workflows/ | GitHub Actions pipeline |
| src/ | Вихідний код програми |
| tests/ | Unit-тести на GoogleTest |
| CMakeLists.txt | Конфігурація системи збірки CMake |
| LICENSE.txt | Ліцензія проєкту |
| README.md | Цей файл |
| sonar-project.properties | Налаштування SonarQube Cloud |

### Мінімальні системні вимоги (приблизні)

- Процесор: 2-х ядерний, 1 ГГц, amd64/x86_64
- Оперативна пам’ять: 512 МБ (2 ГБ рекомендується)
- Дисковий простір: 30 МБ (програма) + ~500 МБ (залежності)
- Відеокарта з підтримкою OpenGL 2.1+ або Vulkan
- Операційна система: Fedora 40+ / Ubuntu 22.04+ / Debian 12+ / Linux Mint 21+ / Windows 10+

## Залежності

*Fedora 41:*

```sh
sudo dnf install -y gcc-c++ cmake qt6-qtbase-devel
```

*Debian / Ubuntu / Linux Mint:*

```sh
sudo apt update
sudo apt install -y build-essential qt6-base-dev
```

*Windows 10/11:*

1. Встановіть [Qt 6.5+](https://www.qt.io/download) через Qt Online Installer.
2. Встановіть [CMake](https://cmake.org/download/) з офіційного сайту.
3. Використовуйте VS 2022+ або іншу IDE для збірки

Альтернативно можна використовувати Vcpkg чи Conan для керування пакунками.

## Збірка і запуск

Для збірки клонуйте репозиторій через Git, створіть теку build/, згенеруйте у ній makefiles
та скомпілюйте проєкт:

```sh
git clone https://github.com/yaBobJonez/YaPZT_Lab6.git
cd YaPZT_Lab6/
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
cmake --build .
```

Запустити виконувану програму можна подвійним натисканням або через термінал:
`./src/TaskList`. Для виконання тестів слід запускати `./tests/TaskList_Tests` у терміналі.

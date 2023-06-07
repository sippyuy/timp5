# Лабораторная работа №5

[![Coverage Status](https://coveralls.io/repos/github/ledibonibell/lab-05-1/badge.svg?branch=master)](https://coveralls.io/github/ledibonibell/lab-05-1?branch=master)

# Report-05
Данная лабораторная работа посвещена изучению фреймворков для тестирования на примере GTest

# Task 1
Создайте `CMakeList.txt` для библиотеки banking

Клонируем репозиторий 5 лабы для работы с библиотекой banking

Подключаем библиотеку gtest:                                               
- mkdir third-party                                         
- git submodule add https://github.com/google/googletest third-party/gtest                                               
- cd third-party/gtest && git checkout release-1.8.1 && cd ../..                                                              

![2](https://github.com/sippyuy/timp5/blob/master/screens/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2023-06-07_14-19-18.png)


- git add third-party
- git commit -m "added gtest framework"
- git push origin master

![](https://github.com/sippyuy/timp5/blob/master/screens/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2023-06-07_14-23-51.png)

Создадим файл CMake для banking:

- cd banking
- cat >> CMakeLists.txt << EOF
- nano CMakeLists.txt 

Содержимое файла CMakeLists.txt:

![](https://github.com/sippyuy/timp5/blob/master/screens/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2023-06-07_14-29-53.png)

- git add CMakeLists.txt 
- git commit -m "CMake - 1 - 1"
- git push origin master

Создадим другой CMake для tests:

- cat >> CMakeLists.txt << EOF
- nano CMakeLists.txt 

Содержимое файла CMakeLists.txt:

![](https://github.com/sippyuy/timp5/blob/master/screens/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2023-06-07_14-32-34.png)

- git add CMakeLists.txt 
- git commit -m "CMake - 1"
- git push origin master

# Task 2
Создайте модульные тесты на классы `Transaction` и `Account`
- Используйте mock-объекты
- Покрытие кода должно составлять 100%

Создадим `tests.cpp`:

- cat >> tests.cpp << EOF
- nano tests.cpp
- 
Содержимое файла tests.cpp:

![](https://github.com/sippyuy/timp5/blob/master/screens/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2023-06-07_14-34-46.png)

- git add tests.cpp
- git commit -m "Tests - 1"
- git push origin master

# Task 3 
Настройте сборочную процедуру на TravisCI

Создадим yml файл:

- mkdir .github
- cd ~/lab-05/.github
- mkdir workflows
- cd ~/lab-05/.github/workflows
- cat >> Action.yml << EOF
- nano Action.yml

Содержимое файла Action.yml:

![](https://github.com/sippyuy/timp5/blob/master/screens/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2023-06-07_14-35-38.png)

- git add Action.ymk
- git commit -m "Action - 1"
- git push origin master

# Task 4
Настройте Coveralls.io

- nano CMakeLists.txt 

Новое содержимое файла CMakeLists.txt:

![](https://github.com/sippyuy/timp5/blob/master/screens/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2023-06-07_14-37-14.png)

- git add CMakeLists.txt 
- git commit -m "CMake - 2"
- git push origin master

Поменяем файл сценария:

- cd ~/lab-05/.github/workflows
- nano Action.yml

Новое содержимое файла Action.ymk:

![](https://github.com/sippyuy/timp5/blob/master/screens/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2023-06-07_14-39-36.png)

- git add Action.ymk
- git commit -m "Action - 2"
- git push origin master

Регистрируемся на сайте `https://coveralls.io`

# MulticlassClassification
Это приложение демонстрирующее одну из частей моей библиотеки машинного обучения kazamori. Здесь при помощи FNN (Feed-Forward Neural Network) осуществляется классификация точек на плоскости, также в программе можно использовать метод KNN (K-Nearest Neighbors).
Для отрисовки всего используется SDL.

## Building 
### Windows
Для сборки этого проекта под Windows необходимо использовать компилятор MinGW (gcc) и Cmake, так как библиотеки SDL и SDL_ttf собраны под MinGW.
Чтобы собрать проект можно просто воспользовать маленьким скриптом, которые соберёт проект при помощи MinGW Makefiles в типе Debug.
``` bat
build
```
### Linux, macOS
Сборка невозможна, потому что я использую SDL и SDL_ttf собранные для MinGW.

## Executing
``` bat
build/main.exe
```

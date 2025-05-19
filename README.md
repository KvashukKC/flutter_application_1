# flutter_application_1

Порядок установки Flutter
Поскольку Flutter - фреймворк для ЯП Dart, то перед установкой первого необходимо установить Dart. Дальнейшая установка предполагает, что у вас уже установлен Visual Studio Code.

Установка менеджера пакетов Chocolatey

Запускаем PowerShell от имени администратора.
Выполняем команду Get-ExecutionPolicy. Если вывелось не Bypass, то выполняем следующие 3 команды (Они могут потребовать выбора действий. Выбираем Y или A):
Set-ExecutionPolicy AllSigned;
Set-ExecutionPolicy Bypass -Scope Process;
Get-ExecutionPolicy.
Выполняем команду Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1')).
Установка Dart SDK.

В том же PowerShell выполняем choco install dart-sdk. После установки PowerShell больше не понадобится.

Установка плагина Dart для VS Code

В панели расширений (Комбинация клавиш Ctrl + Shift + X) ищем и устанавливаем расширение Dart. После установки перезапускаем VS Code

Установка Flutter SDK

Переходим по ссылке для скачивания .zip архива. Разархивируем в удобное для вас место (для удобства я установил в C:/tools).

Изменение переменной среды

Изменяем переменную Path с добавлением адреса до папки из прошлого пункта. Обязательно до папки bin! В моем случае путь выглядит так: C:/tools/flutter/bin.

Установка плагина Flutter в VS Code

Все в полной аналогии как для Dart. После перезапуска переходим в Параметры (Ctrl + ,) и ищем пункт Dart: Flutter Sdk Path. Редактируем settings.json, добавив к параметру "dart.flutterSdkPath" путь до папки Flutter (уже без bin).

Источники:

https://codelab.pro/nastrojka-razrabotki-dart-v-visual-studio-code/
https://codelab.pro/kak-ustanovit-flutter-v-vs-code-poshagovoe-rukovodstvo/
https://ru.wikipedia.org/wiki/Flutter

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

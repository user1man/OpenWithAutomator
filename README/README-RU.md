# OpenWithAutomator
Readme на других языках:

[English :gb:](../../)

Этот репозиторий содержит сценарии Automator, которые помогут вам открывать файлы или папки в нужном вам приложении без запуска самого приложения. Просто воспользуйтесь быстрым действием в меню файла Finder.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./Images/RU/Finder-example-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="./Images/RU/Finder-example.png">
  <img width="50%" style="margin: 0 auto" alt="An example of what the script does" src="./Images/RU/Finder-example.png">
</picture>

## VS Code:
Чтобы открыть ваши файлы или каталоги в VS Code (Microsoft Visual Studio Code):
* [Загрузите скрипт](https://github.com/user1man/OpenWithAutomator/raw/main/Open%20in%20Fork.zip)
* Распакуйте архив
* Запустите файл из Zip

Вам не нужно предпринимать никаких дополнительных действий, чтобы использовать скрипт.

## Fork
[Fork](https://fork.dev) - это простой и понятный в использовании графический интерфейс для Git. Чтобы включить поддержку скриптов, перейдите в Настройки. Установите **Fork CLI** на вкладке *Integration* настроек в нижней части страницы.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./Images/Fork-cli-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="./Images/Fork-cli.png">
  <img width="50%" alt="Fork settings UI. Integration tab" src="./Images/Fork-cli.png">
</picture>

[Скачайте](https://github.com/user1man/OpenWithAutomator/raw/main/Open%20in%20Fork.zip), распакуйте архив, запустите и сохраните скрипт.

## Удаление и изменение
Все скрипты сохраняются по следующему пути:
```
/Users/YOUR_USER/Library/Services
```
Чтобы изменить сценарий, откройте его.

## Как это работает
Работа скрипта основывается на том, что при запуске быстрого действия в Automator передается путь к файлу, который используется для вызова любого приложения.
Поскольку команде может быть передано несколько путей, используется цикл For.
```bash
for f in "$@"
do
some your command here $f
done
```
Для использования значения f, используйте `$f` там, где вам это будет нужно.

## Создание собственного скрипта
- Откройте Automator
- Файл -> Новый -> Быстрое действие
- Измените «Процесс получает текущий элемент» в «файлы или папки» в «Finder» 
- Добавьте действие «Запустить Shell Script»
- Поменяйте «Передать входные данные» на «как аргументы» 
- Вставьте ваш скрипт
- Сохраните под нужным вам названием
Спасибо @tonysneed за [инструкцию](https://gist.github.com/tonysneed/f9f09bfa28bcf98e8d8306f9b21f99e2)

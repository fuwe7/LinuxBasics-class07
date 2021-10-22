## Занятие 7

Перед началом выполнения задания нужно создать ветку `task` и все задания выполнять в ней.

1. (1 балл) Модифицируйте файл [`.github/workflows/ci.yml`](.github/workflows/ci.yml) таким 
образом, чтобы автогрейдинг запускался в системе с установленной программой `cmatrix`.
2. (1 балл) Выясните установленную на Ubuntu-машине, выполняющей GitHub Actions, версию компилятора GHC командой `ghc --version` и сохраните её полный вывод в файл `ghc-version.txt` в корневой каталог репозитория. Этот шаг необходимо выполнить непосредственно перед запуском автогрейдинга в файле [`.github/workflows/ci.yml`](.github/workflows/ci.yml).
3. (2 балла) Разработайте workflow в файле [`.github/workflows/log-push.yml`](.github/workflows/log-push.yml), которое на каждом пуше добавляет в файл в корне репозитория с именем `push.log` строку с текущей датой и временем, после чего создаёт в ветке `task` коммит с сообщением `"log push"` и отправляет его на гитхаб.
4. (3 балла) Разработайте действие `Task04` в файле [`.github/actions/task04.yml`](.github/actions/task04.yml), 
которое создает файл с заданным именем в текущем каталоге, и организуйте его вызов для файла с именем `task04-result` непосредственно перед запуском автогрейдинга в файле [`.github/workflows/ci.yml`](.github/workflows/ci.yml).
5. (3 балла) Пользуясь [GitHub CLI](https://docs.github.com/en/actions/advanced-guides/using-github-cli-in-workflows) и GitHub Actions, организуйте автоматическое создание в репозитории issue с названием `Task 05` и меншеном  `@sloboegen98` в тексте. При каждом последующем пуше в репозиторий к этому issue должен добавляться комментарий с текстом `"yet another push"`.
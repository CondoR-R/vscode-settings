# Конфигурация VSCode / VSCodium

Репозиторий содержит файл личных настроек `settings.json` для редакторов VSCode и VSCodium. 

## Установка

Скопируйте файл `settings.json` в директорию с настройками вашего редактора:

| ОС | VSCode | VSCodium |
| --- | --- | --- |
| macOS | `~/Library/Application Support/Code/User/` | `~/Library/Application Support/VSCodium/User/` |
| Windows | `%APPDATA%\Code\User\` | `%APPDATA%\VSCodium\User\` |
| Linux | `~/.config/Code/User/` | `~/.config/VSCodium/User/` |

Вместо копирования можно создать симлинк, чтобы изменения в репозитории автоматически подхватывались:

```bash
ln -s ~/Projects/vscodium_config/settings.json ~/Library/Application Support/VSCodium/User/settings.json
```

После установки перезапустите редактор.

## Обзор настроек

### Интерфейс
- Sidebar справа, скрыт статус-бар
- Увеличенный zoom (`window.zoomLevel: 1`)
- Старт с пустой страницы вместо стартового вкладки
- Тёмная тема Kanagawa Wave

### Редактор
- Шрифт 18px, отступы — 4 пробела
- Скрыты скроллбары, minimap, хлебные крошки и липкий скролл
- Подсветка всех пробелов (`editor.renderWhitespace: "all"`)
- Курсор без мигания, отключены подсветка скобок и вхождений
- Фиксированный курсор и отключённая лампочка подсказок

### Автосохранение и форматирование
- Автосохранение после короткой паузы
- Форматирование при сохранении
- Добавление пустой строки в конец файла

### Оформление и упрощение
- Отключены подсказки, туториал и лампочки
- Поддержка плагина Todo Highlight
- Группировка (file nesting): JS/TS файлы, конфиги, БД, lock-файлы скрываются под основными файлами

### Python
- Форматирование через Black Formatter
- Автоматическая сортировка импортов через Ruff
- Отключено автоматическое создание виртуальных окружений

### VSCodium
- Отключены автообновления (`update.mode: "none"`)
- Приоритетная загрузка расширения vscode-neovim

## Необходимые расширения

Для полноценной работы некоторых настроек установите:

- [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme) — иконки проекта
- [Todo Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight) — подсветка TODO
- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) + [Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter) — форматирование Python
- [Ruff](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff) — линтер и сортировка импортов
- [Kanagawa Wave](https://github.com/the-flywheel/kanagawa-vscode) — цветовая тема

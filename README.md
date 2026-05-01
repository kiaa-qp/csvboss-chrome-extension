# CSVBOSS Chrome Extension EN

A Chrome extension for bulk managing Steam nicknames and friends — built for Rust clan Electricians.

---

## Features

**Nickname Manager**
Paste a CSV of Steam IDs and names, optionally add a clan tag prefix, and apply all nicknames in one click. Progress bar and per-entry log included.

**Remove All Nicknames**
Fetches your full friends list and clears every nickname at once — useful at the end of a wipe.

**Language Filter**
Filter CSV entries by language column before applying. Supports `ru`, `en`, and `cn` — useful when you only want to nickname a specific region's players.

**Friend Manager**
Use the same CSV to send bulk friend requests or unfriend players in bulk.

---

## CSV Format

```
steamid64,nickname
76561198000000001,PlayerOne,en
76561198000000002,PlayerTwo,ru
76561198000000003,PlayerThree
```

- `steamid64` — 17-digit Steam ID (required)
- `nickname` — the name to set (required)
- `language` — `ru`, `en`, or `cn` (optional, used for language filter)

---

## Installation

1. Go to the [Releases](https://github.com/kiaa-qp/csvboss-chrome-extension/releases) page and download the latest zip, or clone the repo
2. Open Chrome and go to `chrome://extensions`
3. Enable **Developer Mode** (toggle in the top right)
4. Click **Load unpacked** and select the `extension` folder (unzip the zipped folder you downloaded first)
5. Navigate to `https://steamcommunity.com/my/friends` — the panel will appear automatically

> The extension only works on `steamcommunity.com/*/friends*` pages and requires you to be logged into Steam in the same browser.

---

## Notes

- Nicknames are applied at ~1.5 seconds each due to Steam rate limits
- Your CSV and prefix are saved between sessions automatically
- The panel is draggable — click the header and drag it anywhere on the page
- **Error code 8** — already friends or request already pending
- **Error code 84** — their profile restricts incoming friend requests

############################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################################
# CSVBOSS Chrome Extension RU

Расширение для Chrome для массового управления никнеймами и друзьями в Steam — создано для клановых администраторов Rust.

---

## Функции

**Менеджер никнеймов**
Вставь CSV со Steam ID и именами, при необходимости добавь префикс клана и примени все никнеймы одним нажатием. Включает прогресс-бар и лог по каждой записи.

**Удалить все никнеймы**
Загружает полный список друзей и удаляет все никнеймы сразу — удобно в конце вайпа.

**Языковой фильтр**
Фильтрует записи CSV по столбцу языка перед применением. Поддерживает `ru`, `en` и `cn` — полезно, если нужно поставить никнеймы только игрокам определённого региона.

**Менеджер друзей**
Используй тот же CSV для массовой отправки заявок в друзья или удаления из друзей.

---

## Формат CSV

```
steamid64,nickname,language
76561198000000001,PlayerOne,en
76561198000000002,PlayerTwo,ru
76561198000000003,PlayerThree
```

- `steamid64` — 17-значный Steam ID (обязательно)
- `nickname` — никнейм для установки (обязательно)
- `language` — `ru`, `en` или `cn` (необязательно, используется для языкового фильтра)

---

## Установка

1. Перейди на страницу [Releases](https://github.com/kiaa-qp/csvboss-chrome-extension/releases) и скачай последний zip, либо клонируй репозиторий
2. Открой Chrome и перейди в `chrome://extensions`
3. Включи **Режим разработчика** (переключатель в правом верхнем углу)
4. Нажми **Загрузить распакованное расширение** и выбери папку `extension` (сначала распакуй скачанный zip)
5. Перейди на `https://steamcommunity.com/my/friends` — панель появится автоматически

> Расширение работает только на страницах `steamcommunity.com/*/friends*` и требует, чтобы ты был авторизован в Steam в том же браузере.

---

## Примечания

- Никнеймы применяются с задержкой ~1.5 секунды из-за ограничений Steam
- CSV и префикс сохраняются между сессиями автоматически
- Панель можно перетаскивать — кликни на заголовок и перемести в любое место страницы
- **Код ошибки 8** — уже в друзьях или заявка уже отправлена
- **Код ошибки 84** — профиль ограничивает входящие заявки в друзья

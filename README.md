# CSVBOSS Chrome Extension — EN

A Chrome extension for bulk managing Steam nicknames and friends — built for Rust clan leaders.

---

## Features

<br>

**Nickname Manager**
Paste a CSV of Steam IDs and names, optionally add a clan tag prefix, and apply all nicknames in one click. Progress bar and per-entry log included.

<br>

**Remove All Nicknames**
Fetches your full friends list and clears every nickname at once — useful at the end of a wipe.

<br>

**Friend Manager**
Use the same CSV to send bulk friend requests or unfriend players in bulk.

---

## CSV Format
steamid64,nickname
76561198000000001,PlayerOne
76561198000000002,PlayerTwo
76561198000000003,PlayerThree

- `steamid64` — 17-digit Steam ID (required)
- `nickname` — the name to set (required)

---

## Installation

1. Go to the [Releases](https://github.com/kiaa-qp/csvboss-chrome-extension/releases) page and download the latest zip, or clone the repo
2. Open Chrome and go to `chrome://extensions`
3. Enable **Developer Mode** (toggle in the top right)
4. Click **Load unpacked** and select the `extension` folder (unzip first)
5. Navigate to `https://steamcommunity.com/my/friends` — the panel will appear automatically

> The extension only works on `steamcommunity.com/*/friends*` pages and requires you to be logged into Steam in the same browser.

---

## Notes

- Nicknames are applied at ~1.5 seconds each due to Steam rate limits
- Your CSV and prefix are saved between sessions automatically
- The panel is draggable — click the header and drag it anywhere on the page
- **Error code 8** — already friends or request already pending
- **Error code 84** — their profile restricts incoming friend requests

---

<br><br>

---

# CSVBOSS Chrome Extension — RU

Расширение для Chrome для массового управления никнеймами и друзьями в Steam — создано для клановых администраторов Rust.

---

## Функции

<br>

**Менеджер никнеймов**
Вставь CSV со Steam ID и именами, при необходимости добавь префикс клана и примени все никнеймы одним нажатием. Включает прогресс-бар и лог по каждой записи.

<br>

**Удалить все никнеймы**
Загружает полный список друзей и удаляет все никнеймы сразу — удобно в конце вайпа.

<br>

**Менеджер друзей**
Используй тот же CSV для массовой отправки заявок в друзья или удаления из друзей.

---

## Формат CSV
steamid64,nickname
76561198000000001,PlayerOne
76561198000000002,PlayerTwo
76561198000000003,PlayerThree

- `steamid64` — 17-значный Steam ID (обязательно)
- `nickname` — никнейм для установки (обязательно)

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

---

<br><br>

---

# CSVBOSS Chrome Extension — TR

Steam'de toplu takma ad ve arkadaş yönetimi için bir Chrome eklentisi — Rust klan liderleri için yapılmıştır.

---

## Özellikler

<br>

**Takma Ad Yöneticisi**
Steam ID'leri ve isimleri içeren bir CSV yapıştırın, isteğe bağlı olarak klan etiketi öneki ekleyin ve tüm takma adları tek tıklamayla uygulayın. İlerleme çubuğu ve her kayıt için log dahildir.

<br>

**Tüm Takma Adları Kaldır**
Arkadaş listenizin tamamını çeker ve tüm takma adları bir kerede temizler — wipe sonunda kullanışlıdır.

<br>

**Arkadaş Yöneticisi**
Aynı CSV'yi kullanarak toplu arkadaşlık isteği gönderin veya oyuncuları toplu olarak arkadaşlıktan çıkarın.

---

## CSV Formatı
steamid64,nickname
76561198000000001,PlayerOne
76561198000000002,PlayerTwo
76561198000000003,PlayerThree

- `steamid64` — 17 haneli Steam ID (zorunlu)
- `nickname` — ayarlanacak takma ad (zorunlu)

---

## Kurulum

1. [Releases](https://github.com/kiaa-qp/csvboss-chrome-extension/releases) sayfasına gidin ve son zip dosyasını indirin veya repoyu klonlayın
2. Chrome'u açın ve `chrome://extensions` adresine gidin
3. **Geliştirici Modu**'nu etkinleştirin (sağ üst köşedeki geçiş)
4. **Paketlenmemiş yükle**'ye tıklayın ve `extension` klasörünü seçin (önce zip'i çıkarın)
5. `https://steamcommunity.com/my/friends` adresine gidin — panel otomatik olarak görünecektir

> Eklenti yalnızca `steamcommunity.com/*/friends*` sayfalarında çalışır ve aynı tarayıcıda Steam'e giriş yapmış olmanızı gerektirir.

---

## Notlar

- Steam hız sınırları nedeniyle takma adlar ~1.5 saniyede bir uygulanır
- CSV ve önekiniz oturumlar arasında otomatik olarak kaydedilir
- Panel sürüklenebilir — başlığa tıklayın ve sayfanın herhangi bir yerine taşıyın
- **Hata kodu 8** — zaten arkadaşsınız veya istek zaten beklemede
- **Hata kodu 84** — profilin gelen arkadaşlık isteklerini kısıtlıyor

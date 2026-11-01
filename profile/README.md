<img src="https://raw.githubusercontent.com/sovagrid/.github/main/profile/assets/sovagrid.svg" width="72" alt="SovaGrid">

# SovaGrid

Подключайте свои Ubuntu-серверы с телефона или компьютера. Установите Hub и веб-панель на выбранном вами сервере и добавляйте к ним другие серверы с отдельными Agent. SSH, мониторинг, терминал, файлы, Telegram и WireGuard работают без общего сервиса аккаунтов.

## Установка

[SovaGrid 1.0.0](https://github.com/sovagrid/sovagrid-blueprint/releases/tag/server-v1.0.0) устанавливает Hub, веб-панель, Agent и зависимости одной командой на пустой Ubuntu:

```sh
bash -o pipefail -c 'curl -fsSL https://raw.githubusercontent.com/sovagrid/sovagrid-blueprint/main/bootstrap/run.sh | sudo bash'
```

Установщик предложит публичный IPv4 или домен и путь панели. Корень сайта по умолчанию сохраняется. Для SSH-доступа без публичной панели выберите `-`. [Инструкция установки](https://github.com/sovagrid/sovagrid-blueprint/blob/main/QUICKSTART.md) объясняет каждый вариант; контрольные суммы находятся в серверном выпуске.

Без консоли используйте [Connect для macOS, Windows и Linux](https://github.com/sovagrid/sovagrid-connect/releases/tag/v1.0.0): введите SSH-адрес и пользователя, выберите ключ или пароль, подтвердите установку. Дополнительные Ubuntu-серверы подключаются из установленной панели. Есть [Android APK](https://github.com/sovagrid/sovagrid-android/releases/tag/v1.0.0), [приложение macOS и проект для iPhone/iPad](https://github.com/sovagrid/sovagrid-apple/releases/tag/v1.0.0), а также Web/PWA. Для личного iPhone используется Xcode и Apple ID; App Store не требуется.

## Возможности

- Прямой SSH по ключу или паролю, проверка отпечатка сервера, подключение через промежуточный SSH-хост и генерация Ed25519-ключей в клиентах.
- Свой Hub и аккаунты на каждом Ubuntu-хосте; роли администратора, оператора и наблюдателя, отдельные права на серверы, Telegram-бот с подтверждением команд.
- Мониторинг системы, процессов, разрешённых systemd-журналов, Docker-контейнеров и HTTP/TCP/DNS-проверок; инциденты и обслуживание.
- Веб-терминал, разрешённые файлы, управление отдельными службами, системная/светлая/тёмная темы и установка панели как PWA.
- WireGuard и поддерживаемый AmneziaWG: установка, управление клиентами и защищённая выдача профилей через явно включаемый broker. Автоматическая установка AmneziaWG поддерживает amd64.
- Резервная копия из пяти согласованных файлов, проверка и перенос поддерживаемой полной установки на чистую Ubuntu. Операция продолжается после отключения клиента; Web и Connect позволяют переподключиться к её состоянию.

Подписанные серверные обновления включаются отдельно в настройках: занятый сервер откладывает замену, ошибочный кандидат откатывается. Токен Telegram вводится в панели. Применение общих параметров AWG3 доступно только при отсутствии клиентов и после отдельного разрешения администратора.

Переносимые копии пока не включают изменяемые данные контейнера AmneziaWG и SSH-транспорты внешних Agent; такие Agent после переноса Hub подключаются заново. Полные условия и следующие направления — в [плане развития](https://github.com/sovagrid/sovagrid-blueprint/blob/main/ROADMAP.md).

## Репозитории

| Компонент | Код |
| --- | --- |
| Hub, аккаунты, API, Telegram | [sovagrid-hub](https://github.com/sovagrid/sovagrid-hub) |
| Ubuntu Agent | [sovagrid-agent](https://github.com/sovagrid/sovagrid-agent) |
| Веб-панель | [sovagrid-web](https://github.com/sovagrid/sovagrid-web) |
| iPhone, iPad, macOS | [sovagrid-apple](https://github.com/sovagrid/sovagrid-apple) |
| Android | [sovagrid-android](https://github.com/sovagrid/sovagrid-android) |
| Connect и графический установщик | [sovagrid-connect](https://github.com/sovagrid/sovagrid-connect) |
| WireGuard и AmneziaWG | [sovagrid-vpn](https://github.com/sovagrid/sovagrid-vpn) |
| Установка, документация, roadmap | [sovagrid-blueprint](https://github.com/sovagrid/sovagrid-blueprint) |
| Подписанный канал обновлений | [sovagrid-update-feed](https://github.com/sovagrid/sovagrid-update-feed) |

**Copyright (C) 2026 [Jigokuraku01](https://github.com/Jigokuraku01).** Оригинальный код распространяется по [GNU AGPLv3-only](https://github.com/sovagrid/.github/blob/main/LICENSE) с [условием сохранения авторской подписи](https://github.com/sovagrid/.github/blob/main/ATTRIBUTION.md) по разделу 7(b). Сторонние компоненты сохраняют собственные лицензии.

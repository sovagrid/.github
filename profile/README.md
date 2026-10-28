<img src="https://raw.githubusercontent.com/sovagrid/.github/main/profile/assets/sovagrid.svg" width="72" alt="SovaGrid">

# SovaGrid

Подключайте свои Ubuntu-серверы с телефона или компьютера. SSH, мониторинг, терминал, файлы, Telegram, WireGuard и веб-панель работают с вашим Hub на каждом сервере. Общий сервис аккаунтов не нужен.

## Установка

[SovaGrid Blueprint](https://github.com/sovagrid/sovagrid-blueprint) содержит `run.sh`, сценарии Docker Compose и [инструкцию первой установки](https://github.com/sovagrid/sovagrid-blueprint/blob/main/QUICKSTART.md). Для сервера нужен Ubuntu и SSH-доступ администратора. Hub и учётные записи создаются на вашем сервере; общего сервиса аккаунтов нет.

[Актуальный серверный пакет 0.10.0-preview](https://github.com/sovagrid/sovagrid-blueprint/releases/tag/v0.10.0-preview) содержит пять проверенных серверных компонентов. SHA-256 архива: `275c5f03c30b1a924b1fcb48067a41f7b76481cd4c249589a7c8b5098db749fb`. Его можно выбрать в графическом установщике либо установить вручную по инструкции. Исходники приложений доступны в репозиториях ниже.

## Возможности

- Прямой SSH по ключу или паролю, проверка отпечатка сервера, подключение через промежуточный SSH-хост и генерация Ed25519-ключей в клиентах.
- Свой Hub и аккаунты на каждом Ubuntu-хосте; роли администратора, оператора и наблюдателя, отдельные права на серверы, Telegram-бот с подтверждением команд.
- Мониторинг системы, процессов, разрешённых systemd-журналов, Docker-контейнеров и HTTP/TCP/DNS-проверок; инциденты и обслуживание.
- Веб-терминал, разрешённые файлы, управление отдельными службами, системная/светлая/тёмная темы и установка панели как PWA.
- Собственный WireGuard с клиентскими профилями и маршрутом; существующий AmneziaWG наблюдается отдельно. Управление peer доступно через явно включаемый broker.
- Закрытые копии данных Hub и управляемого состояния хоста. Панель и Connect показывают план, проверку и ход копирования; при отключении Hub восстановление служб доступно через Connect по SSH.

Применение общих параметров AWG3 доступно только при отсутствии клиентов и после отдельного разрешения администратора. Подписанный канал поиска новых стабильных серверных релизов пока выключен; одноразовое обновление с проверкой пакета и откатом доступно через Connect.

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
| Подготовка подписанного канала обновлений | [sovagrid-update-feed](https://github.com/sovagrid/sovagrid-update-feed) |

**Copyright (C) 2026 [Jigokuraku01](https://github.com/Jigokuraku01).** Оригинальный код распространяется по [GNU AGPLv3-only](https://github.com/sovagrid/.github/blob/main/LICENSE) с [условием сохранения авторской подписи](https://github.com/sovagrid/.github/blob/main/ATTRIBUTION.md) по разделу 7(b). Сторонние компоненты сохраняют собственные лицензии.

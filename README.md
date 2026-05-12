<div align="center">
  <img src="https://github.com/user-attachments/assets/e46cdd01-ffef-4c51-bdb5-daeaafb0c2e7" alt="ArtVPN Logo" width="120" />
  
  <h1>🛡️ ArtVPN Pro</h1>
  <p><b>Умный, быстрый и современный VPN-клиент с продвинутым обходом блокировок (DPI).</b></p>

  [![Latest Release](https://img.shields.io/github/v/release/ArtsoftTeam/ArtVPN-Release?color=00F2FF&label=Latest%20Release&style=for-the-badge)](https://github.com/ArtsoftTeam/ArtVPN-Release/releases)
  [![Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android)](#)
  [![Xray-core](https://img.shields.io/badge/Powered%20by-Xray--core-blue?style=for-the-badge)](#)
</div>

<br/>

**ArtVPN Pro** — это клиентское приложение для Android на базе **Xray-core**, созданное с упором на максимальную производительность, красивый дизайн и бесшовный опыт использования. Главная фишка приложения — умный DPI-режим, который пускает через прокси только то, что нужно.

---

## ✨ Ключевые возможности

- 🚀 **Умный обход (DPI Mode)**: Больше не нужно выключать VPN, чтобы зайти в банковское приложение! Режим DPI автоматически направляет заблокированные сервисы (YouTube, Discord, Instagram, Twitter) через прокси. Российские сервисы, банки и локальные сайты работают напрямую на максимальной скорости.
- 📞 **Идеальные голосовые звонки**: Специально настроенная маршрутизация UDP-трафика и WebRTC (порты 50000-65535) обеспечивает работу голосовых каналов Discord и WhatsApp без прерываний и "глухих" звонков.
- 🔄 **Умное переключение серверов (Failover)**: Добавьте до 5 серверов. Если текущий сервер недоступен или завис, ArtVPN мгновенно и незаметно переключится на следующий рабочий сервер.
- 🎯 **Раздельное туннелирование (Split Tunneling)**: Самостоятельно выбирайте, какие приложения будут использовать VPN, а какие — идти напрямую.
- 🛡️ **Защита от утечек (Kill Switch)**: Полная интеграция с Android Always-on VPN. Если связь оборвётся, ваш реальный IP-адрес не утечёт в сеть.
- 📋 **Умный буфер обмена**: Скопируйте ключ VLESS/VMess/Trojan из Telegram или браузера, откройте ArtVPN — и приложение само предложит добавить новый сервер!
- 📡 **Обход провайдерских "Белых списков"**: Специальный режим, маскирующий трафик и позволяющий пробиться даже через самые жесткие ограничения провайдера (когда работают только избранные сайты).

---

## 📸 Скриншоты интерфейса

<div align="center">
  <table>
    <tr>
      <td align="center"><b>Главный экран</b></td>
      <td align="center"><b>Статистика</b></td>
      <td align="center"><b>Сервера</b></td>
    </tr>
    <tr>
      <td align="center"><img src="https://github.com/user-attachments/assets/ed487cae-02a5-4282-8409-bf5d37abed84" width="220"/></td>
      <td align="center"><img src="https://github.com/user-attachments/assets/2096583f-a9f2-41ef-a2c4-118038db711a" width="220"/></td>
      <td align="center"><img src="https://github.com/user-attachments/assets/0601ad47-c78d-43c1-bf3f-d82a60151731" width="220"/></td>
    </tr>
  </table>
  
  <table>
    <tr>
      <td align="center"><b>Настройки</b></td>
      <td align="center"><b>Туннелирование</b></td>
    </tr>
    <tr>
      <td align="center"><img src="https://github.com/user-attachments/assets/a6221dc4-7dc0-4802-ba0a-a34c01c71df7"  width="220"/></td>
      <td align="center"><img src="https://github.com/user-attachments/assets/11b84b2e-9283-4144-a23f-105764516014" width="220"/></td>
    </tr>
  </table>
</div>

---

## 📥 Как установить?

1. Перейдите в раздел [**Releases**](https://github.com/ArtsoftTeam/ArtVPN-Release/releases) справа.
2. Скачайте самый свежий файл `app-release.apk`.
3. Установите его на ваше Android устройство (возможно, потребуется разрешить установку из неизвестных источников).
4. **Готово!** Приложение будет автоматически проверять наличие новых версий (OTA-обновления) и предлагать обновиться прямо внутри интерфейса.

---

## ⚙️ Технические детали для гиков

Приложение использует кастомный движок на базе Xray-core (v26.5.9).  
Конфигурация маршрутизации (Routing) разделена на несколько этапов:
1. `geoip:ru` и `geoip:private` — всегда направляются `direct`.
2. Популярные RU-домены (sber.ru, gosuslugi.ru, yandex.ru и т.д.) — `direct`.
3. Специфичные пулы IP-адресов Telegram, Discord и WhatsApp — `proxy`.
4. Известные заблокированные домены (`geosite:youtube`, `domain:instagram.com` и др.) — `proxy`.
5. UDP-порты голосового трафика (WebRTC 50000-65535, 5222, 3478) — `proxy` для стабильной связи.
6. Блокировка QUIC (UDP 443) для форсирования TCP/HTTP2 (опционально, отключается при обходе белых списков).

---
<div align="center">
  <b>Разработано с ❤️ для свободного интернета.</b>
</div>

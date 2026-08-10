<p align="center">
  <strong>🇷🇺 Русский</strong> ·
  <a href="README.fa.md">🇮🇷 فارسی</a> ·
  <a href="README.en.md">🇬🇧 English</a> ·
  <a href="README.zh.md">🇨🇳 中文</a>
</p>

# BT шаблон PasarGuard

![Russian template preview](assets/preview.webp)


## Ручная установка
1. копируем файл index.html
2. в .env файле панели указываем CUSTOM_TEMPLATES_DIRECTORY и SUBSCRIPTION_PAGE_TEMPLATE
3. Если CUSTOM_TEMPLATES_DIRECTORY отличается от /var/lib/pasarguard/*, то открываем docker-compose.yml и вписываем volumes: вашей директории
4. в консоле ```bash pasarguard restart```

## Быстрая установка из GitHub

```bash
curl -fsSL https://raw.githubusercontent.com/7Berlin/pasarguard-neon-template/main/install.sh | sudo bash -s -- --activate
```

Команда устанавливает и активирует шаблон только с **русским языком**.

## Команды установки

| Команда | Описание |
|---|---|
| `sudo bash install.sh --activate` | Установка с русским языком по умолчанию |
| `sudo bash install.sh --activate -fa -en` | Персидский и английский; персидский по умолчанию |
| `sudo bash install.sh --activate -en -ru --default-lang en` | Английский и русский; английский по умолчанию |
| `sudo bash install.sh --activate -fa -en -ru -zh` | Установка всех языков |
| `sudo bash install.sh --activate --config ./template.conf` | Установка с пользовательской конфигурацией |

| Флаг | Язык |
|---|---|
| `-ru` | 🇷🇺 Русский |
| `-fa` | 🇮🇷 Персидский |
| `-en` | 🇬🇧 Английский |
| `-zh` | 🇨🇳 Китайский |

## Настройка шаблона

Измените `template.conf` и повторно запустите установку:

```bash
git clone https://github.com/7Berlin/pasarguard-neon-template.git
cd pasarguard-neon-template
nano template.conf
sudo bash install.sh --activate --config ./template.conf
```

| Параметр | Назначение |
|---|---|
| `BRAND_NAME` | Название сервиса |
| `BRAND_SUBTITLE` | Текст под именем пользователя |
| `AVATAR_URL` | URL изображения профиля или логотипа |
| `AVATAR_FILE` | Локальный PNG, JPG, WEBP, GIF или SVG |
| `PRIMARY_COLOR` | Основной цвет |
| `SECONDARY_COLOR` | Второй цвет |
| `CYAN_COLOR` | Акцентный цвет |
| `DEFAULT_THEME` | Тема `dark` или `light` |
| `SUPPORT_URL` | Ссылка на инструкцию или поддержку |
| `PANEL_DOMAIN` | Домен панели при необходимости |

Поддержите проект звездой на GitHub ⭐

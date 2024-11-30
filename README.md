# voverehouse
# VOvereHouse Plugin

A Minecraft plugin for managing houses and apartments with region-based ownership.

## Features

- Buy and sell houses using signs
- Region-based house protection
- House ownership management
- House price configuration
- Tax system for house ownership
- Permission-based command system

## Requirements

- Minecraft 1.16.5
- WorldEdit
- WorldGuard
- Vault (for economy support)

## Installation

1. Place the plugin JAR file in your server's `plugins` folder
2. Install the required dependencies (WorldEdit, WorldGuard, Vault)
3. Restart your server
4. Configure the plugin in `config.yml`

## Commands

- `/buyhouse` - Buy a house (must be looking at a house sign)
- `/sellhouse` - Sell your current house
- `/createhouse <name>` - Create a new house region
- `/deletehouse` - Delete a house region
- `/setpricehouse <price>` - Set the price of a house
- `/givehouse <player>` - Give your house to another player
- `/houseclaim` - Confirm a house action (buy/sell/give)


# VOvereHouse - Плагин управления домами

## Описание
VOvereHouse - это плагин для Minecraft 1.16.5, который добавляет систему покупки и продажи домов на вашем сервере. Плагин интегрируется с WorldGuard для защиты регионов и Vault для экономики.

## Возможности
- Создание домов с автоматической нумерацией
- Покупка и продажа домов через таблички
- Интеграция с экономикой сервера (Vault)
- Автоматическое обновление табличек
- Защита регионов с помощью WorldGuard

## Команды
- `/createhouse <цена> [номер]` - Создать новый дом (требуется право minehouse.create)
  - Если номер не указан, будет использован следующий свободный
- `/housewand` - Получить палочку для выделения региона
- `/gethousesign <номер>` - Получить табличку для дома
- `/buyhouse` - Купить дом (смотря на табличку)
- `/sellhouse <цена>` - Выставить свой дом на продажу
- `/deletehouse` - Удалить дом (требуется право minehouse.delete)
- `/setpricehouse <цена>` - Изменить цену дома
- `/househelp` - Показать справку по командам

## Права доступа
- `minehouse.create` - Создание домов
- `minehouse.delete` - Удаление домов
- `minehouse.buy` - Покупка домов
- `minehouse.sell` - Продажа домов
- `minehouse.sign` - Создание табличек
- `minehouse.admin` - Все права

## Зависимости
- WorldGuard
- WorldEdit
- Vault
- CMI Economy (опционально)

## Установка
1. Скопируйте файл плагина в папку plugins
2. Перезапустите сервер
3. Настройте права доступа в permissions.yml или через плагин прав

## Использование
1. Админ создает дом командой `/createhouse 1000`
2. Игрок находит табличку с домом
3. Игрок смотрит на табличку и пишет `/buyhouse`
4. После покупки дом автоматически закрепляется за игроком
5. Владелец может продать дом командой `/sellhouse 1500`

## Конфигурация
Плагин автоматически сохраняет:
- Цены домов
- Статус продажи
- Последний использованный номер дома
- Владельцев домов

## Автообновление
Таблички автоматически обновляются каждый час для отображения актуальной информации о владельце и статусе продажи. 

# VOvereHouse - Плагин управления домами

## Описание
VOvereHouse - это мощный плагин для управления домами на вашем Minecraft сервере. Он позволяет игрокам покупать, продавать и управлять своими домами с помощью удобной системы табличек и команд.

## Права доступа

### Административные права
| Право | Описание |
|-------|-----------|
| `voverehouse.admin` | Доступ ко всем командам плагина |
| `voverehouse.housewand` | Использование палочки для создания домов |
| `voverehouse.create` | Создание новых домов |
| `voverehouse.delete` | Удаление домов |
| `voverehouse.setprice` | Изменение цены домов |
| `voverehouse.sign` | Создание табличек для домов |

### Пользовательские права
| Право | Описание |
|-------|-----------|
| `voverehouse.use` | Базовые права для игроков |
| `voverehouse.buy` | Покупка домов |
| `voverehouse.sell` | Продажа домов |

## Таблички
Таблички автоматически обновляются и показывают:
- Номер дома
- Статус (продается/занят)
- Цену (если дом продается)
- Владельца (если дом занят)

### Взаимодействие с табличками
- **Покупка**: Нажмите ПКМ по табличке, чтобы купить дом
- **Отмена продажи**: Владелец может нажать ПКМ по табличке своего дома, чтобы отменить продажу

## Конфигурация
Все настройки хранятся в файле `config.yml`:
- Цены домов
- Расположение схем домов
- Настройки экономики

## Защита
- Только владелец и члены дома могут изменять его
- Дома защищены от гриферства
- При продаже дом автоматически сбрасывается
- Владелец не может изменять дом, пока он в продаже

## Важные заметки
1. При выставлении дома на продажу:
   - Дом будет сброшен к исходному состоянию
   - Владелец не сможет изменять дом
   - Появится GUI подтверждения
2. При отмене продажи:
   - Владелец снова получит доступ к дому
   - Все таблички автоматически обновятся
3. Цены форматируются с разделителями для удобства
   (например: 1 000 000$)

## Установка
1. Скопируйте файл плагина в папку `plugins`
2. Установите необходимые зависимости (Vault, WorldGuard, WorldEdit)
3. Перезапустите сервер
4. Настройте права доступа в файле permissions.yml
5. Готово к использованию!

# 

Бот для мини-игры ["Рабы" ("Рабство")](https://vk.com/app7794757) ВК
Если в консоль пишется какой-то бред, значит у Вас бан на пару часов.

## Установка на Windows

- Устанавливаем [Python](https://www.python.org/downloads/windows). Во время установки ставим галочку **Add Python to PATH (Добавить Python в PATH)**
- [Скачиваем архив с ботом](https://github.com/Kreont1/slavebot/archive/refs/heads/main.zip).
- Распаковываем архив.
- Редактируем файл **config.json**:
	- authorization:
		- Открываем ВК
		- Нажимаем F12 (Для Chromium браузеров)
		- В появившейся панели выбираем вкладку Network
		- Находим кнопку Filter (воронка)
		- В появившемся поле пишем buySlave
		- Покупаем любого раба
		- В панели появится поле buySlave, нажимаем по нему
		- Появится еще одна панель, выбираем в ней вкладку Headers
		- Ищем поле **authorization**
		- Копируем его значение (начинается на vk_access_token_settings)
		- Вставляем скопированное значение в значение **authorization** в **config.json**
	- buy_slaves - покупать ли рабов (0 - выкл, 1 - вкл)
	- buy_fetters - покупать ли оковы (0 - выкл, 1 - вкл)
	- job - какую давать работу
	- delay - задержка в секундах. Низкие значения приведут к бану на несколько часов. Программа работает только при значении больше 1.0

Запуск: **start.bat**.

## Установка на Termux (Android)

- Устанавливаем Termux, желательно с F-Droid, т.к. в Google Play разработчик его больше не обновляет.
- Запускаем Termux.
- Пишем по порядку:
	- cd
	- pkg install -y git
	- git clone https://github.com/Kreont1/slavebot
	- sh vk-slaves-bot/termux.sh
- Редактируем файл **config.json** или перекидываем с компьютера имеющийся. О том, как сделать это, можете почитать в интернете.

Запуск: python vk-slaves-bot/bot.py

## Установка на Testflight (iOS)

Скоро...

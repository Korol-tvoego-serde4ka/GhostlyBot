# GhostlyBot
![GhostlyBot Logo](https://i.imgur.com/lD2Gb42.png)
Юзер-бот для ВК на Golang

## Важная информация!
Это моя первая программа на Golang. Здесь очень много костылей, багов и нелогичных решений в купе с не соблюдением многих условностей языка. Использовать на свой страх и риск!

## Пример
https://vk.com/id574715826

## Сборка
1. Необходимо установить Golang 1.14
2. `git clone https://github.com/WheatleyHDD/GhostlyBot`
3. `cd GhostlyBot`
4. `go build`

## Настройка
### PhasesDB.txt
Это файл с базой ответов в формате:
вопрос|ответ|вложение(если необходимо)

Например:
```
Привет|Здравствуй|
Как дела?|Все хорошо, а у тебя|
Какой твой любимый мем?|Этот|photo574715826_457239130
```

[Python-скрипт для конвертации базы с FP iHA Bot на базу GhostlyBot](https://github.com/WheatleyHDD/GhostBDGen)

### settings.json
Костяк всего и вся. Самое важное поле: "access_token"
Получить access_token можно здесь: https://vkhost.github.io/

Описание других полей:
| Поле                   | Описание                                                                                              |
|------------------------|-------------------------------------------------------------------------------------------------------|
| access_token           | Уже выяснили                                                                                          |
| appeal                 | Обращение к боту (их два: "бот, " и этот)                                                             |
| help_text              | Сообщение, которое надо показать при команде "помощь"                                                 |
| about                  | Сообщение, которое надо показать при команде "о боте"                                                 |
| walls                  | Список стен, которые надо проверять на сообщения к боту                                               |
| onAttemptToBlock       | Что написать пользователю, если в его сообщении есть запрещенные слова (список в blacklist.txt)       |
| commandOnWallDontWorks | Что написать пользователю, если команда не работает на стенах                                         |
| statistic              | Собирать статистику (если true, то вся статистика по использованным командам сохраняется в папке BDs) |
| message_list           | Изменение некоторых ответов под бота (смотри уже написанные примеры)                                  |

### blacklist.txt
Список запрещенных слов. Каждое слово и словосочетание с новой строки

## Команды
Все команды бота расписаны в этой статье: https://vk.com/@ghostlybot-komandy

## Важные файлы, которые должны быть в одной папке с исполняемым файлом
* папка BDs
* blacklist.txt
* settings.json
* PhasesBD.txt
* lobster.ttf
* и сам исполняемый файл

## Контакты
Группа бота: https://vk.com/ghostlybot
Разработчик: https://vk.com/dimasas2

# GhostlyBot
![GhostlyBot Logo](https://i.imgur.com/lD2Gb42.png)
Юзер-бот для ВК на Golang

## Важная информация!
Программа не моя, данный бот был написан Дмитрием Волковым(надеюсь правильно написал). Вот его репо: https://github.com/WheatleyHDD/GhostlyBot 

## В чём отличия твоего кода от Дименого?
На данный момент не в чём, как выйдет v3, то всё опишу. Но пока я лишь запустил его и поддерживаю рабочим.
Вот ссылочка: https://vk.com/h0m3us3r 
Я планирую его поддерживать и обновлять(если будет время, ибо я студент с подработкой и личной жизнью).

## Сборка
1. Необходимо установить Golang 1.14
2. `git clone https://github.com/Korol-tvoego-serde4ka/GhostlyBot`
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

[Python-скрипт для конвертации базы с FP iHA Bot на базу GhostlyBot](https://github.com/Korol-tvoego-serde4ka/GhostBDGen)

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
Все команды бота расписаны в этой статье: https://m.vk.com/@neurotoxinbot-komandy

## Важные файлы, которые должны быть в одной папке с исполняемым файлом
* папка BDs
* blacklist.txt
* settings.json
* PhasesBD.txt
* lobster.ttf
* и сам исполняемый файл

## Сбор статистики
https://github.com/Korol-tvoego-serde4ka/GhostlyBotStat

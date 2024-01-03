---
title: "Переезд Блога на другой хостинг и смена технологий."
date: 2024-01-03T11:30:03+00:00
tags: ["Блог", "GitHub", "Hugo"]
author: "Aull Nikita"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
#description: "Desc Text."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<text>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---

![github](/github.png 'github')

Заметил я такую странную штуку, когда я публиковал новый пост у себя в блоге, первые 3-4 дня сайт зависал от повышенной нагрузки:)   
Получается сайту хватало нагрузки в 3-5 одновременных пользователей чтобы зависнуть:)

Я понимаю почему это происходило:   
- Хостился блог на самом маленьком из возможных серверов на Амазоне.   
- Связка WordPress, Apache и MySQL достаточно прожорливая.   
- Плюс я всё это обвешал всякими мониторингами.   

Случились эти зависания несколько раз и стал терять всякое желание писать посты в блоге, потому что стал сильно расстраиваться, что всё это работает нестабильно. А дополнительного времени для оптимизации и поиска проблем я выделить не мог.

Я стал задумываться о ведении блога только в телеграм.   
Это просто, быстро, современно.   
Плюс есть специальный сервис https://telegra.ph/, который позволяет делать большие посты и пользоваться возможностями разметки.   
Но тогда вставал вопрос, а как же приобретенный красивый домен www.aull.me?   
При переходе чисто в телеграм, исчезала "ламповость" и олдскульность всей этой затеи.   
Ну и при ведении блога в телеграме совсем нечего "ковырять под капотом".

Коллега посоветовал посоветовал как-то связку GitHub Pages + Jekyll.   
Я решил раскурить эту тему.   
Jekyll это инструмент для генерации статических web-страничек.   
Можно написать текст, используя язык разметки маркдаун, добавить картинки, а Jekyll сгенерирует из этого веб-страничку.   
Далее всё это можно прикрутить к GitHub Pages.   
А через GitHub Actions автоматизировать публикацию этих готовых страничек в интернете.   
Пока читал про это всё, мне показалось, что для этих нужд лучше подходит не Jekyll, а другой иснтумент - Hugo.   
Логика точно такая же, готовишь текст с использованием маркдаун, дальше генерация веб-странички, GitHub Actions, GitHub Pages.   
Чем вся эта конструкция хороша?   
После того как один раз настроил все части этой системы, публикация постов делается "в одну кнопку", через git push.   
Не нужно думать о хостинге, гитхаб стабилен и он безопасный.   
Сами статьи хранятся в репозитории и на локальном компьютере.   
Присутствует версионность.   
Один словом, есть все прелести гита.

Когда первый раз об этом читал, мне показалось, что GitHub Pages предоставляет возможность вести блог только в своей доменной зоне.   
Первоначально блог начинает публиковаться по адресу: "имя_пользователя".github.io.   
Но потом я нашел в GitHub Pages возможность подключения своего домена.   
И это пожалуй заняло самую большую часть времени, из всей настройки нового окружения блога.   
DNS записи упорно не хотели прописываться, но многократным гуглением и ютублением я победил этот вопрос:)

Наиболее качественный мануал по настройке этого окружения нашел тут: https://owlpaw.com/blog/hugo-simple-blog/   
Не всё идеально и не взлетит если сделать полностью по мануалу, но это самый точный мануал:)

Для обсуждения приглашаю в Telegram канал https://t.me/aullblog


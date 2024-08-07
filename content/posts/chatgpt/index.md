---
title: "Опыт использования ChatGPT."
date: 2023-12-14T11:30:03+00:00
tags: ["ChatGPT", "Блог"]
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
searchHidden: false
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

![chatgpt](/chatgpt.jpg 'chatgpt')

## Задание для ChatGPT.

Привет!   
Давай напишем статью для моего блога, об опыте использования ChatGPT.   
В статье должны быть отсылки к моей статье: https://aull.me/index.php/deutsch-lernen/

Я расскажу тебе свой опыт, а ты оставишь об этом интересную статью.   
Можешь задать мне 10 уточняющих вопросов.

Мой опыт:
Я скептически относился к хайпу вокруг генеративных ИИ, даже ни разу не пробовал ни одного сервиса ИИ.   
Но тут посмотрел на YouTube видео урок как использовать ChatGPT а изучении языков.   
Меня захватила эта тема, так как у меня нет возможности нанять репетитора по языку или сходить в клубы общения на изучаемом языке, их нет в моем городе, онлайн репетитор, кажется совсем дорогой затеей.   
А вот воспользоваться онлайн помощником, который может генерировать задания, проверять грамматику, показалось удачной идеей.   
К тому же версия 3.5 бесплатная.   
За версией 4, нужно постоять в очереди и платить 20$ в месяц.

И я должен сказать, что меня захватила эта тема)   
С ChatGPT реально интересно общаться.   
А в приложении на телефоне с ChatGPT можно общаться голосом, это вообще показалось волшебством, после туповатых Siri и Google помощника в телефоне.

Очень мне понравилось обсуждать код на Python.   
Я давал ChatGPT функцию из реально написанной мной программы и просил оптимизировать функцию.   
Он выдавал очень приличный результат.   
Я указывал на какие-то моменты и он перерабатывал код и выдавал новую версию.

Потом я попросил написать программу, которая бы брала входной текст, забирала из него уникальные буквы, а потом из этих букв составляла всевозможные слова на русском, но чтобы эти слова были реальными.   
Через 5-6 уточнений ChatGPT родил полностью рабочий скрипт.

Погонял его по немецким словам и предложениям.

Потом я прочитал что ChatGPT через api можно прикрутить к гугл таблицам.   
А у меня же там живёт словарь В1.   
И я решил улучшить качество перевода, добавить примеров предложений, объединить похожие по слыслу слова.   
Приделать предложениям нумерацию.   
Определить часть речи у каждого слова.   
Не без огрехов, но я всё это сделал за полторы недели.   
А как я рассказывал, в прошлый раз у меня это заняло несколько месяцев и кучу сеансов общения с моим дядей, который владеет немецким.

Вот такие промты у меня родились в результате общения с ботом через api:   
```
=GPT(“Welche Wortart ist das?”, B85)   
=GPT(“Составь пример предложения на немецком с использованием слова, без перевода на русский”, B65)   
=GPT(“Переведи с немецкого на русский, в том смысле в котором слово чаще всего используют немцы, если у слова несколько значений перечисли их”, B35)   
=GPT(“Переведи с немецкого на русский дословно, с сохранением порядка слов”, D2)
```

Помоги мне потренировать словарный запас.   
Присылай мне слова на немецком с предложением в котором оно используется.   
А я буду отвечать тебе переводом на русском.   
Будем пофторять это пока я не напишу слово ХВАТИТ.

```
=GPT(“Пронумеровать предложения по порядку начиная с 1”,C984)   
=GPT(“Составь два примера предложения на немецком уровня B1 с использованием слова, без перевода на русский”, A1307)
```

Иногда случаются у бота галлюцинации, типа если спросить “Перечисли фильмы про Джеймса Бонда с Крейгом” он выдает 4 фильма, без последнего.   
И если следом написать ему “А как же фильм Не время умирать?” Он расскажет про этот фильм и скажет что это пятый.   
И следом если задать опять вопрос про фильмы Бонда с Крейгом, то он перечислит все 5:)

Такая же история получилось с фильмами про Джейсона Борна.   
И с фильмами Уэса Андерсона.

Попробовал задать ему текстом математическую задачу с большим количеством переменных, кучей вычислений с процентами.   
И это был полный провал, он ошибался во всём)   
Проценты брал неправильно, вычисления были совсем странными.   
Я указывал на эти ошибки, но он исправлял ошибки только в одном месте и не мог увидеть, что в другим местах он так же ошибся.   
Потом коллега посоветовал не просить посчитать, а попросить дать формулы.   
Я так и сделал, он выдал вполне сносные формулы вычисления этой задачи.   
Я следом ему сказал, а теперь посчитай по этим формулам и парень опять сломался:)   
Попробую так же помучать версию 4 в будущем.

Штука классная и может помочь ускорить работу в куче разных сфер, но пока за ним нужен глаз да глаз)   
Ошибается везде, но можно добиться сносного результата.   
Нужно четко формулировать задачи и понимать что должно быть на выходе, иначе промахов не избежать.   
Если дать таблицу со словами, скажем 3 тысячи строк и попросить перевести на какой-то язык, то он где-то переведет, где-то переведет и допишет какую-то служебную информацию, где-то переведет с английского, подумав что это был английский.   
Где-то вообще не переведёт.

Я встал в очередь на 4 версию, видимо очень активно пользовался API, потому что мне предоставили этот доступ достаточно быстро.

Попробую с ним пообщаться в будущем)

## Ответ от ChatGPT.

ChatGPT   
Прекрасно, давайте приступим к созданию статьи. Я задам вам некоторые вопросы, чтобы уточнить детали и написать более информативный текст.

Каковы были ваши первые впечатления от ChatGPT, когда вы начали им пользоваться?   
Можете ли вы привести примеры, как ChatGPT помог вам в изучении немецкого языка? Например, какие задания он генерировал для вас?   
Вы упомянули, что использовали ChatGPT для оптимизации Python кода. Каковы были результаты этого процесса? Насколько улучшился ваш код?   
В какой степени использование ChatGPT сэкономило ваше время при работе над словарем В1 в Google Таблицах?   
Какие основные недостатки и ограничения ChatGPT вы заметили в процессе использования?   
Есть ли конкретные моменты, когда ChatGPT особенно вас удивил или разочаровал?   
Как вы оцениваете потенциал ChatGPT в обучении языкам по сравнению с традиционными методами, такими как репетиторы или языковые клубы?   
Какие функции или возможности ChatGPT вы бы хотели видеть в будущем?   
Могли бы вы поделиться, какие идеи или проекты вы планируете реализовать с помощью ChatGPT в дальнейшем?   
И наконец, как вы бы описали свой общий опыт использования ChatGPT другим пользователям, которые могут быть скептически настроены или новичками в этой области?   
Ваши ответы помогут мне создать более точное и информативное содержание для вашего блога.

User   
Я буду отвечать по очереди:   
Это было Вау!   
Я очень удивился как далеко шагнули технологии.   
В прошлый раз я общался с аналогом генеративного ИИ в 2001 году.   
Это был чат бот, который запоминал всё, что ему написали и общался этими фразами.   
У него был фаил с историей.   
И если с этим ботом пообщаются 3-5 адекватных друзей, то с ним становилосб вполне интересно общаться.   
Потом стали появляться целые форумы в интернете, в которых все предлагали свой заполненный файл с различными беседами.   
И c “начитанными” ботами было очень интересно пооьщаться.   

ChatGPT   
Спасибо за ваш ответ!   
Ваши воспоминания о впечатлениях от первого общения с генеративным ИИ и сравнение его с предыдущими опытами общения с чат-ботами в 2001 году очень ценны.   
Это показывает, насколько технологии развились за эти годы.

Теперь, пожалуйста, поделитесь своим опытом использования ChatGPT для изучения немецкого языка. Какие задания он для вас генерировал? Это поможет мне более полно описать ваш опыт в статье.

User   
Я написал команду:   
Помоги мне потренировать словарный запас.   
Присылай мне слова на немецком с предложением в котором оно используется.   
А я буду отвечать тебе переводом на русском.   
Будем пофторять это пока я не напишу слово ХВАТИТ.   
Несколько раз я решал эти задания.   

ChatGPT   
Отлично, это дает хорошее представление о том, как вы использовали ChatGPT для практики немецкого языка.   
Использование команды для получения немецких слов с примерами предложений и последующий их перевод на русский является эффективным способом тренировки языковых навыков.   
Такой подход позволяет не только улучшить словарный запас, но и практиковаться в переводе, что является важной частью изучения любого языка.

Теперь давайте перейдем к вашему опыту использования ChatGPT для оптимизации Python кода.   
Каковы были результаты этого процесса и насколько улучшился ваш код благодаря взаимодействию с ChatGPT?   
Это поможет мне осветить использование ИИ в программировании в вашей статье.

User   
Функции которые я давал для обработки боту, после обработки становились более компактными и читаемыми.   
В некоторых случаях бот добавлял обработку ошибок в циклах.   
Мне это понравилось, так как когда я сам пишу, я часто забываю добавить обработку ошибок и исключений.   

ChatGPT   
Ваш опыт с оптимизацией Python кода с помощью ChatGPT подчеркивает важность ИИ в облегчении и улучшении процесса программирования.   
Использование ChatGPT для создания более компактного, читаемого кода и добавления обработки ошибок — это отличный пример того, как ИИ может помочь даже опытным разработчикам улучшить свои навыки и процессы.

Далее, вы упомянули об использовании ChatGPT для работы с Google Таблицами и вашим словарем уровня В1.   
Как использование ChatGPT сэкономило ваше время при этом проекте?   
Было ли это более эффективным, чем предыдущие методы работы над словарем?   
Эта информация поможет мне осветить применение ChatGPT в управлении и обработке данных.

User   
Возьми эту информацию из того текста что я написал, мне нечего тут добавить.

ChatGPT   
Понял, вы использовали ChatGPT для улучшения качества перевода, добавления примеров предложений и объединения похожих по смыслу слов в вашем словаре В1 в Google Таблицах.   
Это значительно ускорило процесс, который ранее занимал несколько месяцев и требовал сеансов общения с вашим дядей, владеющим немецким.   
Использование ChatGPT позволило вам выполнить эту работу за полторы недели, что является значительным улучшением по сравнению с предыдущим опытом.

Переходим к следующему вопросу.   
Какие основные недостатки и ограничения ChatGPT вы заметили в процессе использования?   
Это поможет создать более сбалансированный взгляд на технологию в вашей статье.

User   
Я это так же описал в тексте, возьми это там.

ChatGPT   
Исходя из вашего предыдущего описания, основные недостатки и ограничения ChatGPT, которые вы заметили, включают случаи, когда он допускал ошибки в ответах или давал некорректную информацию.   
Например, в случае с фильмами про Джеймса Бонда и Джейсона Борна, где ChatGPT изначально неправильно перечислил количество фильмов.   
Также были проблемы с обработкой сложных математических задач, где ChatGPT не справлялся с вычислениями, хотя смог предоставить правильные формулы.   
Эти моменты подчеркивают, что, несмотря на его возможности, за работой ChatGPT все еще требуется внимательный контроль, особенно в задачах, требующих точности и специализированных знаний.

Далее, были ли моменты, когда ChatGPT особенно вас удивил или разочаровал?   
Это поможет подчеркнуть конкретные примеры в вашей статье, иллюстрирующие его потенциал и ограничения.

User   
Самое большое удивление конечно было связано с возможностью улучшения кода.   
Какого-то разочарования я не получил, так как у меня не было завышенных ожиданий.   

ChatGPT   
Ваше удивление, вызванное способностью ChatGPT улучшать код, подчеркивает его ценность как инструмента для программистов.   
Это отличный пример того, как искусственный интеллект может быть полезен в реальных рабочих сценариях, особенно в сфере программирования.   
Ваш подход без завышенных ожиданий также помог избежать разочарований, что важно при работе с новыми технологиями.

Далее, как вы оцениваете потенциал ChatGPT в обучении языкам по сравнению с традиционными методами, такими как репетиторы или языковые клубы?   
Это даст понимание о том, насколько эффективен ChatGPT может быть в качестве языкового помощника.

User   
Я думаю что у чатгпт огромный потенциал в изучении иностранных языков.   
Я не думаю, что бот заменитель традиционным способам изучения языков, это очень крутое дополнение к другим способам.   
Это возможность тренировки говорения, слушания, чтения, письма с возможность интересктивного взаимодействия.   
В услувиях когда недоступен преподаватель или носитель языка, это хорошая возможность получить моментальный отклик на выполненные задания.   

ChatGPT   
Ваше мнение о потенциале ChatGPT в изучении иностранных языков как о дополнении к традиционным методам обучения подчеркивает важность технологии в современном образовании.   
Вы правильно отметили, что, хотя ChatGPT не может полностью заменить преподавателя или носителя языка, он предлагает ценные возможности для тренировки говорения, слушания, чтения и письма.   
Особенно важным является его способность предоставлять моментальный отклик на выполненные задания, что особенно полезно в ситуациях, когда доступ к преподавателю или носителю языка ограничен.

Далее, какие функции или возможности ChatGPT вы бы хотели видеть в будущем?   
Это поможет раскрыть ваши ожидания и предпочтения относительно дальнейшего развития этой технологии.

User   
Пока мне нравится как развиватеся технология.   
Особых пожеланий у меня нет.   

ChatGPT   
Понятно, ваше удовлетворение текущим развитием технологии ChatGPT говорит о том, что она отвечает вашим потребностям и ожиданиям.   
Это важный момент для статьи, подчеркивающий, что инновации в области искусственного интеллекта уже приносят практическую пользу пользователям.

Теперь давайте обсудим ваши планы на будущее в отношении использования ChatGPT.   
Есть ли конкретные идеи или проекты, которые вы планируете реализовать с его помощью?   
Это поможет подчеркнуть потенциал применения ChatGPT в различных сферах.

User   
Я планирую использовать чатгпт для улучшения кода, для изучения языков, для поиска информация и просто для Fun’а.   

ChatGPT   
Отлично, ваши планы по использованию ChatGPT охватывают широкий спектр применений: от улучшения кода и изучения языков до поиска информации и развлечения.    
Это подчеркивает гибкость и многофункциональность ChatGPT как инструмента, способного адаптироваться к различным потребностям и интересам.

И, наконец, как бы вы описали свой общий опыт использования ChatGPT другим пользователям, особенно тем, кто может быть скептически настроен или является новичком в этой области?    
Ваше мнение поможет сформировать заключительный раздел статьи, предоставляя читателям реальную перспективу от опытного пользователя.

User   
Обязательно стоит попробовать и возможно вы найдете отличное применение для этой современной технологии.   

ChatGPT   
Ваш совет другим пользователям обязательно стоит попробовать ChatGPT и найти для него применение в соответствии со своими интересами и потребностями отлично подходит для заключения статьи.    
Это подчеркивает открытость к новым технологиям и возможность их применения в различных областях, от программирования до изучения языков и развлечений.

Исходя из вашего опыта и ответов, я подготовлю статью, в которой будет отражен ваш личный опыт использования ChatGPT, его возможности и ограничения, а также ваше видение его будущего развития и потенциала.    
Статья будет включать вашу историю перехода от скептицизма к признанию полезности этой технологии, ваш опыт использования ChatGPT в обучении языкам и программировании, а также ваше общее впечатление и рекомендации для других пользователей.

Если у вас есть какие-либо дополнительные комментарии или пожелания по содержанию статьи, пожалуйста, сообщите мне.

User   
Покажи что получилось, возможно у меня возникнут дополнительные пожелания.

ChatGPT   
Конечно, вот черновой вариант статьи, основанный на вашем опыте использования ChatGPT:

## Статья для блога от ChatGPT, версия 1.

### Название: Погружение в мир искусственного интеллекта: Мой опыт с ChatGPT

Вступление:   
В мире, где технологии развиваются с невероятной скоростью, искусственный интеллект (ИИ) занимает особое место.    
Недавно я решил исследовать этот удивительный мир, используя ChatGPT – инструмент, который оказался гораздо более мощным и полезным, чем я мог представить.

От скептицизма к признанию:   
Мой первый контакт с генеративными ИИ был еще в 2001 году, с чат-ботами, запоминающими и повторяющими фразы пользователей.    
В сравнении с ними, первое знакомство с ChatGPT было настоящим “вау-эффектом”. Я был поражен тем, как далеко за это время продвинулись технологии.

Использование в обучении языков:   
Одно из первых применений ChatGPT для меня стало изучение немецкого языка.    
Я использовал команду, чтобы получать немецкие слова с примерами предложений и переводил их на русский.    
Это был эффективный способ практики и расширения словарного запаса.

Программирование с ChatGPT:   
Другое важное применение нашлось в программировании.   
ChatGPT помог мне оптимизировать код, делая его более компактным и читаемым, а также добавлял обработку ошибок, на что я часто забывал.

Работа с данными:   
В проекте по улучшению словаря В1 в Google Таблицах, ChatGPT существенно сэкономил мое время.    
Ранее этот процесс занимал месяцы и требовал общения с носителем языка.    
С ChatGPT я справился за полторы недели.

Ограничения и недостатки:   
Несмотря на его эффективность, я столкнулся с некоторыми ограничениями ChatGPT, такими как ошибки в количестве фильмов о Джеймсе Бонде и Джейсоне Борне, а также трудности с обработкой сложных математических задач.

Заключение и рекомендации:   
ChatGPT открыл для меня новые горизонты в изучении языков, программировании и обработке данных.   
Я считаю его отличным дополнением к традиционным методам обучения и работы.   
Мой совет тем, кто еще не попробовал ChatGPT – обязательно попробуйте, и, возможно, вы найдете для этой современной технологии отличное применение.


Вот такая получилась переписка с ChatGPT-4:)

А ты пользуешься ИИ инструментами?

Для обсуждения приглашаю в Telegram канал https://t.me/aullblog



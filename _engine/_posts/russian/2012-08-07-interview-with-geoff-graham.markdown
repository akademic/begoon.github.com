---
layout: post
title: "Интервью с Джефом Грэхемом"
language: russian
date: 2012-08-07 17:00
comments: true
categories: 
- russian
- maximite
- interview
---
**Disclaimer**: Данная статья является переводом с английского. Я не
профессиональный переводчик, так что в тексте могут встречаться
небольшие неточности. Желающие всегда могут прочитать 
[оригинал интервью на английском][]. Предложения по улучшению перевода 
принимаются.

[оригинал интервью на английском]: /blog/english/2012/08/07/interview-with-geoff-graham/

- - -
 
Сегодня у меня в гостях Джеф Грэхем, создатель популярного
самодельного микрокомпьютера [Maximite][].  На данный момент мы
наблюдаем бум проектов, основанных на микроконтроллерах.  Мы все еще
называем их "микроконтроллерами" по привычке, но по сути они ими уже 
не являются.  Например, кристалл PIC32 компании Микрочип содержит в 
себе больше возможностей, чем в восьмидесятых мы имели в "полноценных" 
компьютерах типа Эппл 2 или Спектрум 48.

![](/images/blog/maximite/geoff-graham/interview/geoff-graham.jpg)

> Я занимался электроникой, мини-компьютерами и
Бейсиком долгое время.  Поэтому, когда я понял, что PIC32 может
работать с VGA-дисплеем и клавиатурой, самой собой получилось, что
я решил вспомнить молодость и воссоздать один их моих первых 
компьютеров.

[Maximite]: http://geoffg.net/maximite.html

- - -

Джеф создал Maximite на основе PIC32. Maximite является полностью 
законченным бытовым компьютером, оснащенным современными интерфейсами, 
такими как VGA, PS/2, SD, USB, а управляет всем этим -- Бейсик!  Вам 
это ничего не напоминает?  По мне, Maximite является превосходным 
инструментом для изучения микроэлектроники, в котором можно пощупать,
где и как железо соприкасается с программным обеспечением.

У нас есть возможность лично задать Джефу несколько вопросов.
Джеф живет в пригороде Кенсингтон города Перт в западной части
Австралии.  Перт весьма далеко расположен от других городов, но
благодаря интернету и FedEx'у, расстояния не кажутся такими уж и 
большими в наши дни, так что это не мешает Джефу в работе над его 
проектами.

**Здравствуйте, Джеф, спасибо за интервью.  Почему "Maximite"?
Как родилось это название?**

Изначально, когда проект начинался, я хотел назвать его "The
Mighty Mite", что значит что-то небольшое (mite) и одновременно
что-то "продвинутое" (mighty).  Когда проект готовился к публикации
в журнале "Silicon Chip", редакторы выяснили, что предложенное мной
имя уже зарегистрировано каким-то производителем продуктов, и 
предложили изменить его на Maximite.  На тот момент у меня не было
других идей, и мы приняли это имя.  Кроме того, имя стало похоже
на название взрывчатки в некотором роде, что тоже было неплохо.

**Maximite очень популярен.  Вы знаете, хотя бы примерно, сколько
их вообще сделано?  И как и когда вы вдруг поняли, что проект стал
хитом?**

Обычно я говорю, что их собрано тысячи, хотя если поточнее, 
где-то между тремя и четырьмя тысячами.  Около половины собраны 
энтузиастами самостоятельно, а другая половина с помощью готовых плат
от компаний, скопировавших разработку.

Я понял, что проект популярен, по статистике посещаемости моего сайта.
В первые дни после выхода статьи в журнале количество посетителей 
увеличилось в сто раз, и после этого постепенно закрепилось где-то на 
отметке в двадцать раз по сравнению с до Maximite'овскими временами.
Забавно, что в первой опубликованной статье не было ссылки на мой 
сайт, что говорило о том, что люди самостоятельно начинали гуглить 
после прочтения.

Начиная разрабатывать Maximite, я представлял компьютеры 
восьмидесятых, с которыми мне довелось поиграться в те времена.
Они были очень популярны в свое время до появления более современных
моделей, которые стали гораздо сложнее в конструкции и использовании.
Ниша простых и понятных компьютеров исчезла.

**Для Maximite вы спроектировали железо и написали софт, что весьма 
необычно в наши дни.  Программисты нечасто занимаются железками,
а инженеры-железячники -- программами. Лично вы кто больше: 
программист или железячник?**

Да, это одна из вещей, с которой я столкнулся с момента выхода
Maximite.  Люди часто смотрят на проект однобоко: либо они пытаются
изменить принципиальную схему без учета прошивки, либо наоборот.
Про себя могу сказать, что все-таки я программист, но с хорошим 
пониманием электроники.

Еще одна вещь, которую люди часто пытаются сделать с Maximite -- это
изменить его целостность как устройства, его взаимодействие с 
пользователем, но делаться это должно с учетом и железа и программного 
обеспечения.  Эти три составляющие важны все вместе, что
часто упускается из виду и программистами, и специалистами по
аппаратной части.

**Я лично был поражен, насколько целостным и законченным является 
проект Maximite. Вы разработали все: прототип, корпус, программное
обеспечение. Можно купить даже конструкторы для любителей.  В мире
любительских проектов люди часто не доводят их до законченной формы
из-за потери интереса.  Как вы справились с этой проблемой?**   

Изначально настрой все закончить был из-за желания опубликовать
проект в журнале Silicon Chip.  Большинство проектов в нем являются
законченными профессиональными продуктами, и мне пришлось следовать
стандартам.  Подобное внимание к деталям весьма необычно в наши дни,
и журналы часто не публикуют ни документации, ни модели корпуса, ни 
тем более красивой лицевой панели.

Мне понравился столь дисциплинированный подход конкретно этого
журнала.  У меня есть несколько проектов (например, из
неопубликованных) в полузаконченном состоянии, на которые у меня 
не хватает терпения довести все до ума.

**Джеф, вы занялись микроэлектроникой после выхода на пенсию.
Сколько времени, например, в день вы тратите на это хобби? Опять-таки,
чтобы довести проект Maximite до столь вылизанного состояния, видимо,
потребовалось ощутимое время.**

Да, я действительно потратил на проект много времени после выхода
на пенсию, но, что интересно, мне в некотором роде пришлось это 
сделать.  Я почувствовал, что в моей прошлой профессиональной
карьере мне не удалось реализовать скрытый во мне потенциал инженера,
а вот на пенсии этой реализовалось.

С Maximite все происходило волнообразно. Я работал по двенадцать 
часов в течении месяца, а потом практически ничего не делал несколько
недель.  Это здорово, что мне нравится работать над проектами вроде
этого, которые требуют много времени.  Я бы оценил трудозатраты на
Maximite как девять месяцев полноценной работы по восемь часов в 
день, сорок часов неделю.

**MMBasic. Я знаю, что вы пытались начала найти готовую версию
Бейсика для Maximite, но после нескольких неуспешных попыток
адаптировать некоторые готовые реализации, вы решили написать свою.
По какой лицензии распространяется MMBasic?  Есть ли планы
разработать библиотеку драйверов для аппаратуры Maximite, чтобы можно
было проще создавать альтернативные прошивки, например, RetroBSD
или Lua?**

Да, я начал Maximite в надежде найти открытую версию Бейсика в
интернете и использовать ее.  Но, увы, так и не нашел подходящей
доступной реализации. Везде были какие-то сложности.  В итоге, решил
написать все сам.

Сначала я выпустил свой вариант Бейсика, названного MMBasic, под
лицензией GPL GNU, но был неприятный эпизод, когда некая фирма просто 
удалила мое имя из авторских прав, выдав программу за свою. В довершение они даже изменили название Бейсика.  Я был вынужден создать
свою собственную лицензию, по которой код являет открытым, но не
может распространяться без моего согласия.

Это сработало, и сейчас несколько университетов и коммерческих 
организаций используют MMBasic по договоренности со мной на тему
вариантов использования кода.  Это намного лучше, чем разрешать кому
угодно анонимно скачивать исходные тексты, а потом видеть их в сети
под чужим именем и авторскими правами.

На данный момент у меня нет планов создавать драйвера для аппаратуры
Maximite.  Главной причиной тому является ограниченность объема
памяти PIC32 на сегодняшний день.  Одновременно для всех устройств
(VGA, клавиатура, USB и т.д.) просто нет места сделать полноценные
загружаемые драйвера.  Можно было бы использовать более мощный
микроконтроллер, но я хотел бы пока остаться с PIC32.  Для компьютеров
типа Raspberry Pi можно сделать загружаемые драйвера, но это требует
гораздо более развитой операционной системы, а мне хотелось бы сохранить Maximite простым.

**Немного о вашем профессиональном прошлом. Например, когда и как вы
первый раз взяли в руки паяльник?  Я знаю многих людей, которые были
б не против заняться электроникой, но для которых факт пайки выглядит 
очень трудной или даже невозможной задачей.  Чтобы вы посоветовали 
таким людям в качестве отправной точки?**

Не могу точно вспомнить, когда я впервые взял в руки паяльник, 
возможно мне было около двенадцати.  Может я не самый удачный
консультант в этом вопросе, но как мне кажется, все что нужно для 
пайки -- это недорогой паяльник и немного припоя.

Одна из хороших сторон увлечения электроникой, что это весьма дешевое
хобби.  Я бы посоветовал начать с чего-нибудь простого, например,
схемы бегущего огонька или добавления часов в Ардуино, попутно купив, 
непосредственно, паяльник.  Конечно, первый блин может выйти комом,
но это неважно, так как к проекту третьему вы будете чувствовать себя
почти профессионалом.

**Можете посоветовать какие-нибудь книги или веб-сайты для
начинающих, по которым можно сделать первые шаги в электронике?
И какой, например, уровень подготовки нужен для сборки или создания 
проекта типа Maximite?**

Я бы посоветовал начать с журналов, например Silicon Chip (Австралия), 
Elektor (Европа) и Nuts and Volts (США).  На все эти журналы можно 
подписаться и из-за границы.  Если вы полный новичок, то скорее всего
Nuts and Volts подойдет лучше всего.   Подписавшись на журнал, вы 
будете постоянно иметь поток свежих идей для проектов, и, возможно,
придумаете что-нибудь свое.  Так что подписаться однозначно стоит.

Уровень знаний для изготовления Maximite нужен не такой уж и большой, 
так как все уже готово.  Конечно, для создания подобного проекта с 
нуля безусловно требуется некоторый опыт.  У меня он был.
Изначально  я учился на инженера-электронщика, а затем тридцать лет 
работал в области системного программирования -- так что у меня были 
все необходимые знания.

**Сейчас существует множество веб-сайтов, на которых частные
разработчики железа могу продавать свои идеи и готовые проекты,
например, SparkFun.com. Интернет позволяет им за свое хобби получать
деньги. Как человек, чьи разработки активно продаются в интернете,
как вы считаете, возможно ли на подобных сайтах зарабатывать
на жизнь?**

Будет очень трудно заработать достаточное количество денег таким
образом.  Некоторым разработчикам, например, создателям Arduino,
это удалось, но большинству все-таки приходится иметь
постоянную работу еще где-то.  Отчасти проблема в том, что люди как я,
создающие сложные устройства и затем бесплатно их распространяющие,
не могут реально конкурировать.  И покупатели привыкли получать
результаты их труда по очень низким ценам.

**Расскажите немного лично о себе. Есть ли какие-то люди, например,
инженеры или программисты, у которых вам довелось или хотелось бы
поучиться?**

Если говорить о программистах, то для меня это Брайн Керниган,
который вместе с Деннисом Ритчи создал язык С и написал книгу
"The C Programming Language" в 1978 году. До сих пор эта книга
является прекрасным введением в С и стоит того, чтобы ее прочитать.
Когда я пишу статьи для журналов, я стараюсь писать в таком же простом
и понятном стиле.

Джим Роув, возможно, является инженером, оказавшим на меня
значительное влияние. Он писал статьи для журналов по электронике
в Австралии, когда я был подростком.  Спустя пятьдесят лет, он 
все еще продолжает этим заниматься, и его проекты и статьи всегда
грамотно спроектированы, и при этом просты и понятны.  Он еще один
человек, кому я стараюсь подражать.

**Кстати, что привело вас в мир компьютеров и электроники?
Каким был ваш первый компьютер, и на каком языки вы начали
программировать?**

Давайте попробуем сориентироваться во времени (мне сейчас 64).
Я помню, как появился Altair, и немногим позже компания, где я 
работал, стала дистрибутором Intel в Австралии.  Я учился на 
инженера-электронщика и свой первый компьютер спаял сам.  Он был на
процессоре Intel 8080 и имел 512 байт памяти.

Тогда Бейсик был, пожалуй, единственным языком программирования из-за
ограниченных аппаратных возможностей и небольшого объема памяти. 
Гораздо позже, когда появились жесткие диски, мы стали использовать
более сложные языки, и в свое время я программировал на большинстве
из них (Fortran, COBOL, PL/1, ассемблер, Pascal и т.д.)
 
Как я уже говорил, я занимался электроникой, мини-компьютерами и 
Бейсиком долгое время.  Поэтому, когда я понял, что PIC32 может
работать с VGA-дисплеем и клавиатурой, самой собой получилось, что
я решил вспомнить молодость и воссоздать один их моих первых компьютеров.

**Под конец, не могли бы вы рассказать немного о своих планах.
Будет ли новая версия Maximite, например, с Ethernet или WiFi?**

В сентябрьском выпуске журнала Silicon Chip будет опубликован
проект нового Maximite с поддержкой цветного дисплея.  Он будет
поддерживать восемь цветов на VGA-дисплее, синтезированный стерео
звук и иметь разъем, совместимый в Arduino, плюс все остальные 
возможности оригинального Maximite (USB, Бейсик и т.д.).  Данный 
проект занял  у меня прилично времени и сил, так что я после 
публикации хочу немного отдохнуть, прежде чем браться за что-то новое.

Вот пара эксклюзивных фотографий нового цветного Maximite.

![](/images/blog/maximite/geoff-graham/interview/maximite-colour.jpg)

![](/images/blog/maximite/geoff-graham/interview/maximite-colour-tv-keyboard.jpg)

**Спасибо, Джеф, за интервью и за проект Maximite. Очень ждем ваших 
новых разработок.**

**Лично я очень рад, что в последнее время люди стали понимать, что 
обучение компьютерам, это не  только Word и Excel, а также знания о 
том, как все это работает изнутри.  И такие проекты, как Raspberry Pi 
или Maximite очень  помогают новичкам понять, как работает "железо" 
компьютеров.**

&#9632;

*// Джеф Грэхем, Александр Дëмин*

*// Август 2012*

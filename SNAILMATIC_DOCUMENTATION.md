<p align="center">
  <img src="https://user-images.githubusercontent.com/71496296/152130484-be1f57fd-45cb-428f-9184-8d314024683b.png" />
</p>

## SnailMatic

1. [Установка](#1-установка)
2. [Требования для биндера и его запуск](#2-требования-для-биндера-и-его-запуск)
3. [Главное окно](#3-главное-окно)
4. [Редактор биндов](#4-редактор-биндов)
   - [Гайд по созданию биндов](https://github.com/GrezeeBal/SnailMaticDocs/blob/main/BINDS_CREATING_GUIDE.md)
5. [Переменные](#5-переменные)
   - [Гайд по функциональным переменным](https://github.com/GrezeeBal/SnailMaticDocs/blob/main/FUNCTIONAL_VARIABLES_GUIDE.md)
6. [Выбор цели (переменные $target...$)](#6-выбор-цели-переменные-target)
7. [Настройки биндера](#7-настройки-биндера)
8. [Шпаргалка (внутриигровой блокнот)](#8-шпаргалка-внутриигровой-блокнот)
9. [Конструктор HUD](#9-конструктор-hud)
10. [Остальные функции биндера](#10-остальные-функции-биндера)
    - [Горячие клавиши интерфейса](#101-горячие-клавиши)
    - [Перемещение скриншотов по папкам прямо из игры](#102-перемещение-скриншотов-по-папкам-из-игры)
    - [Создание временных переменных](#103-создание-временных-переменных)
    - [Функциональные диалоги](#104-функциональные-диалогиотправка-строк-бинда-по-отдельности)
    - [Установка напоминаний и ввод заданного текста спустя время](#105-установка-напоминаний-и-ввод-заданного-текста-спустя-время)
    - [Пауза, остановка, деактивация биндов](#106-пауза-остановка-и-деактивация-биндов)
    - [Сокращение команд, фраз, текста](#107-сокращение-команд-фраз-текста)
    - [Конвертер профилей](#108-конвертер-профилей-из-других-биндеров)
11. [Информация для разработчиков](#11-информация-для-разработчиков)
12. [Известные ошибки и их решения](#12-известные-ошибки-и-их-решения)

</br>

<!-- .........................УСТАНОВКА......................... -->
# 1. Установка

[Ручная установка](https://disk.yandex.ru/d/FfHdxTfRx52dJw) - .rar архив

- Все файлы из архива переместить в папку `moonloader`.
- Файл `port.luac` сконвертирует профили от ScriptPatrol для SnailMatic.
- Папка `lib` содержит все нужные для работы биндера библиотеки.

После успешного запуска биндера — создастся папка с настройками и профилями биндера по пути:

`C:\Users\user\Documents\GTA San Andreas User Files\SAMP`

</br>

<!-- .........................ТРЕБОВАНИЯ......................... -->
# 2. Требования для биндера и его запуск

## Требования

Для работы биндера требуется (*установить в папку с игрой*):

> [Moonloader 0.26.5+](https://www.blast.hk/threads/13305)

и библиотеки Moonloader (*установить в* `.../moonloader/lib`):

> [mimgui](https://www.blast.hk/threads/66959/#:~:text=github.com-,%D0%A1%D0%BA%D0%B0%D1%87%D0%B0%D1%82%D1%8C%20mimgui,-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0:%20%D0%BF%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D1%81%D1%82%D0%B8%D1%82%D1%8C%20%D0%BF%D0%B0%D0%BF%D0%BA%D1%83), [fa-icons](https://disk.yandex.ru/d/JlTZXDRostOp0g), [copas](https://disk.yandex.ru/d/-hnx59P2qRq-uQ), [socket](https://disk.yandex.ru/d/nJeIbYenuZQG3A)

*скачивать библиотеки отдельно не нужно, всё идет в архиве с биндером*

Биндер совместим с SA-MP 0.3.7 R1, R3, 0.3DL, CRMP и независим от SAMPFUNCS и CLEO.
Работает на лаунчерах, при условии, что на них можно устанавливать моды (в частности .lua)

## Запуск

При успешном запуске биндера ты увидишь всплывающее уведомление справа внизу экрана. Открыть биндер — `CTRL+Z` или по команде `/sm.open`.

![image](https://user-images.githubusercontent.com/71496296/152141257-71d2358e-3aaf-4633-ad66-3ab832b5a2b1.png)

В случае, если биндер не запустился/не работает — убедись, что SnailMatic был установлен правильно, а так же в твоей сборке не присутствует антистиллер от DarkP1xel (`!0AntiStealerByDarkP1xel32.ASI`).

Так же некоторые ошибки и их решения описаны здесь:
> 12. [Известные ошибки и их решения](#12-известные-ошибки-и-их-решения)

В ином случае обратись в [тех. поддержку (vk.com)](https://vk.me/scriptpatrol), приложив в сообщении файл `moonloader.log` ( `\GTA San Andreas\moonloader\moonloader.log` )

</br>

<!-- .........................ГЛАВНОЕ ОКНО......................... -->
# 3. Главное окно

![image](https://user-images.githubusercontent.com/71496296/152163956-392f3470-7df2-4c41-ac9d-6457dcf52dc8.png)

В главном окне происходит взаимодействие с биндами (не редактирование). Отсюда же можно выйти в меню к настройкам и другим функциям.

## Взаимодействие с биндами

### Панель инструментов

<img src="https://user-images.githubusercontent.com/71496296/152145836-7823ccbb-6ba2-4bbe-8419-ed04947858f0.png" width="700">

Кнопки (слева направо):

<pre><code><b>Добавить бинд</b>, CTRL+N
<b>Редактировать бинд</b>, CTRL+O/Enter
<b>Дублировать бинд</b>
<b>Удалить бинд</b>, Delete
<b>Добавить/убрать бинд из селектора</b>, CTRL+G
<b>Открыть окно отправки отдельных строк бинда</b>
<b>Запустить/остановить бинд</b>
<b>Переместить бинд назад</b>, CTRL+Стрелочки/Drag&Drop
<b>Переместить бинд вперёд</b>, CTRL+Стрелочки/Drag&Drop
<b>Выключить/включить бинд</b>, ПКМ по бинду
<b>Свернуть панель инструментов</b></code></pre>

### Быстрые действия

Помимо взаимодействия с биндами через панель инструментов - в интерфейсе существуют быстрые действия: горячие клавиши, Drag&Drop и панель быстрого доступа по наведению на бинд:

![gif](https://media.giphy.com/media/TRtH6Lfc628NSSEf9I/giphy.gif)

Несколько полезных функций:

<pre><code>
<b>ПКМ по бинду</b> - выключить бинд <em>(бинд не сможет активироваться никаким способом)</em>
<b>СКМ по бинду</b> - показать некоторую информацию о бинде
<b>Кнопка "Добавить бинд"</b> - При перемещении бинда на эту кнопку - бинд дублируется
<b>Кнопка "Добавить бинд"</b> - Если поле поиска не пустое - создается бинд с введенным названием
<b>ПКМ по папке</b> - открыть настройки папки
<b>Перенос папки с помощью Drag&Drop на бинд</b> - бинд переместится в эту папку
<b>ESC</b> - закрыть окно биндера
<b>CTRL+N и сразу же CTRL+Enter</b> - создать новый бинд и сразу открыть его
</code></pre>

</br>

<!-- .........................РЕДАКТОР БИНДОВ......................... -->
# 4. Редактор биндов

> [Подробный гайд по созданию биндов](https://github.com/GrezeeBal/SnailMaticDocs/blob/main/BINDS_CREATING_GUIDE.md)

Что такое бинд? — это набор команд (указаний) для биндера, которые он должен выполнить в определенной последовательности и с определенной задержкой, например, отправить текст на сервер, очистить чат, запустить другой бинд и т.д.

![image](https://user-images.githubusercontent.com/71496296/152163817-c67548ac-6310-4bb4-949f-3699f5bdfd8f.png)

## Редактор биндов визуально разделен на две секции: верхнюю и нижнюю

### Верхняя секция

![image](https://user-images.githubusercontent.com/71496296/152165221-13865c9c-a14f-49af-aadc-ee2601cf9aa9.png)

Верхняя подразумевает под собой все функции и пункты до секции «Сообщение, Задержка, Отправка».

*«Название»*

> название бинда

*«Условия»*

> установка условий активации бинда

*«Три иконки»*

> выбор варианта отображения нижней секции: «Построчно», «В виде блокнота».

</br>

*«Клавиша»*

> активация бинда по клавише/сочетанию клавиш. Биндер очень чувствителен к сочетанию клавиш, поэтому CTRL+ALT+Z и ALT+CTRL+Z могут активировать разные бинды. Так же активация по клавише ставит и убирает бинд с паузы.

*«Активация по тексту в чате»*

> активация бинда по появлению указанного текста в чате. При использовании регулярных выражений (например, как на скрине «<b>[Гг]</b>олова») следует включить <a href="https://www.blast.hk/threads/62661/">Lua Pattern</a> (галочка ниже). В ином случае эту галочку нужно держать выключенной.

*«Команда»*

> активация бинда по введению команды. В начале команды ставить слэши и другие знаки необязательно.

</br>

*«Требовать подтверждение активации»*

> при попытке активации по тексту в чате будет всплывать уведомление о подтверждении активации.

*«Включить Lua Pattern»*

> позволяет использовать регулярные выражения в активации по тексту в чате. При отсутствии регулярных выражений следует держать Lua Pattern выключенным.

*«Блокировать клавишу бинда»*

>блокирует клавишу активации бинда, не давая управлению игры реагировать и обрабатывать её.

</br>

### Нижняя секция

![image](https://user-images.githubusercontent.com/71496296/152166670-3f93449e-7986-4684-aa7e-076c781ad623.png)

Нижняя в свою очередь после «Сообщение, Задержка, Отправка»

*«Сообщение»*

> строка, в которой будет содержаться текст или функции, отправляемые биндом. Каждая строка в бинде это одна команда(указание) для биндера. Все строки выполняются в последовательности сверху вниз.

*«Задержка»*

> задержка перед отправкой следующей строки, указывается в миллисекундах. 1000 мсек = 1 сек.

*«Отправка»*

> метод отправки строки (список ниже)

### Методы отправки строки:

![image](https://user-images.githubusercontent.com/71496296/152166858-b90fb014-ddad-4efd-84c7-901de5dae544.png)

<details>
  <summary markdown="span">Отправить серверу</summary>
  
* Отправляет строку напрямую на сервер. Отправленный текст не будет виден для вашего клиента, а значит, что сторонние скрипты и плагины его не увидят (например, если была отправлена на сервер команда, которая активирует какой-то скрипт на вашем клиенте — ничего не произойдет, т.к клиент эту команду не увидит и не обработает). Так же данная отправка не использует чат клиента(F6) и не будет мешать при наборе текста.

</details>

<details>
  <summary markdown="span">Отправить клиенту SA-MP</summary>
  
* Отправляет строку на обработку клиенту SA-MP. Если «Отправить серверу» отправляет текст непосредственно напрямую на сервер, то обработка клиентом SA-MP сначала убедится, что текст или команда не присутствует на вашем клиенте (например команда скрипта или плагина), а уже потом отправит эту строку на сервер. В случае, если на клиенте присутствует отправленная биндером команда — она не отправится на сервер, а выполнит свою функцию, если это команда стороннего скрипта. Отправленное сообщение остается в памяти клиента и использует для этого чат(F6)

</details>

<details>
  <summary markdown="span">Написать в чат и закрыть его</summary>
  
* Отправляет текст из строки в инпутбокс чата(F6) и сразу же его закрывает. При открытии чата там будет заготовленный текст из строки.

</details>

<details>
  <summary markdown="span">Написать в чат</summary>
  
* Тоже самое, что и предыдущий вариант, но чат не будет закрываться.

</details>
  
<details>
  <summary markdown="span">В локальный чат</summary>
  
* Отправляет строку в чат, который видишь только ты.

</details>
  
<details>
  <summary markdown="span">В активное диалоговое окно</summary>
  
* Вписывает текст из строки в диалоговое окно, если такое открыто.

</details>

<details>
  <summary markdown="span">Скопировать в буфер обмена</summary>
  
* Копирует текст из строки, как CTRL+C.

</details>
  
<details>
  <summary markdown="span">В консоль SF и биндера</summary>
  
* Отправляет строку в консоль SAMPFUNCS (\~) и консоль биндера (CTRL+\~). При отсутствии SAMPFUNCS текст отправляется только в консоль биндера.

</details>

<details>
  <summary markdown="span">В уведомления</summary>
  
* Отправляет текст в виде уведомления биндера.

</details>
  
<details>
  <summary markdown="span">Без отправки</summary>
  
* Способ отправки строки, при которой строка не отправится, но её обработает биндер и выполнит функции, содержащиеся в этой строке (биндер обрабатывает все отправки). Эта отправка полезна, если в строке не содержится текст.

</details>

</br>

<!-- .........................ПЕРЕМЕННЫЕ......................... -->
# 5. Переменные

> [Полная инструкция по функциональным переменным](https://github.com/GrezeeBal/SnailMaticDocs/blob/main/FUNCTIONAL_VARIABLES_GUIDE.md)

> [Сборник дополнительных переменных, которых нет в стандартном наборе (vk.com)](https://vk.com/topic-142775990_39081706)

- Переменная (в SnailMatic) — маленький внутренний скрипт, который возвращает определенную функцию, текст.
- В стандартном наборе SnailMatic находится около 80-ти переменных.
- Система переменных в SnailMatic модульная. Каждый пользователь может добавить/создать/скачать себе в биндер новую переменную.
- В SnailMatic переменные двух типов: **обычные** и **функциональные**
  - **Обычные** (`$var$`): не принимают параметры, а работают по четко-заданному алгоритму.
    - Например, переменная `$time$` - вернет время в формате HH:MM:SS (`20:51:42`)

  - **Функциональные** (`@var(...)@`): работают по параметрам, задаваемыми самим пользователем, от которых зависит конечный результат переменных.
    - Параметрами в функциональных переменных выступают выражения, условия, порядковые номера, другие переменные из биндера.
    - Например, переменная `@nickrp($targetid$)@` - вернет RP ник выбранного игрока по его ID (`Vyacheslav_Kolotushkin` -> `Vyacheslav Kolotushkin`)

![image](https://user-images.githubusercontent.com/71496296/152506274-773e7ae6-1724-4b24-a506-5c4f7888ad6f.png)

Переменные от **ScriptPatrol Lua**, которые установлены в `moonloader/SP/variables/` в большинстве своем поддерживаются и **SnailMatic**, для этого переместите их в `Documents\GTA San Andreas User Files\SAMP\SnailMatic\variables`

</br>

<!-- .........................ВЫБОР ЦЕЛИ......................... -->
# 6. Выбор цели (переменные $target…$)

В биндере присутствует возможность взаимодействовать с определенным игроком через специальные переменные:

Для использования этих переменных нужно выбрать одну определенную цель (игрока), с которой нужно взаимодействовать (будь-то автовставка nick, ID цели или получение информации об этом игроке).

<pre><code><b>$targetcar$</b> - машина выбранного игрока
<b>$targetcolor$</b> - цвет ника выбранного игрока {RRGGBB}
<b>$targetid$</b> - ид выбранного игрока
<b>$targetname$</b> - имя выбранного игрока
<b>$targetsurname$</b> - фамилия выбранного игрока
<b>$targetnick$</b> - полный ник выбранного игрока</code></pre>

</br>

**В SnailMatic существует несколько различных способов выбора цели:**

## На расстоянии

Выбор цели при такой ситуации осуществляется с помощью сочетания клавиш и ввода ID'а как чит-код.

Для начала нужно нажать на определенное сочетание клавиш (по умолчанию `CTRL+P`).

*Меню биндера > Настройки*

![image](https://user-images.githubusercontent.com/71496296/152357350-c4bd85d5-8dff-414c-8bf9-1951fc09a394.png)

После нажатия этого комбо клавиш в левой части экрана появится подсказка, какой ID сейчас вводится и будет выбран.

![image](https://user-images.githubusercontent.com/71496296/152357423-7c63a139-18e9-4cd0-9df2-2279d3fc76f6.png)

Далее при помощи **цифр над QWERTY** нужно ввести как чит-код ID нужного игрока и затем нажать на `Enter/NumEnter`

После ввода ID и нажатия Enter биндер захватит цель (игрока) и переменные $target…$ заработают.

![gif](https://media.giphy.com/media/eZpnJwdJhKDXEdFWN5/giphy.gif)

## С помощью нацеливания(`ПКМ`) на игрока

Для выбора цели таким способом нужно подойти к игроку и зажать ПКМ, чтобы над игроком появился зеленый треугольник. Дальше нужно нажать на клавишу выбора цели через ПКМ (по умолчанию `Е`)

![image](https://user-images.githubusercontent.com/71496296/152357698-d55a0d18-b361-4a19-80a3-16f4794687c0.png)

Либо, если включена галочка **«Без клавиши»** хватит лишь нажать ПКМ по игроку и биндер выберет его как цель.

![image](https://user-images.githubusercontent.com/71496296/152357732-0959ded2-8b9a-421e-9929-65fe118ea105.png)

![target_rmb](https://user-images.githubusercontent.com/71496296/152429926-7ba99d64-444b-40b8-945b-9d4cba34acc0.gif)

## С помощью команды в чат

<pre><code><b>/sm.target</b> [id/nick] - выбрать цель</code></pre>

## С помощью переменной

<pre><code>@targetset(id/nick)@</code></pre>

`@targetset($closestidtocenter$)@`:

https://user-images.githubusercontent.com/71496296/152427981-9e2a9ba2-1f29-4294-8be7-40b1ab1031fb.mp4

## С помощью предложения цели от биндера

При нажатии на сочетание клавиш выбора цели на расстоянии (по умолчанию `CTRL+P`) биндер может предложить самого ближайшего игрока как цель. При таком способе вводить ID вообще не нужно, достаточно лишь подтвердить это предложение нажатием `Enter/NumEnter`

![target_suggestion](https://user-images.githubusercontent.com/71496296/152428998-22b0b446-c618-4915-8e78-e7fa254739b8.gif)

</br>

<!-- .........................НАСТРОЙКИ БИНДЕРА......................... -->
# 7. Настройки биндера

![image](https://user-images.githubusercontent.com/71496296/152361955-ecde9176-64a3-43e0-9956-2f4d25c21514.png)

### Установка клавиш и автопрефикса

*«Открыть меню биндера»*

> открыть биндер клавишей

*«Селектор биндов»*

> открыть селектор биндов. Предварительно в него нужно добавить бинды с помощью кнопки на панели инструментов или CTRL+G.

*«Выбор цели»*

> выбор цели для переменных $target…$. При нажатии этой клавиши слева экрана появится подсказка о том, какой ID введён. Вводить ID нужно с помощью цифр как чит-код и после нажать Enter, чтобы подтвердить выбор.

«Выбор цели через ПКМ»

> выбор цели для переменных $target…$ путём нацеливания на игрока и нажатия установленной клавиши. При включенной галочке «Без клавиши» достаточно только лишь нацелиться на игрока.

«Автопрефикс перед введенным текстом»

> текст, который всегда будет подставляться перед введенным текстом, например автоакцент. Автопрефикс не будет срабатывать на знаки ( , . / ! @ ? и т.д).

</br>

### Уведомления

*«Push-уведомления вместо уведомлений в чат»*

> заменяет все уведомления биндера в чат на всплывающие уведомления справа внизу экрана.

*«Звук при уведомлении»*

> воспроизводит звук при появлении уведомления от биндера

*«Беспалевный режим»*

> режим, при котором все уведомления биндера убираются в консоль SAMPFUNCS (\~) и консоль биндера (CTRL+\~). При отсутствии SAMPFUNCS уведомления убираются только в консоль биндера.

</br>

### Система профилей

![image](https://user-images.githubusercontent.com/71496296/152680047-a90af398-238c-4b51-b6b0-cb6672f6a329.png)

При клике на кнопку **«Добавить профиль»** добавляется профиль с указанным названием. С помощью ПКМ по созданному профилю ему можно изменить название или удалить его. 

Так же профили можно устанавливать от других пользователей. Сборник профилей [находится здесь (vk.com)](https://vk.com/topic-142775990_39480277)

Чтобы добавлять профили через проводник во время игры нужно - перезагружать биндер (`/sm.reload`). Профили находятся по адресу `C:\Users\user\Documents\GTA San Andreas User Files\SAMP\SnailMatic\profiles`

### Редактор отыгровки оружия

![image](https://user-images.githubusercontent.com/71496296/152430269-7e5a6523-13b4-4f7f-8130-81c1fbb466dd.png)

*«Оружие»*

> выбор оружия для редактирования отыгровки

*«Клавиша»*

> клавиша активации отыгровки оружия. Считается как полностью ручная активация и не зависит от других способов активации отыгровки оружия

*«Задержка перед отыгровкой»*

> задержка перед тем, как биндер отыграет оружие. Ставится в миллисекундах. 1000 мсек = 1 сек

</br>

*«Автоматическая отыгровка оружия»*

> биндер будет отыгрывать доставание/убирание оружия полностью автоматически, без флуда.

*«Полу-автоматическая отыгровка оружия»*

> автоматическая отыгровка оружия при прицеливании с помощью ПКМ.

</br>

### Сброс и удаление биндера

*«Сбросить настройки биндера»*

> сбрасывает настройки биндера

*«Сбросить текущий профиль»*

> удаляет все бинды в текущем профиле

*«Сбросить текущую сессию»*

> биндер сохраняет все функции, которые создаются на одну сессию игры (до закрытия игры) (на случай краша биндера). Эта кнопка будет сбрасывать эти функции.

*«Удалить биндер»*

> удалить snailmatic.luac через интерфейс.

*Исполняющий файл биндера*

> `«\GTA San Andreas\moonloader\snailmatic.luac»`

*Настройки и профили биндера*

> `C:\Users\user\Documents\GTA San Andreas User Files\SAMP\SnailMatic`

</br>

<!-- .........................ШПАРГАЛКА......................... -->
# 8. Шпаргалка (внутриигровой блокнот)

Представь Word-документ, но в реалиях SA-MP. Это и есть шпаргалка в биндере SnailMatic.

![image](https://user-images.githubusercontent.com/71496296/152431239-31ef21d1-070c-472e-89f8-090f8561abaf.png)

Из функций шпаргалка предлагает неограниченное создание файлов, размер текста, а так же форматирование текста:

![image](https://user-images.githubusercontent.com/71496296/152431266-cc3b8410-602f-4a20-b8f0-1d5fa3916621.png)

<pre><code>С помощью колортэгов в формате RGB (например, {FFFFFF} — белый цвет) можно устанавливать цвет тексту.
<b>#sameline</b> — переносит текст на предыдущую строку.
</code></pre>

> Обработка текста в шпаргалке происходит построчно, а значит, что каждая строка не зависит от другой и редактируется отдельно.
Если первая строка находится в левой части шпаргалки, а вторая строка в правой (флаг `#right`) — с помощью `#sameline` их можно соединить вместе и на одной строке будет два разных текста слева и справа. Эти два текста все равно будут считаться как отдельные строки и редактироваться отдельно.

<pre><code><b>#center</b> — переносит текст в строке в центр
<b>#right</b> — переносит текст в строке в право
<b>#font</b> — устанавливает для текста в одной строке размер шрифта (12, 14, 16, 18, 30)
<b>#iconICON</b> — рисует указанную иконку.
Названия иконок можно посмотреть в файле <em>\GTA San Andreas\moonloader\lib\fa-icons.lua</em>
Сами иконки можно посмотреть на <a href="https://fontawesome.com/v4.7/icons/">этом сайте</a>
</code></pre>

## Быстрый просмотр шпаргалки

С помощью команд:

<pre><code><b>«/sm.spur</b> [название шпаргалки] [текст]» — открыть/искать текст в указанной шпаргалке. Вписывать полное название шпаргалки необязательно.
«/> [текст]» — открыть/искать текст в активной шпаргалке.</code></pre>

— можно быстро открыть просмотр созданной шпаргалки.

![image](https://user-images.githubusercontent.com/71496296/152432476-c92b077b-463d-4192-9a12-31b9aa380d1b.png)

В этом же окне можно скопировать строку с помощью нажатия ЛКМ на неё, переключаться между шпаргалками и найти нужный текст с помощью кнопки поиска сверху окна. Так же это окно можно масштабировать.

</br>

<!-- .........................КОНСТРУКТОР HUD......................... -->
# 9. Конструктор HUD

Система, которая рендерит любой текст и переменные на экран.

![image](https://user-images.githubusercontent.com/71496296/152432562-7ec0e539-dfe6-4606-b78a-b50bb51dcd3a.png)

*«Показать/скрыть»*

> клавиша, по которой появляется и убирается HUD биндера

*«Фон»*

> установка цвета и прозрачности фона окна.

*«Закругление»*

> закругление границ окна

*«Расстояние от границ окна»*

> расстояние между текстом и границами окна по X и Y

*«Авторазмер»*

> при включенном авторазмере биндер сам будет подстраивать размер окна в реальном времени. При выключенном авторазмере размер окна можно редактировать вручную.

*Кнопка «Пресеты»*

> три готовых пресета на выбор.

В поле редактора вписывается любой текст и переменные, а биндер в реальном времени рисует и обрабатывает этот текст в указанном месте.

Имеет такие же флаги, как и в шпаргалке.

![image](https://user-images.githubusercontent.com/71496296/152433076-fcf2020a-c29f-49b2-a797-f55a4026c407.png)

<pre><code>С помощью колортэгов в формате RGB (например, {FFFFFF} — белый цвет) можно устанавливать цвет тексту.
<b>#sameline</b> — переносит текст на предыдущую строку.
</code></pre>

> Обработка текста в HUD происходит построчно, а значит, что каждая строка не зависит от другой и редактируется отдельно.
Если первая строка находится в левой части шпаргалки, а вторая строка в правой (флаг `#right`) — с помощью `#sameline` их можно соединить вместе и на одной строке будет два разных текста слева и справа. Эти два текста все равно будут считаться как отдельные строки и редактироваться отдельно.

<pre><code><b>#center</b> — переносит текст в строке в центр
<b>#right</b> — переносит текст в строке в право
<b>#font</b> — устанавливает для текста в одной строке размер шрифта (12, 14, 16, 18, 30)
<b>#iconICON</b> — рисует указанную иконку.
Названия иконок можно посмотреть в файле <em>\GTA San Andreas\moonloader\lib\fa-icons.lua</em>
Сами иконки можно посмотреть на <a href="https://fontawesome.com/v4.7/icons/">этом сайте</a>
</code></pre>

</br>

<!-- .........................ОСТАЛЬНЫЕ ФУНКЦИИ......................... -->
# 10. Остальные функции биндера

## 10.1. Горячие клавиши

Управление в интерфейсе биндера может осуществляться с помощью горячих клавиш. Посмотреть все доступные горячие клавиши можно в разделе «**Больше**» в меню биндера


## 10.2. Перемещение скриншотов по папкам из игры

С помощью команды можно перемещать созданные скриншоты через `F8` по папкам, которые будут создаваться в папке скриншотов SA-MP

<pre><code><b>«/sm.ss</b> [папка]* [номер скрина] [новое название скрина]» — перемещение (последнего)скриншота в указанную папку с указанным именем (по умолчанию перемещается с оригинальным названием).</code></pre>

\*если нужно переместить определенный скрин — вписывать полное название необязательно, хватит лишь номера скрина.

### Например

```
/smss Вылеченные
```

— переместит последний сделанный скрин в папку «Вылеченные». Если такой папки нет — создаст её и переместит туда последний сделанный скрин.

### Или, например

```
/smss Патруль 098
```

— переместит скрин под номером 098 в папку «Патруль»

### Или, например

```
/smss Патруль 098 Патруль-1
```

— переместит скрин под номером 098 в папку «Патруль» и изменит название этого скрина на «Патруль-1»

## 10.3. Создание временных переменных

> [Гайд по использованию этой команды (vk.com)](https://vk.com/@scriptpatrol-sozdaem-arifmeticheskuu-progressiu)

Временная переменная — переменная на одну сессию игры (до закрытия игры)

<pre><code>«/sm.regvar [название переменной]* [значение/текст]*» — установка простой переменной на одну сессию

«/sm.regvarwn [название переменной]* [значение/текст]*» — полный аналог /sm.regvar, но без уведомлений от биндера</code></pre>

Создание временных переменных полезно, если нужно записать какую-то информацию и быстро её использовать. Так же полезно для слияния двух и более переменных в одну переменную.

## 10.4. Функциональные диалоги/отправка строк бинда по отдельности

> [Небольшой гайд по созданию функциональных диалогов](https://github.com/GrezeeBal/SnailMaticDocs/blob/main/BINDS_CREATING_GUIDE.md#9-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D1%91%D0%BC-%D1%81%D0%B2%D0%BE%D0%B8-%D0%B4%D0%B8%D0%B0%D0%BB%D0%BE%D0%B3%D0%BE%D0%B2%D1%8B%D0%B5-%D0%BE%D0%BA%D0%BD%D0%B0)

![image](https://user-images.githubusercontent.com/71496296/152434057-5b6a4de1-74ac-4a87-a49e-e685f6dcba60.png)

С помощью данного окна можно отправлять строки бинда в любом порядке по отдельности, нажимая на них

Так же можно использовать для создания функциональных диалогов, которые будут активировать нужные бинды.

<pre><code>«/sm.select [номер бинда/имя бинда]* [папка]» — открыть окно выбора отдельных строк бинда по его номеру/названию. Имеет такие же параметры, как и переменные @bindstart/stop/pause()@.

Так же можно открыть через кнопку на панели инструментов в главном окне или через быструю панель при наведении на бинд.</code></pre>

## 10.5. Установка напоминаний и ввод заданного текста спустя время

<pre><code>«/sm.remind [сек/время]* (@/!)[текст]*» — отправка введенного текста на клиент SA-MP через кол-во [сек] или в назначенное [время] (HH:MM или HH:MM:SS)
Знак @ перед текстом отправит текст в уведомления биндера.
Знак ! перед текстом отправит текст в никуда, полезно для некоторых переменных ($chatclear$...)</code></pre>

С помощью данной функции можно устанавливать напоминания или дать указание биндеру ввести указанный текст спустя какое-то количество времени.

### Например

```
/sm.remind 21:22:35 @Сделать доклад
```

— биндер в `21:22:35` отправит в виде уведомления от биндера текст «Сделать доклад».

### Или, например

```
/smremind 600 /doklad
```

— биндер через 600 секунд (10 минут) напишет команду `/doklad`, которая, допустим, активирует бинд с докладом.

### Или, например

```
/smremind 20:35 /autogov
```

— биндер в `20:35` напишет команду `/autogov`, которая, допустим, активирует бинд с автоматическими подачами объявлений в `/gov`. Перед этим нужно, соответственно, создать такой бинд, вписать в него нужные сообщения и повесить на него команду активации `/autogov`

### Или, например

```
/smremind 1 !$chatclear$
```

— биндер через 1 секунду очистит чат, без отправления пустой строки.

> Функция `/sm.remind` устанавливается на одну сессию игры.

## 10.6. Пауза, остановка и деактивация биндов

### Остановка бинда через универсальную команду:

<pre><code>«/sm.stop [номер бинда/имя бинда] [папка]» — остановить запущенный бинд через универсальную команду по его номеру/названию. Если не вводить бинд — остановятся все запущенные бинды.

Расширенные параметры команды смотри ниже</code></pre>

### Остановка бинда с помощью переменной:

<pre><code>@bindstop(...)@ - остановить бинд с помощью переменной

Параметры переменной смотри ниже</code></pre>

### Остановка бинда через интерфейса биндера:

*Кнопка остановки бинда*

![image](https://user-images.githubusercontent.com/71496296/152435377-c9f700c6-7f17-4ecc-ac33-f14fcdc9ba6d.png)

### Деактивировать бинд через интерфейс биндера:

```
ПКМ по бинду - выключить бинд
```

> Если деактивировать бинд, его нельзя будет запустить никаким способом до того момента, пока его не включить

### Деактивировать бинд с помощью переменной:

<pre><code>@binddisable(...)@ - выключить бинд через переменную.

Параметры переменной смотри ниже</code></pre>

> Если деактивировать бинд, его нельзя будет запустить никаким способом до того момента, пока его не включить

### Активировать бинд через интерфейс биндера:

```
ПКМ по выключенному бинду - включить бинд
```

### Активировать бинд с помощью переменной:

<pre><code>@bindenable(...)@ - включить бинд через переменную.

Параметры переменной смотри ниже</code></pre>

### Пауза бинда через команду активации:

![image](https://user-images.githubusercontent.com/71496296/152435736-aab6d588-f715-487b-8009-9cb1e5536864.png)

### Пауза бинда через интерфейс биндера:

*Поставить на паузу*

![image](https://user-images.githubusercontent.com/71496296/152435819-ea93ee9c-88f0-404f-82d0-f2a46d5197fe.png)

*Снять с паузы*

![image](https://user-images.githubusercontent.com/71496296/152435833-5dbeb351-9cc5-4910-8e45-d50eaf59b8ca.png)

### Пауза бинда с помощью переменной:

<pre><code>@bindpause(...)@ - поставить бинд на паузу.
@bindunpause(...)@ - снять бинд с паузы.

Параметры переменной смотри ниже</code></pre>

### Параметры переменных и команд

> @bindstart/stop/pause/unpause/disable/enable(…)@ и /smbind, /smselect, /smstop:

<details>
  <summary markdown="span">Параметры</summary>
  
<pre><code>"10" "папка" - бинд строго с названием 10 и строго в папке "папка"

"10" папка - бинд строго с названием 10 и в первой попавшейся папке в имени которой встречается "папка"

имя папка - первый попавшийся бинд в имени которого встречается "имя" и в первой попавшейся папке в имени которой встречается "папка"

имя "папка" - первый попавшийся бинд в имени которого встречается "имя" и строго в папке "папка"

10 папка - бинд под порядковым номером 10 и в первой попавшейся папке с именем "папка"

10 "папка" - бинд под порядковым номером 10 и строго в папке "папка"

--*не указывая папку - по умолчанию бинд из первой папки
--например, @bindstart("10" "папка")@ или /sm.bind "10"</code></pre>

</details>

## 10.7. Сокращение команд, фраз, текста

> [Несколько примеров с использованием этого функционала](https://github.com/GrezeeBal/SnailMaticDocs/blob/main/BINDS_CREATING_GUIDE.md#4-%D1%81%D0%BE%D0%BA%D1%80%D0%B0%D1%89%D0%B0%D0%B5%D0%BC-%D1%84%D1%80%D0%B0%D0%B7%D1%83)

Бинды в SnailMatic можно активировать командами, которым необязательно содержать в начале себя слэши или какие-нибудь другие знаки. Таким образом через бинды можно сокращать нужные команды, фразы и текст.

![image](https://user-images.githubusercontent.com/71496296/152436517-bc90556d-1a58-499f-910f-a2e7ff24b009.png)

*Результат*

![inside](https://user-images.githubusercontent.com/71496296/152436682-afad5472-187c-4958-8240-2724536d82ee.gif)

## 10.8. Конвертер профилей из других биндеров

Чтобы быстро перейти из другого биндера на SnailMatic мы разработали свой собственный конвертор, который перенесет профиль из другого биндера в SnailMatic.

Скачать [конвертор профилей](https://disk.yandex.ru/d/thgyaUe9UdFfLA) (идет вместе с архивом биндера)
Данный файл нужно переместить в папку moonloader и запустить игру. После он сам сконвертирует все поддерживаемые профили (список ниже) и самоудалится.

После конвертации нужно переключиться на профиль в настройках биндера

```
### Для конвертации SP Lua
Профили должны находиться по пути:
папка с игрой*\moonloader\SP\profiles
```

```
### Для конвертации SP AHK
Пересохранить профиль по пути:
Documents\GTA San Andreas User Files\SAMP\ScriptPatrol.ini в 
"ScriptPatrol AHK.ini" с кодировкой ANSI(она же Windows1251, CP1251)
```

```
### Для конвертации Binder by Kvas
Профили должны находиться по пути:
документы\GTA San Andreas User Files\SAMP\SnailMatic\profiles
```

```
### Для конвертации Police Assistant
Профиль должен находиться по пути:
папка с игрой\moonloader\Police Assistant\bindlist.json
```
 
 </br>

<!-- .........................ИНФОРМАЦИЯ ДЛЯ РАЗРАБОТЧИКОВ......................... -->
# 11. Информация для разработчиков

SnailMatic экспортирует некоторые функции, которые вы можете использовать чтобы написать для него плагин или дополнить свой скрипт функционалом.

Для этого нужно его подключить через

```Lua
local sm = import("snailmatic.lua")
```

В переменной `sm` будут находиться такие функции:

```Lua
sm.version -- получает версию биндера
sm.updateVariable(name, value) -- обновляет значение переменной

sm.updateVariable('targetid', 1) -- обновит переменную targetid, задав ей новое значение
```

```Lua
sm.registerVariable(name, description, value) -- зарегистрировать новую обычную переменную
sm.registerFunctionalVariable(name, description, value, render) -- зарегистрировать новую функциональную переменную
```

— параметр `render` может быть строкой, тогда это превратится в подсказку к функциональной переменной.

И может быть функцией, которая рендерит имгуи окно, как пример:

```Lua
function()
  imgui.Button("ok")
end
```
Пример по регистрации новой функциональной переменной:

```Lua
registerFunctionalVariable('time+min', 'Текущее время + указанное время, MM:SS', function(param)
    local min, sec = param:match('(%d+):(%d+)')
    min, sec = tonumber(min), tonumber(sec)
    return os.date("%H:%M:%S", os.time() + (min*60) + sec)
end)
-- создаёт функциональную переменную, которая добавляет к текущему времени время указанное в параметре переменной в формате МИНУТЫ:СЕКУНДЫ
```


```Lua
result = sm.callVariable(name, ...) -- вызвать переменную, возвращается результат обработки.

id = sm.callVariable('targetid') -- получить ид текущей цели, обычная переменная
nick = sm.callVariable('nick', 1) -- получить ник по ид, функциональная переменная
```

```Lua
result = sm.convertString(str) -- обрабатывает строку с переменными

result = sm.convertString("hello, my name is $myname$") -- "hello, my name is Yarik"
```

```Lua
sm.print(...)
```

— у SM есть консоль, которая открывается на Ctrl+Ё(Ctrl+~) или командой /smconsole, выводит сообщение туда, сделано на случай если не установлен SAMPFUNCS.

 </br>

<!-- .........................ОШИБКИ И РЕШЕНИЯ......................... -->
# 12. Известные ошибки и их решения

## 1.

```
(error)    SnailMatic: [string "..."]:0: attempt to index a nil value
stack traceback:
    [string "..."]: in function <[string "..."]:0>
    [C]: in function 'wait'
    [string "..."]: in function <[string "..."]:0>
```

`Решение`: В настройках биндера с помощью ползунка "Режим хукинга" измени режим на любой другой. Описание режимов указаны в подсказке.

## 2.

```
(error)    SnailMatic: Ошибка #1. Перезагрузка
```

`Решение`: В настройках биндера с помощью ползунка "Режим хукинга" измени режим на любой другой. Описание режимов указаны в подсказке.

## 3.

```
(exception) SnailMatic: CJSON: Expected value but found T_END at character 1
(error) SnailMatic: [string "..."]:0: attempt to index a nil value
stack traceback:
    [string "..."]: in function 'loadSetting'
    [string "..."]: in function <[string "..."]:0>
(error) SnailMatic: Script died due to an error. (33B3215C)
```

`Решение`: Удали snailmatic.json по пути C:/Users/user/Documents/GTA San Andreas User Files/SAMP/`SnailMatic`

## 4.

```
(error)    SnailMatic: C:\GTA San Andreas\moonloader\lib\mimgui\imgui.lua:8: cannot load module 'C:\GTA San Andreas\moonloader\lib\mimgui\cimguidx9': Не найден указанный модуль.
    stack traceback:
        [C]: in function 'load'
        C:\GTA San Andreas\moonloader\lib\mimgui\imgui.lua:8: in main chunk
        [C]: in function 'require'
        C:\GTA San Andreas\moonloader\lib\mimgui\init.lua:7: in main chunk
        [C]: in function 'require'
        [string "..."]: in function <[string "..."]:0>
        C:\GTA San Andreas\moonloader\snailmatic.luac: in function <C:\GTA San Andreas\moonloader\snailmatic.luac:0>
        C:\GTA San Andreas\moonloader\snailmatic.luac: in function <C:\GTA San Andreas\moonloader\snailmatic.luac:0>
```

`Решение`: Установи Microsoft Visual C++ (желательно все пакеты).

## 5.

```
Игра при запуске крашится, если установлен SnailMatic
```

`Решение`: Установи с заменой [RakLua](https://www.blast.hk/threads/69433/) 2.1 в папку `…\moonloader\lib`.

`Если не поможет`: смени параметр `hookmode` на `0`(это автономный) или `3`(это sampfuncs) в файле C:/Users/user/Documents/GTA San Andreas User Files/SAMP/SnailMatic/`snailmatic.json`

## 6.

![image](https://user-images.githubusercontent.com/71496296/152438177-18c92fc2-548f-419f-bd77-4d29d0dcb906.png)

`Решение`: нет решения. Ошибка, возможно, возникает из-за старой видеокарты
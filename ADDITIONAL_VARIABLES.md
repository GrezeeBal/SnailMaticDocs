Обновлено 29.06.2025

## Дополнительные переменные для SnailMatic

В SnailMatic есть система, которая подгружает дополнительные пользовательские переменные без необходимости обновлять сам биндер.

В этом репозитории находится сборник переменных, которые не попали в стандартный набор. Сборник время от времени пополняется новыми переменными.

### Как установить новую переменную?

1. Скачай прикрепленный **.zip** архив с переменной
2. Перемести **.lua** файл из архива в папку _...\Документы\GTA San Andreas User Files\SAMP\SnailMatic\variables_
3. Перезагрузи биндер с помощью **/sm.reload**, если он был запущен

## Переменные

### [@nickru(...)@](https://github.com/GrezeeBal/SnailMaticDocs/files/8681685/nickru.zip)

Переводит указанный в параметре ник на русский язык по иду/нику

> @nickru(Yarik_Vodila)@ -> Ярик Водила

### [@addtime(...)@](https://github.com/GrezeeBal/SnailMaticDocs/files/14594187/addtime.zip)

Добавляет к текущему времени указанное кол-во времени в формате МИНУТЫ:СЕКУНДЫ и пишет это время

> @addtime(13:27)@ - добавит к текущему времени 13 минут и 27 секунд (00:55:21 > 01:08:48) и напишет это время

### [$cops...](https://github.com/GrezeeBal/SnailMaticDocs/files/8681411/cops.zip)

- `$copsid$` - пишет все иды полицейских рядом с тобой в радиусе 5 метров
- `$copsname$` - пишет все имена полицейских рядом с тобой в радиусе 5 метров
- `$copssurname$` - пишет все фамилии полицейских рядом с тобой в радиусе 5 метров
- `$copsnick$` - пишет все РП ники полицейских рядом с тобой в радиусе 5 метров

> При желании переменную можно переделать под себя: в строчках `--Скины полицейских` можно добавить или убрать иды скинов (не обязательно полицейских), на которых будет реагировать переменная. Так же можно изменить радиус с 5 метров на любой другой в строчках `local radius = 5`

### [$army...](https://github.com/GrezeeBal/SnailMaticDocs/files/8681483/army.zip)

- `$armyid$` - пишет все иды военнослужащих рядом с тобой в радиусе 5 метров
- `$armyname$` - пишет все имена военнослужащих рядом с тобой в радиусе 5 метров
- `$armysurname$` - пишет все фамилии военнослужащих рядом с тобой в радиусе 5 метров
- `$armynick$` - пишет все РП ники военнослужащих рядом с тобой в радиусе 5 метров

> При желании переменную можно переделать под себя: в строчках `--Скины армии` можно добавить или убрать иды скинов (не обязательно армии), на которых будет реагировать переменная. Так же можно изменить радиус с 5 метров на любой другой в строчках `local radius = 5`

### [$targetvehcolor$](https://github.com/GrezeeBal/SnailMaticDocs/files/8682168/vehColor.zip)

Пишет цвет автомобиля выбранного игрока [(таргета)](https://github.com/GrezeeBal/SnailMaticDocs/blob/main/SNAILMATIC_DOCUMENTATION.md#6-%D0%B2%D1%8B%D0%B1%D0%BE%D1%80-%D1%86%D0%B5%D0%BB%D0%B8-%D0%BF%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5-target) на русском языке в родительном падеже

> `$targetcar$` `$targetvehcolor$` цвета -> Bravura красного цвета

<!--  ### [@hudpos](https://github.com/GrezeeBal/SnailMaticDocs/files/9115915/hudpos.zip)

Автоматически прикрепляет виджет (HUD) биндера к одной из 9 позиций на экране. Автор - Maksimilian Avdeev aka g1id3on

Значения:
tl, tc, tr, cl, cc, cr, bl, bc, br.

Вставлять в начало кода HUD'а.

![Screenshot_1](https://user-images.githubusercontent.com/71496296/179097807-4127889c-20ba-4e4a-8412-12292bd8b782.png) -->

### [$mycarid$](https://github.com/GrezeeBal/SnailMaticDocs/files/10911298/mycarid.zip)

Пишет ид транспорта, в котором находится твой персонаж

### [damage.zip](https://github.com/GrezeeBal/SnailMaticDocs/files/12565949/damage.zip)

Включает в себя несколько переменных, которые подставляют вместо себя ник и ид игрока, который стрелял по тебе и/или по которому стрелял ты.

> Переменная требует наличия SampFuncs и библиотеки samp.lua

![damage.lua](https://github.com/GrezeeBal/SnailMaticDocs/assets/71496296/66b71288-cfce-491e-ab36-e92f12da1812)

### [@sub](https://github.com/GrezeeBal/SnailMaticDocs/files/14392830/sub.zip)

Обрезает текст с определенного до определенного символа

> @sub(string;startIndex;endIndex)@
> 
> @sub(Hello World!;1;5)@ // - Hello

### [@setweapon](https://github.com/user-attachments/files/16652815/setweapon.zip)

Дает твоему персонажу в руки указанное оружие, по его иду (если есть в инвентаре)

> @setweapon(24)@ - достанет дигл

### [@numberwithdots](https://github.com/user-attachments/files/20966582/numberswithdots.zip)

Разделяет тысячи, миллионы и т.д точками

> @numberwithdots(15000)@ -> 15.000
>
> @numberwithdots(5000000)@ -> 5.000.000
>
> @numberwithdots(@math(100*10))@ -> 1.000

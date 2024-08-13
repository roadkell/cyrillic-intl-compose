# Compose-таблица для кириллических алфавитов #

<p align="right">
<i>Every time a user is forced to switch input languages,</br>
God kills a kitten. Stop the slaughter!</i>
</p>

- [Что это](#что-это)
- [Как установить](#как-установить)
  - [Windows](#windows)
  - [Linux](#linux)
  - [Android](#android)
- [Как пользоваться](#как-пользоваться)
- [Зачем](#зачем)
- [Список комбинаций](#список-комбинаций)
- [Похожие проекты](#похожие-проекты)
- [Важное](#важное)
- [Лицензия](#лицензия)

## Что это ##

[Compose](https://ru.wikipedia.org/wiki/Compose) — это метод ввода символов, отсутствующих на клавиатуре, с помощью комбинаций. Например, нажав клавишу <kbd>⎄ Сompose</kbd>, а затем <kbd>a</kbd> и <kbd>e</kbd>, можно ввести лигатуру **æ**. Клавишу <kbd>⎄ Compose</kbd> можно назначить на <kbd>Caps Lock</kbd> или на правый <kbd>Alt</kbd>, как вам удобнее. В Linux поддержка compose-ввода есть изначально, а в Windows — с помощью программы [WinCompose](https://github.com/samhocevar/wincompose).

Стандартные комбинации в Linux и WinCompose охватывают преимущественно латиницу и греческий, с небольшим количеством кириллицы, эмодзи, математических и специальных символов. Данный проект значительно расширяет список поддерживаемых кириллических букв.

Подробнее про этот способ ввода можно прочитать в Википедии ([Ру](https://ru.wikipedia.org/wiki/Compose) / [En](https://en.wikipedia.org/wiki/Compose_key)). Там же есть и список стандартных комбинаций (длинное тире, типографские кавычки, символы валют, диакритические знаки, математические символы и т.д.)

Если что-то будет непонятно или не заработает как надо, [спрашивайте](https://github.com/roadkell/xcompose/discussions), будем рады вам помочь. Так же будем рады предложениям и пожеланиям по проекту.

## Как установить ##

### Windows ###

1. Установить [WinCompose](https://github.com/samhocevar/wincompose)
2. Скачать файл [`dotXCompose`](/dotXCompose)
3. Сохранить его в папке пользовательского профиля (обычно это `C:\Users\имя_пользователя\`) под именем `.XCompose`
4. Перезапустить WinCompose
5. Если нужно, переназначить compose-клавишу в настройках приложения (по умолчанию это <kbd>правый Alt</kbd>)

### Linux ###

1. Скачать файл [`dotXCompose`](/dotXCompose)
2. Сохранить его в домашней папке пользователя (обычно это `/home/имя_пользователя/`) под именем `.XCompose` (включите показ скрытых файлов); если у вас уже установлен собственный `.XCompose`-файл, добавьте к нему содержимое скачанного файла
3. Выбрать и назначить compose-клавишу (например, в GNOME это `Настройки → Клавиатура → Ввод специальных символов → Compose Key`, по умолчанию это <kbd>Shift</kbd> + <kbd>правый Alt</kbd>)
4. Перезапустить приложение, в котором вы набираете текст

### Android ###

1. Установить [AnySoftKeyboard](https://anysoftkeyboard.github.io/) ([Google Play](https://play.google.com/store/apps/details?id=com.menny.android.anysoftkeyboard), [F-Droid](https://f-droid.org/en/packages/com.menny.android.anysoftkeyboard/))
2. Установить русскую раскладку к ней ([Google Play](https://play.google.com/store/apps/details?id=com.anysoftkeyboard.languagepack.russian2), [F-Droid](https://f-droid.org/packages/com.anysoftkeyboard.languagepack.russian2/))
3. Зайти в `Настройки → Язык и ввод → AnySoftKeyboard → Языки раскладок` и выбрать `Русский`
4. В настройках клавиатуры включить раскладку `Кириллица (Кириллические символы при длительном нажатии)`

## Как пользоваться ##

Буквы с диакритическими знаками вводятся по схеме <kbd>⎄ Compose</kbd> <kbd>знак</kbd> <kbd>буква</kbd>. Можно и наоборот: <kbd>⎄ Compose</kbd> <kbd>буква</kbd> <kbd>знак</kbd>. Например чтобы ввести букву **ѓ**, нужно набрать <kbd>⎄ Compose</kbd> <kbd>´</kbd> <kbd>г</kbd> (т.е. если клавиша <kbd>⎄ Compose</kbd> назначена на <kbd>правый Alt</kbd>, то комбинация будет выглядеть как <kbd>правый Alt</kbd> <kbd>г</kbd> <kbd>´</kbd>).

Поскольку многих "правильных" типографских диакритиков (умлаута <kbd>¨</kbd>, гачека <kbd>ˇ</kbd>, макрона <kbd>¯</kbd> и др.) на клавиатуре нет, вместо них используются обычные ASCII-символы:

| Диакритический знак                    | Символ на клавиатуре              | Пример комбинации                               | Результат |
| -------------------------------------- | --------------------------------- | ----------------------------------------------- | --------- |
| акут <kbd>´</kbd>                      | апостроф <kbd>'</kbd>             | <kbd>⎄ Compose</kbd> <kbd>к</kbd> <kbd>'</kbd>  | ќ         |
| двойной акут <kbd>˝</kbd>              | равенство <kbd>=</kbd>            | <kbd>⎄ Compose</kbd> <kbd>у</kbd> <kbd>=</kbd>  | ӳ         |
| гравис <kbd>\`</kbd>                   | обратный апостроф <kbd>\`</kbd>   | <kbd>⎄ Compose</kbd> <kbd>е</kbd> <kbd>`</kbd>  | ѐ         |
| умлаут <kbd>¨</kbd>                    | кавычки <kbd>"</kbd>              | <kbd>⎄ Compose</kbd> <kbd>и</kbd> <kbd>"</kbd>  | ӥ         |
| макрон <kbd>¯</kbd>                    | подчёркивание <kbd>_</kbd>        | <kbd>⎄ Compose</kbd> <kbd>у</kbd> <kbd>_</kbd>  | ӯ         |
| гачек <kbd>ˇ</kbd>                     | меньше <kbd><</kbd>               | <kbd>⎄ Compose</kbd> <kbd><</kbd> <kbd>р</kbd>  | р̌         |
| кратка <kbd>˘</kbd>                    | скобка <kbd>(</kbd>               | <kbd>⎄ Compose</kbd> <kbd>ж</kbd> <kbd>(</kbd>  | ӂ         |
| седиль <kbd>¸</kbd> (или нижний вынос) | запятая <kbd>,</kbd>              | <kbd>⎄ Compose</kbd> <kbd>х</kbd> <kbd>,</kbd>  | ҳ         |
| нижний вынос слева                     | запятая перед буквой <kbd>,</kbd> | <kbd>⎄ Compose</kbd> <kbd>,</kbd> <kbd>ч</kbd>  | ӌ         |
| хвостик <kbd>ˏ</kbd>                   | точка с запятой <kbd>;</kbd>      | <kbd>⎄ Compose</kbd> <kbd>м</kbd> <kbd>;</kbd>  | ӎ         |
| горизонтальный штрих                   | дефис <kbd>-</kbd>                | <kbd>⎄ Compose</kbd> <kbd>о</kbd> <kbd>-</kbd>  | ө         |
| вертикальный штрих                     | <kbd>1</kbd>                      | <kbd>⎄ Compose</kbd> <kbd>1</kbd> <kbd>ч</kbd>  | ҹ         |
| диагональный штрих                     | обратный слэш <kbd>\\</kbd>       | <kbd>⎄ Compose</kbd> <kbd>р</kbd> <kbd>\\</kbd> | ҏ         |
| штрих сверху слева                     | <kbd>7</kbd> перед буквой         | <kbd>⎄ Compose</kbd> <kbd>7</kbd> <kbd>к</kbd>  | ҡ         |
| крюк <kbd> ̡</kbd>                      | <kbd>9</kbd>                      | <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>9</kbd>  | ԓ         |
| крюк слева                             | <kbd>9</kbd> перед буквой         | <kbd>⎄ Compose</kbd> <kbd>9</kbd> <kbd>н</kbd>  | ԩ         |
| крюк посередине                        | <kbd>5</kbd>                      | <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>5</kbd>  | ҕ         |

Если буква имеет уникальное начертание, её можно получить, набрав похожую букву дважды:

| Ввод                                           | Буква |
| ---------------------------------------------- | ----- |
| <kbd>⎄ Compose</kbd> <kbd>е</kbd> <kbd>е</kbd> | ә     |
| <kbd>⎄ Compose</kbd> <kbd>у</kbd> <kbd>у</kbd> | ү     |
| <kbd>⎄ Compose</kbd> <kbd>ч</kbd> <kbd>ч</kbd> | һ     |

Или соединив с цифрой с похожим начертанием:

| Ввод                                           | Буква |
| ---------------------------------------------- | ----- |
| <kbd>⎄ Compose</kbd> <kbd>с</kbd> <kbd>5</kbd> | ѕ     |
| <kbd>⎄ Compose</kbd> <kbd>з</kbd> <kbd>3</kbd> | ӡ     |

Некоторые буквы кириллицы похожи на латинские. Их можно ввести, дважды нажав клавишу с похожей латинской буквой (в раскладке QWERTY/ЙЦУКЕН):

| Ввод                                           | Буква |
| ---------------------------------------------- | ----- |
| <kbd>⎄ Compose</kbd> <kbd>р</kbd> <kbd>р</kbd> | һ     |
| <kbd>⎄ Compose</kbd> <kbd>ш</kbd> <kbd>ш</kbd> | і     |
| <kbd>⎄ Compose</kbd> <kbd>н</kbd> <kbd>н</kbd> | ү     |

С лигатурами всё просто:

| Ввод                                           | Буква |
| ---------------------------------------------- | ----- |
| <kbd>⎄ Compose</kbd> <kbd>а</kbd> <kbd>е</kbd> | ӕ     |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>ь</kbd> | љ     |
| <kbd>⎄ Compose</kbd> <kbd>ъ</kbd> <kbd>к</kbd> | ҡ     |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>н</kbd> | ԩ     |

(Строго говоря, **ҡ** и **ԩ** — не лигатуры, но так проще запомнить).

Мультиграфы с палочкой (буква **Ӏ** в алфавитах кавказских языков) можно ввести, набрав букву и единицу:

| Ввод                                                        | Буква |
| ----------------------------------------------------------- | ----- |
| <kbd>⎄ Compose</kbd> <kbd>а</kbd> <kbd>1</kbd>              | аӏ    |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>ъ</kbd> <kbd>1</kbd> | гъӏ   |

Знаки валют — это буква и знак равенства (иногда подчёркивания):

| Ввод                                           | Буква |
| ---------------------------------------------- | ----- |
| <kbd>⎄ Compose</kbd> <kbd>р</kbd> <kbd>=</kbd> | ₽     |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>=</kbd> | ₴     |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>_</kbd> | ₸     |

Одинарный и двойной апострофы:

| Ввод                                                | Знак |
| --------------------------------------------------- | ---- |
| <kbd>⎄ Compose</kbd> <kbd>'</kbd> <kbd>пробел</kbd> | ʼ    |
| <kbd>⎄ Compose</kbd> <kbd>"</kbd> <kbd>пробел</kbd> | ˮ    |

## Зачем ##

Кириллица служит письменностью для [более чем сотни языков](https://ru.wikipedia.org/wiki/Алфавиты_на_основе_кириллицы), при этом собственная клавиатурная раскладка есть [всего у нескольких](https://learn.microsoft.com/en-us/globalization/windows-keyboard-layouts). Это значит, что на многих языках печатать крайне неудобно — надо копировать буквы из таблицы символов или запоминать номера в Юникоде и вводить через <kbd>Alt</kbd>+<kbd>NNNN</kbd>. И хотя диакритики для многих европейских языков доступны через [комбинации клавиш](https://support.microsoft.com/ru-ru/topic/вставка-букв-национальных-алфавитов-с-помощью-сочетаний-клавиш-108fa0c1-fb8e-4aae-9db1-d60407d13c35), кириллица и здесь оказалась за бортом технического прогресса.

В Linux ситуация чуть получше — там можно использовать [мёртвые клавиши](https://ru.wikipedia.org/wiki/Мёртвые_клавиши) и [compose-ввод](https://ru.wikipedia.org/wiki/Compose) без установки дополнительного софта. Но поддержка кириллицы там всё ещё скудная.

Этим проектом мы хотим изменить ситуацию — сделать кириллические алфавиты доступнее и помочь сохранению языкового наследия коренных народов.

## Список комбинаций ##

(...слегка устарел, сейчас их намного больше)
<details><summary>Развернуть</summary>

| Ввод                                                        | Буква |
| ----------------------------------------------------------- | ----- |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>г</kbd>              | ѕ     |
| <kbd>⎄ Compose</kbd> <kbd>с</kbd> <kbd>5</kbd>              | ѕ     |
| <kbd>⎄ Compose</kbd> <kbd>5</kbd> <kbd>с</kbd>              | ѕ     |
| <kbd>⎄ Compose</kbd> <kbd>е</kbd> <kbd>е</kbd>              | ә     |
| <kbd>⎄ Compose</kbd> <kbd>ё</kbd> <kbd>ё</kbd>              | ӛ     |
| <kbd>⎄ Compose</kbd> <kbd>з</kbd> <kbd>з</kbd>              | ԑ     |
| <kbd>⎄ Compose</kbd> <kbd>м</kbd> <kbd>м</kbd>              | ԝ     |
| <kbd>⎄ Compose</kbd> <kbd>у</kbd> <kbd>у</kbd>              | ү     |
| <kbd>⎄ Compose</kbd> <kbd>ц</kbd> <kbd>ц</kbd>              | џ     |
| <kbd>⎄ Compose</kbd> <kbd>ч</kbd> <kbd>ч</kbd>              | һ     |
| <kbd>⎄ Compose</kbd> <kbd>э</kbd> <kbd>э</kbd>              | є     |
| <kbd>⎄ Compose</kbd> <kbd>є</kbd> <kbd>є</kbd>              | э     |
| <kbd>⎄ Compose</kbd> <kbd>з</kbd> <kbd>3</kbd>              | ӡ     |
| <kbd>⎄ Compose</kbd> <kbd>3</kbd> <kbd>з</kbd>              | ӡ     |
| <kbd>⎄ Compose</kbd> <kbd>о</kbd> <kbd>о</kbd>              | ҩ     |
| <kbd>⎄ Compose</kbd> <kbd>с</kbd> <kbd>о</kbd>              | ҩ     |
| <kbd>⎄ Compose</kbd> <kbd>с</kbd> <kbd>0</kbd>              | ҩ     |
| <kbd>⎄ Compose</kbd> <kbd>0</kbd> <kbd>с</kbd>              | ҩ     |
| <kbd>⎄ Compose</kbd> <kbd>о</kbd> <kbd>0</kbd>              | ҩ     |
| <kbd>⎄ Compose</kbd> <kbd>0</kbd> <kbd>о</kbd>              | ҩ     |
| **Лигатуры**                                                |       |
| <kbd>⎄ Compose</kbd> <kbd>а</kbd> <kbd>е</kbd>              | ӕ     |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>ь</kbd>              | љ     |
| <kbd>⎄ Compose</kbd> <kbd>н</kbd> <kbd>г</kbd>              | ҥ     |
| <kbd>⎄ Compose</kbd> <kbd>н</kbd> <kbd>ь</kbd>              | њ     |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>ц</kbd>              | ҵ     |
| **Диграфы**                                                 |       |
| <kbd>⎄ Compose</kbd> <kbd>ь</kbd> <kbd>і</kbd>              | ы     |
| <kbd>⎄ Compose</kbd> <kbd>ъ</kbd> <kbd>і</kbd>              | ы     |
| <kbd>⎄ Compose</kbd> <kbd>ь</kbd> <kbd>\|</kbd>             | ы     |
| <kbd>⎄ Compose</kbd> <kbd>ъ</kbd> <kbd>\|</kbd>             | ы     |
| <kbd>⎄ Compose</kbd> <kbd>ь</kbd> <kbd>1</kbd>              | ы     |
| <kbd>⎄ Compose</kbd> <kbd>ъ</kbd> <kbd>1</kbd>              | ы     |
| <kbd>⎄ Compose</kbd> <kbd>¨</kbd> <kbd>ь</kbd> <kbd>і</kbd> | ӹ     |
| <kbd>⎄ Compose</kbd> <kbd>¨</kbd> <kbd>ъ</kbd> <kbd>і</kbd> | ӹ     |
| <kbd>⎄ Compose</kbd> <kbd>"</kbd> <kbd>ь</kbd> <kbd>і</kbd> | ӹ     |
| <kbd>⎄ Compose</kbd> <kbd>"</kbd> <kbd>ъ</kbd> <kbd>і</kbd> | ӹ     |
| <kbd>⎄ Compose</kbd> <kbd>а</kbd> <kbd>\|</kbd>             | аӀ    |
| <kbd>⎄ Compose</kbd> <kbd>а</kbd> <kbd>1</kbd>              | аӀ    |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>\|</kbd>             | гӀ    |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>1</kbd>              | гӀ    |
| <kbd>⎄ Compose</kbd> <kbd>к</kbd> <kbd>\|</kbd>             | кӀ    |
| <kbd>⎄ Compose</kbd> <kbd>к</kbd> <kbd>1</kbd>              | кӀ    |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>\|</kbd>             | лІ    |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>1</kbd>              | лІ    |
| <kbd>⎄ Compose</kbd> <kbd>о</kbd> <kbd>\|</kbd>             | оӀ    |
| <kbd>⎄ Compose</kbd> <kbd>о</kbd> <kbd>1</kbd>              | оӀ    |
| <kbd>⎄ Compose</kbd> <kbd>п</kbd> <kbd>\|</kbd>             | пӀ    |
| <kbd>⎄ Compose</kbd> <kbd>п</kbd> <kbd>1</kbd>              | пӀ    |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>\|</kbd>             | тӀ    |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>1</kbd>              | тӀ    |
| <kbd>⎄ Compose</kbd> <kbd>у</kbd> <kbd>\|</kbd>             | уӀ    |
| <kbd>⎄ Compose</kbd> <kbd>у</kbd> <kbd>1</kbd>              | уӀ    |
| <kbd>⎄ Compose</kbd> <kbd>ф</kbd> <kbd>\|</kbd>             | фӀ    |
| <kbd>⎄ Compose</kbd> <kbd>ф</kbd> <kbd>1</kbd>              | фӀ    |
| <kbd>⎄ Compose</kbd> <kbd>х</kbd> <kbd>\|</kbd>             | хӀ    |
| <kbd>⎄ Compose</kbd> <kbd>х</kbd> <kbd>1</kbd>              | хӀ    |
| <kbd>⎄ Compose</kbd> <kbd>ц</kbd> <kbd>\|</kbd>             | цӀ    |
| <kbd>⎄ Compose</kbd> <kbd>ц</kbd> <kbd>1</kbd>              | цӀ    |
| <kbd>⎄ Compose</kbd> <kbd>ч</kbd> <kbd>\|</kbd>             | чӀ    |
| <kbd>⎄ Compose</kbd> <kbd>ч</kbd> <kbd>1</kbd>              | чӀ    |
| <kbd>⎄ Compose</kbd> <kbd>ш</kbd> <kbd>\|</kbd>             | шІ    |
| <kbd>⎄ Compose</kbd> <kbd>ш</kbd> <kbd>1</kbd>              | шІ    |
| <kbd>⎄ Compose</kbd> <kbd>щ</kbd> <kbd>\|</kbd>             | щІ    |
| <kbd>⎄ Compose</kbd> <kbd>щ</kbd> <kbd>1</kbd>              | щІ    |
| <kbd>⎄ Compose</kbd> <kbd>ы</kbd> <kbd>\|</kbd>             | ыӀ    |
| <kbd>⎄ Compose</kbd> <kbd>ы</kbd> <kbd>1</kbd>              | ыӀ    |
| <kbd>⎄ Compose</kbd> <kbd>\|</kbd> <kbd>У</kbd>             | Іу    |
| <kbd>⎄ Compose</kbd> <kbd>1</kbd> <kbd>У</kbd>              | Іу    |
| <kbd>⎄ Compose</kbd> <kbd>\|</kbd> <kbd>у</kbd>             | Іу    |
| <kbd>⎄ Compose</kbd> <kbd>1</kbd> <kbd>у</kbd>              | Іу    |
| **Палочка**                                                 |       |
| <kbd>⎄ Compose</kbd> <kbd>˙</kbd> <kbd>і</kbd>              | Ӏ     |
| <kbd>⎄ Compose</kbd> <kbd>і</kbd> <kbd>˙</kbd>              | Ӏ     |
| <kbd>⎄ Compose</kbd> <kbd>.</kbd> <kbd>і</kbd>              | Ӏ     |
| <kbd>⎄ Compose</kbd> <kbd>і</kbd> <kbd>.</kbd>              | Ӏ     |
| <kbd>⎄ Compose</kbd> <kbd>ь</kbd> <kbd>ы</kbd>              | Ӏ     |
| <kbd>⎄ Compose</kbd> <kbd>ъ</kbd> <kbd>ы</kbd>              | Ӏ     |
| <kbd>⎄ Compose</kbd> <kbd>ы</kbd> <kbd>ь</kbd>              | Ӏ     |
| <kbd>⎄ Compose</kbd> <kbd>ы</kbd> <kbd>ъ</kbd>              | Ӏ     |
| **Кириллические і, ї, ј на основе и, й**                    |       |
| <kbd>⎄ Compose</kbd> <kbd>˙</kbd> <kbd>и</kbd>              | і     |
| <kbd>⎄ Compose</kbd> <kbd>и</kbd> <kbd>˙</kbd>              | і     |
| <kbd>⎄ Compose</kbd> <kbd>.</kbd> <kbd>и</kbd>              | і     |
| <kbd>⎄ Compose</kbd> <kbd>и</kbd> <kbd>.</kbd>              | і     |
| <kbd>⎄ Compose</kbd> <kbd>¨</kbd> <kbd>й</kbd>              | ї     |
| <kbd>⎄ Compose</kbd> <kbd>й</kbd> <kbd>¨</kbd>              | ї     |
| <kbd>⎄ Compose</kbd> <kbd>"</kbd> <kbd>й</kbd>              | ї     |
| <kbd>⎄ Compose</kbd> <kbd>й</kbd> <kbd>"</kbd>              | ї     |
| <kbd>⎄ Compose</kbd> <kbd>˙</kbd> <kbd>й</kbd>              | ј     |
| <kbd>⎄ Compose</kbd> <kbd>й</kbd> <kbd>˙</kbd>              | ј     |
| <kbd>⎄ Compose</kbd> <kbd>.</kbd> <kbd>й</kbd>              | ј     |
| <kbd>⎄ Compose</kbd> <kbd>й</kbd> <kbd>.</kbd>              | ј     |
| **Буквы с вертикальным штрихом**                            |       |
| <kbd>⎄ Compose</kbd> <kbd>\|</kbd> <kbd>к</kbd>             | ҝ     |
| <kbd>⎄ Compose</kbd> <kbd>1</kbd> <kbd>к</kbd>              | ҝ     |
| <kbd>⎄ Compose</kbd> <kbd>\|</kbd> <kbd>ч</kbd>             | ҹ     |
| <kbd>⎄ Compose</kbd> <kbd>1</kbd> <kbd>ч</kbd>              | ҹ     |
| **Буквы с горизонтальным штрихом**                          |       |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>о</kbd>              | ө     |
| <kbd>⎄ Compose</kbd> <kbd>о</kbd> <kbd>-</kbd>              | ө     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>г</kbd>              | ғ     |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>-</kbd>              | ғ     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>к</kbd>              | ҟ     |
| <kbd>⎄ Compose</kbd> <kbd>к</kbd> <kbd>-</kbd>              | ҟ     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>ү</kbd>              | ұ     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>у</kbd>              | ұ     |
| <kbd>⎄ Compose</kbd> <kbd>ү</kbd> <kbd>-</kbd>              | ұ     |
| <kbd>⎄ Compose</kbd> <kbd>у</kbd> <kbd>-</kbd>              | ұ     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>х</kbd>              | ӿ     |
| <kbd>⎄ Compose</kbd> <kbd>х</kbd> <kbd>-</kbd>              | ӿ     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>е</kbd>              | ҽ     |
| <kbd>⎄ Compose</kbd> <kbd>е</kbd> <kbd>-</kbd>              | ҽ     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>һ</kbd>              | ћ     |
| <kbd>⎄ Compose</kbd> <kbd>һ</kbd> <kbd>-</kbd>              | ћ     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>ч</kbd> <kbd>ч</kbd> | ћ     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>ь</kbd>              | ҍ     |
| <kbd>⎄ Compose</kbd> <kbd>ь</kbd> <kbd>-</kbd>              | ҍ     |
| **Буквы с диагональным штрихом**                            |       |
| <kbd>⎄ Compose</kbd> <kbd>к</kbd> <kbd>\\</kbd>             | ԟ     |
| <kbd>⎄ Compose</kbd> <kbd>\\</kbd> <kbd>к</kbd>             | ԟ     |
| <kbd>⎄ Compose</kbd> <kbd>р</kbd> <kbd>\\</kbd>             | ҏ     |
| <kbd>⎄ Compose</kbd> <kbd>\\</kbd> <kbd>р</kbd>             | ҏ     |
| **Буквы со штрихом сверху слева**                           |       |
| <kbd>⎄ Compose</kbd> <kbd>7</kbd> <kbd>ь</kbd>              | ъ     |
| <kbd>⎄ Compose</kbd> <kbd>7</kbd> <kbd>ъ</kbd>              | ь     |
| <kbd>⎄ Compose</kbd> <kbd>7</kbd> <kbd>к</kbd>              | ҡ     |
| <kbd>⎄ Compose</kbd> <kbd>7</kbd> <kbd>ы</kbd>              | ꙑ     |
| **Буквы с седилью**                                         |       |
| <kbd>⎄ Compose</kbd> <kbd>,</kbd> <kbd>з</kbd>              | ҙ     |
| <kbd>⎄ Compose</kbd> <kbd>з</kbd> <kbd>,</kbd>              | ҙ     |
| <kbd>⎄ Compose</kbd> <kbd>¸</kbd> <kbd>з</kbd>              | ҙ     |
| <kbd>⎄ Compose</kbd> <kbd>з</kbd> <kbd>¸</kbd>              | ҙ     |
| <kbd>⎄ Compose</kbd> <kbd>,</kbd> <kbd>с</kbd>              | ҫ     |
| <kbd>⎄ Compose</kbd> <kbd>с</kbd> <kbd>,</kbd>              | ҫ     |
| <kbd>⎄ Compose</kbd> <kbd>¸</kbd> <kbd>с</kbd>              | ҫ     |
| <kbd>⎄ Compose</kbd> <kbd>с</kbd> <kbd>¸</kbd>              | ҫ     |
| **Буква с подъёмом**                                        |       |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>'</kbd>              | ґ     |
| **Буквы с нижним выносным элементом**                       |       |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>с</kbd>              | ц     |
| <kbd>⎄ Compose</kbd> <kbd>ш</kbd> <kbd>,</kbd>              | щ     |
| <kbd>⎄ Compose</kbd> <kbd>ж</kbd> <kbd>,</kbd>              | җ     |
| <kbd>⎄ Compose</kbd> <kbd>к</kbd> <kbd>,</kbd>              | қ     |
| <kbd>⎄ Compose</kbd> <kbd>н</kbd> <kbd>,</kbd>              | ң     |
| <kbd>⎄ Compose</kbd> <kbd>х</kbd> <kbd>,</kbd>              | ҳ     |
| <kbd>⎄ Compose</kbd> <kbd>ч</kbd> <kbd>,</kbd>              | ҷ     |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>,</kbd>              | ӷ     |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>,</kbd>              | ԯ     |
| <kbd>⎄ Compose</kbd> <kbd>п</kbd> <kbd>,</kbd>              | ԥ     |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>,</kbd>              | ҭ     |
| <kbd>⎄ Compose</kbd> <kbd>һ</kbd> <kbd>,</kbd>              | ԧ     |
| <kbd>⎄ Compose</kbd> <kbd>'</kbd> <kbd>ч</kbd> <kbd>ч</kbd> | ԧ     |
| <kbd>⎄ Compose</kbd> <kbd>о</kbd> <kbd>,</kbd>              | ԛ     |
| **Буква с нижним выносом слева**                            |       |
| <kbd>⎄ Compose</kbd> <kbd>,</kbd> <kbd>ч</kbd>              | ӌ     |
| **Буквы с нижним выносом посередине**                       |       |
| <kbd>⎄ Compose</kbd> <kbd>,</kbd> <kbd>ц</kbd>              | џ     |
| <kbd>⎄ Compose</kbd> <kbd>ц</kbd> <kbd>,</kbd>              | џ     |
| <kbd>⎄ Compose</kbd> <kbd>е</kbd> <kbd>,</kbd>              | ҿ     |
| <kbd>⎄ Compose</kbd> <kbd>,</kbd> <kbd>е</kbd>              | ҿ     |
| **Буквы с крюком**                                          |       |
| <kbd>⎄ Compose</kbd> <kbd>і</kbd> <kbd>9</kbd>              | ј     |
| <kbd>⎄ Compose</kbd> <kbd>к</kbd> <kbd>5</kbd>              | ӄ     |
| <kbd>⎄ Compose</kbd> <kbd>к</kbd> <kbd>9</kbd>              | ӄ     |
| <kbd>⎄ Compose</kbd> <kbd>к</kbd> <kbd>ј</kbd>              | ӄ     |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>9</kbd>              | ԓ     |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>ј</kbd>              | ԓ     |
| <kbd>⎄ Compose</kbd> <kbd>н</kbd> <kbd>9</kbd>              | ӈ     |
| <kbd>⎄ Compose</kbd> <kbd>н</kbd> <kbd>ј</kbd>              | ӈ     |
| <kbd>⎄ Compose</kbd> <kbd>х</kbd> <kbd>9</kbd>              | ӽ     |
| <kbd>⎄ Compose</kbd> <kbd>х</kbd> <kbd>ј</kbd>              | ӽ     |
| <kbd>⎄ Compose</kbd> <kbd>ғ</kbd> <kbd>9</kbd>              | ӻ     |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>9</kbd>              | ӻ     |
| **Буквы с крюком посередине**                               |       |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>5</kbd>              | ҕ     |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>ј</kbd>              | ҕ     |
| <kbd>⎄ Compose</kbd> <kbd>п</kbd> <kbd>5</kbd>              | ҧ     |
| <kbd>⎄ Compose</kbd> <kbd>п</kbd> <kbd>ј</kbd>              | ҧ     |
| <kbd>⎄ Compose</kbd> <kbd>ћ</kbd> <kbd>5</kbd>              | ђ     |
| <kbd>⎄ Compose</kbd> <kbd>һ</kbd> <kbd>5</kbd>              | ђ     |
| <kbd>⎄ Compose</kbd> <kbd>һ</kbd> <kbd>ј</kbd>              | ђ     |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>5</kbd>              | ђ     |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>ј</kbd>              | ђ     |
| **Буквы с крюком слева**                                    |       |
| <kbd>⎄ Compose</kbd> <kbd>9</kbd> <kbd>н</kbd>              | ԩ     |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>н</kbd>              | ԩ     |
| <kbd>⎄ Compose</kbd> <kbd>ј</kbd> <kbd>н</kbd>              | ԩ     |
| **Буквы с хвостиком**                                       |       |
| <kbd>⎄ Compose</kbd> <kbd>л</kbd> <kbd>;</kbd>              | ӆ     |
| <kbd>⎄ Compose</kbd> <kbd>м</kbd> <kbd>;</kbd>              | ӎ     |
| <kbd>⎄ Compose</kbd> <kbd>н</kbd> <kbd>;</kbd>              | ӊ     |
| **Буквы с несколькими диакритиками**                        |       |
| <kbd>⎄ Compose</kbd> <kbd>"</kbd> <kbd>-</kbd> <kbd>о</kbd> | ӫ     |
| <kbd>⎄ Compose</kbd> <kbd>-</kbd> <kbd>"</kbd> <kbd>о</kbd> | ӫ     |
| **Буквы, отсутствующие в сербском и македонском**           |       |
| <kbd>⎄ Compose</kbd> <kbd>ј</kbd> <kbd>и</kbd>              | й     |
| <kbd>⎄ Compose</kbd> <kbd>й</kbd> <kbd>о</kbd>              | ё     |
| <kbd>⎄ Compose</kbd> <kbd>ј</kbd> <kbd>о</kbd>              | ё     |
| <kbd>⎄ Compose</kbd> <kbd>й</kbd> <kbd>у</kbd>              | ю     |
| <kbd>⎄ Compose</kbd> <kbd>ј</kbd> <kbd>у</kbd>              | ю     |
| <kbd>⎄ Compose</kbd> <kbd>й</kbd> <kbd>а</kbd>              | я     |
| <kbd>⎄ Compose</kbd> <kbd>ј</kbd> <kbd>а</kbd>              | я     |
| **Знаки валют**                                             |       |
| <kbd>⎄ Compose</kbd> <kbd>=</kbd> <kbd>г</kbd>              | ₴     |
| <kbd>⎄ Compose</kbd> <kbd>г</kbd> <kbd>=</kbd>              | ₴     |
| <kbd>⎄ Compose</kbd> <kbd>=</kbd> <kbd>р</kbd>              | ₽     |
| <kbd>⎄ Compose</kbd> <kbd>р</kbd> <kbd>=</kbd>              | ₽     |
| <kbd>⎄ Compose</kbd> <kbd>=</kbd> <kbd>т</kbd>              | ₮     |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>=</kbd>              | ₮     |
| <kbd>⎄ Compose</kbd> <kbd>_</kbd> <kbd>т</kbd>              | ₸     |
| <kbd>⎄ Compose</kbd> <kbd>т</kbd> <kbd>_</kbd>              | ₸     |
| <kbd>⎄ Compose</kbd> <kbd>_</kbd> <kbd>с</kbd>              | ⃀¹    |
| <kbd>⎄ Compose</kbd> <kbd>с</kbd> <kbd>_</kbd>              | ⃀¹    |

¹: Знак кыргызского сома (подчёркнутая С) лишь в 2021 году был включён в стандарт Unicode, поэтому во многих шрифтах он пока отсутствует.

</details>

## Похожие проекты ##

- [Мультиязычное дополнение к клавиатурной раскладке](https://github.com/uqqu/qPhyx#%D0%B1%D1%83%D0%BA%D0%B2%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5-%D1%80%D0%B0%D1%81%D0%BA%D0%BB%D0%B0%D0%B4%D0%BA%D0%B8) ([статья на Хабре](https://habr.com/ru/articles/592913/))
- [Типографская раскладка для 60-процентной клавиатуры](https://github.com/sukhe/Sukhe-60-percent-keyboard-emulator) ([статья на Хабре](https://habr.com/ru/articles/659471/))
- [Типографская раскладка Ильи Бирмана](https://ilyabirman.ru/typography-layout/)
- [Русско-украинская совмещённая раскладка](http://wiki.opennet.ru/RUU)

## Важное ##

[Queer Svit](https://queersvit.org/) — независимая команда волонтёров со всего мира. С вашей поддержкой мы помогаем ЛГБТК+ сообществу и небелым* людям из Украины, России, Беларуси и других стран региона ВЕЦА. Мы помогаем людям, пострадавшим от войны и/или политических репрессий, оказываем поддержку при переезде — проводим консультации, приобретаем билеты, находим бесплатное жильё и предоставляем гуманитарную помощь.

Война, как и всякая катастрофа, сильнее всего бьет по наиболее уязвимым членам общества. Так, маргинализированные группы (включая ЛГБТК+ и небелых* людей) находятся в большей опасности, но об их проблемах общество почти не слышит. Но так как наша команда и состоит из квир- и небелых* людей, мы не понаслышке знаем о трудностях, с которыми сталкиваются наши бенефициары, и хорошо понимаем, как им помочь.

Ваши пожертвования имеют значение; Queer Svit существует в значительной степени за счет небольших пожертвований индивидуальных жертвователей. Мы благодарны за любую помощь — спасибо!

[Queer Svit](https://queersvit.org/) is a black queer-run independent team of volunteers from all over the world. With your support we help LGBTQ+ and BAME people affected by the war and/or political repressions get to safety by providing consultations, purchasing tickets, finding free accommodation and providing humanitarian aid.

‌‌Just like any other catastrophe, war affects the most those who are most vulnerable, including LGBTQ+ and BAME people while at the same time their troubles are often rendered invisible. But because our own team comprises LGBTQ+ and BAME people we see the specific challenges our beneficiaries face and understand how to help them.

‌Your donations make a difference; Queer Svit is run in large part on small donations from individual donors. We are grateful for any and all help to continue our work — thank you!

## Лицензия ##

[MIT](blob/main/LICENSE)

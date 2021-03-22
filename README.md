# Анти-Максютин

Эй, здесь лежат готовые решения заданий Максютина для ИТИСа на 2 курс 2 семестр!

***⚠⚠⚠ ПРЕДОСТЕРЕЖЕНИЕ!!! Не палитесь перед самим Максютиным, не открывайте перед ним этот репозиторий или другие доки с готовыми решениями и не говорите ему про них, иначе Максютин просто поменяет задания, и готовых решений больше не будет! ⚠⚠⚠***

Структура репозитория:

- Лабораторные работы в папках Lab_XX, где XX — номер работы
	- Общие файлы, относящиеся ко всей лабораторной работе XX (дополнения к заданию, вспомогательные картинки и прочее)
	- Части лабораторной работы в папках Lab_XX_Y, где Y — номер части работы
		- Оригинальное задание от Максютина в файле Lab_XX_Y.txt
		- Решение в файле Lab_XX_Y.md
		- Начальная (собранная для старта задания) топология eNSP для задания в папке eNSP_Initial
		- Готовая топология eNSP для решённого задания в папке eNSP_Final
		- Возможные проверки в папке Tasks

## О заданиях

Максютин в начале каждой пары раздаёт каждому человеку новый номер, его нужно подставлять вместо N при решении заданий: так он проверяет, что лаба сделана самостоятельно, а не списана. В готовых топологиях eNSP считается, что N = 1.

Саму лабу Максютин проверяет по скриншотам, которые нужно скидывать ему. В начале каждой пары он присылает текстовый файл Tasks.txt, в котором есть описание, какие именно скриншоты ожидает Максютин.

## Топологии eNSP

Чтобы работать с топологией eNSP, нужно открыть файл Lab_XX_Y.topo в папке с нужной топологией. Внимание! Путь к файлу Lab_XX_Y.topo не должен содержать кириллицу, иначе топология не откроется.

Зачем нужны эти топологии?

- Начальная топология
  - Быстрый старт задания, когда не хочется самому собирать топологию
- Готовая топология
  - Просмотр конфигурации устройств (команда `display current-configuration`)
  - Проверка на практике, как должно работать готовое решение

Если хочешь сохранить топологию eNSP после её изменения, обрати внимание:

- В пути к файлу с топологией, как уже было написано, не должно быть кириллицы.
- Перед сохранением самой топологии нужно сначала сохранить состояние устройств в ней:
  - Идём в консоль устройства
  - Нажимаем Ctrl+Z, чтобы перейти в user view
  - Выполняем команду `save`
  - Вводим `y` и нажимаем Enter, чтобы подтвердить запись
    - Для коммутаторов потребуется ещё раз нажать Enter, если сохранение происходит в первый раз

## О командах

Для получения [справки о командах](https://support.huawei.com/enterprise/en/doc/EDOC1000178166/31c3c5ba/using-command-line-online-help) в консоли устройств eNSP:

- Набери вопросительный знак, чтобы получить список всех доступных команд.
- Введи начало команды и вопросительный знак, чтобы получить список команд, которые начинаются на введённую последовательность.
- Аналогично делай и с параметрами команды, набирая вопросительный знак на месте параметра команды.

Например:

```
<Huawei> di?
<Huawei> display ?
```

Кстати, есть [документ](https://docs.google.com/document/d/1OLyn9j66fk6rimBzcF10EfehzMgr4ZaK_ySQ-RSVmnc/edit) со списком команд, составленный добрыми людьми нам в помощь.

Почти все команды [можно сокращать](https://support.huawei.com/enterprise/en/doc/EDOC1000178166/51044c5f/editing-command-lines). Если введённые слова можно однозначно дополнить до некоторой команды с учётом параметров, то консоль сама сделает это и выполнит такую команду. Например, следующие команды эквивалентны:

```
<Huawei> display current-configuration
<Huawei> dis cu
<Huawei> di cu
<Huawei> d cu
```

А вот для `d c` и `dis c` уже нельзя найти однозначного соответствия, поэтому консоль выплюнет сообщение `Ambiguous command found`.

Также можно использовать Tab для автодополнения команд.

В целях лучшей читаемости и понятности в решениях заданий будут приводиться полные команды, однако это не означает, что их нельзя сокращать! Пиши `int g0/0/0` вместо `interface GigabitEthernet 0/0/0`! 😉

## Скачать eNSP

[Скачать](https://mega.nz/file/LlgEHITQ#5r8fBBF2ZU9DKRu27wEuqTPcU_mYqPAfmkoTwNdleTc) eNSP последней версии (1.3.00.100). Пароль от архива: `q3Z2*xi87YUC`

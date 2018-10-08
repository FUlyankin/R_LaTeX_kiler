# R_LaTeX_kiler
В этом репозитории лежат файлы для автоматического создания огромного числа однотипных файлов с разным контентом. В качестве примера используются анкеты для игры в киллера.


**В папке лежат:**

1. Служебные файлы:
   * `base.csv` - база данных по людям. Собиралась с помощью гугл-анкет. Люди, которые хотели поиграть, заполняли анкеты.
   * `images` - фотографии людей. В этой же папке лежит файл `urls`. Прописав в терминале `wget -i urls` (конечно же для этого сначала надо перейти в папку, где лежит этот файл), можно скачать все фотографии разом.
   * TypewriterRegular - шрифт прям как на печатной машинке
2. Создание анкет
   * `head.Rnw` - шапочка документа. Преамбула и подгрузка таблички.
   * `body.Rnw` - шаблон для создания анкет. Туда подставляется информация из таблицы `base.csv`
   * `socks.Rnw` - носочки для документа. То, что будет расположено после анкет.
   * `pdf_creator.R` - скрипт, который верстает анкеты в цельный pdf.

На выходе должны получиться файлы: `main.Rnw` - заготовка для анкет и `main.pdf` - готовые анкеты. На всякий случай эти файлы уже лежат в папке.

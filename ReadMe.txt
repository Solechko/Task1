﻿ПОДДЕРЖИВАЕМЫЙ ФУНКЦИОНАЛ:

1. ТВ программа работает в современных браузерах: MSIE, Edge, Firefox, Safari, Google Chrome, Яндекс.Браузер, Opera. 
2. Лэйаут адаптирован для мобильных устройств.
3. Программа содержит раписание программ для 10 телеканалов. Телеканалы не ограничены, зависят от содержимого xmltv.
4. В области заголовка отображаются передачи, показываемые в эфире на данный момент.
5. Отображение информации в двух режимах (переключение - стрелка внизу левого меню): 
	- по дням недели (телепрограммы отображаются для каждого из каналов для выбранного дня недели);
	- по телеканалам (телепрограммы отображаются на всю неделю для выбранного телеканала).
6. Поддерживаются фильтры: фильмы, сериалы, информационные, развлекательные, детям, спорт, познавательные.
7. Поддерживается отображение доп. информации в сплывающем меню при наведении на программу.



ОСОБЕННОСТИ РЕАЛИЗАЦИИ:

1. Данные хранятся в файле формата xmltv.
2. Реализована библиотека xmltvparser.js, которая получает данные из файла формата xmltv.
3. В index.html определены основные блоки и элементы, также определены шаблоны для генерируемой разметки при помощи script.js.
4. По возможности, использовалось наименование css классов по методологии БЭМ.
5. Применение sass для возможности использования переменных, вложенных media классов, для возможности логического разделения классов css и их последующего объединения в style.css.  
6. Использование reset.css.
7. Для иконок используется шрифт icomoon, содержащий только необходимые иконки.
8. Использованы следующие javascript библиотеки:
	- jQuery - для парсинга телепрограммы из XmlDocument, а также при выборках телепрограмм по дням/жанрам/на ближайшее время;
	- moment - для работы с датой/временем телепрограммы, включая получение показываемых сейчас программ и программ на ближайшее время.


 
ЗАДАЧИ, РАШАЕМЫЕ С ПОМОЩЬЮ JAVASCRIPT:

1. Получение данных через xmltvparser.js и генерация разметки (с использованием шаблонов) для отображения телепрограмм в любом из двух режимов, списка телеканалов и программ в эфире. Благодаря этому страничка является динамической и отображает данные xmltv файла.
2. Для фильтрации, при выборе пользователем фильтра, script.js генерирует необходимую разметку в соответствии с выбранными фильтрами.
3. Для переключения между режимами отображения программы.
4. Для фиксирования меню выбора дня недели и телеканала и меню фильтра при скролинге документа.
5. Для отображения всплывающего окна детализации программы. Так как в один момент времени может быть отображено только одно всплывающее окно при наведении на программу, нет смысла в html создавать блок всплывающего окна для каждой программы. Поэтому был создан один блок в общей структуре html, при наведении курсора на программу, script.js рассчитывает позицию всплывающего окна, в зависимости от доступного места, позиционирует его и заполняет его данными, соответствующими программе над которой находится курсор.

  
РАЗВЕРТЫВАНИЕ ПРИЛОЖЕНИЯ:

Для работы приложения показа ТВ программы, его необходимо развернуть на любом веб-сервере, поддерживающем статическую отдачу контента. Например, на IIS или Apache. Так же оно может быть развернуто на сервере GitHub Pages или любом аналогичном.


Тарасов Сергей Владимирович
----------------------------
Объемы работ по [прикладному программированию](https://en.wikipedia.org/wiki/Application_software) на [**C++**](https://en.wikipedia.org/wiki/C%2B%2B), [**Tcl/Tk**](https://en.wikipedia.org/wiki/Tcl), [**Python**](https://en.wikipedia.org/wiki/Python_(programming_language)) на [Windows Server](https://en.wikipedia.org/wiki/Windows_Server) для [централизованных вычислений](https://en.wikipedia.org/wiki/Centralized_computing) и для [распределенных вычислений](https://en.wikipedia.org/wiki/Distributed_computing), а также на [клиентской Windows](https://en.wikipedia.org/wiki/Microsoft_Windows) для [децентрализованных вычислений](https://en.wikipedia.org/wiki/Decentralized_computing):

Язык [C++](https://isocpp.org/) в настоящее время в основном используется для написания операционных систем, драйверов и коммерческого программного обеспечения и в источниках уже не упоминается как язык высокого уровня.

Язык [Tcl](https://www.tcl.tk/about/language.html) (имеет возможности примерно как у [Pascal](https://en.wikipedia.org/wiki/Pascal_(programming_language)) и [Basic](https://en.wikipedia.org/wiki/BASIC)) изначально был задуман для системных задач, в конце 1990-х также применятся для написания скриптов-обработчиков виджетов на графических оболочках внутри например среды разработки [tkBuilder](https://sourceforge.net/projects/tkbuilder84/) и [Komodo](https://www.activestate.com/products/komodo-ide/).

Язык [R](https://en.wikipedia.org/wiki/R_(programming_language)) - предметно-ориентированный язык с бедным набором типов данных. Приложений на нем нет. Есть скрипты, которые можно исполнять на голом интерпретаторе или внутри среды разработки [R-Studio](https://en.wikipedia.org/wiki/RStudio) (еще достаточно кривая), в котором наблюдаются косяки с отображением разных кодировок. Документации по нему мало, примеров тоже мало. При занятости сервера СУБД ждет несколько секунд и сбрасывает соединение.

Доля [Python](https://www.python.org/)-а в прикладном программировании увеличивается по сравнению с остальными языками. Фрэймворки [Tk, Ttk и Ttk+](https://en.wikipedia.org/wiki/Tk_(software)) в виде комплектной библиотеки [tkinter](https://en.wikipedia.org/wiki/Tkinter) имеют ограниченные возможности для творчества по сравнению с самым ходовым фрэймворком [pyQt](https://en.wikipedia.org/wiki/Qt_(software)). Фрэймворк [pySimpleGUI](https://www.pysimplegui.org/en/latest/) прост, интересен, имеет наборы стилей, внешне напоминает ВЭБ-разработку, но на нем мало примеров. Фрэймворки [Gtk и Gtk+](https://en.wikipedia.org/wiki/GTK) используются в Linux-е и в настоящее время имеют ошибки (библиотека pyGTK на Windows пока не ставится). Фрэймворк [wxPython](https://en.wikipedia.org/wiki/WxPython) неправильно отображает кодировки и не пропорцинально отображает виждеты в разных сочетаниях.

Для простой прикладной задачи вполне подходит скрипт, работающий в командной строке с ключами и с путями. Для одновременного обозревания нескольких параметров в прикладной задаче разрабатывается и применяется графическая оболочка (окно с диалогами или диалог с диалогами). Если требуется что-то явить миру, поверх серверной или отдельной клиентской компоненты подымается ВЭБ-сайт (выполняется отдельно, в объем данных репозиториев может входить в виде подмодуля как внешняя разработка).

 - Прототипирование

В принципе практически все наработки являются прототипами и склоняются к циклу **"Анализ - Дизайн - Разработка - Тестирование - Эксплуатация - Анализ"**, поэтому для поддержания актуальности требуют постоянного совершенствования (UX/UI и CI/CD).

 - Расчеты и математическое моделирование

С появлением вычислительной техники в 1990-х многие эмпирические методы в прикладной математике с номограммами потеряли свою практическую пользу. Стало возможно посчитать аналитические формулы напрямую, используя конечно-разностные формы их записи. Посчитали различные задачи оптимизации, которые ждали своего решения еще с 1960-х годов. Для удобства восприятия решение как правило стремились получить в виде экстремума градиента на поверхности или на облаке точек, подбирая диапазоны итерации вручную или более осторожно методом последовательного приближения.

- Разработка и администрирование баз данных на **MS SQL Server**-е в части **[SQL](https://en.wikipedia.org/wiki/SQL) + [XML](https://en.wikipedia.org/wiki/XML)** [описание](http://www.chernyshov.com/SPPO_6/theory/wt_xml.htm) ([XPath](https://en.wikipedia.org/wiki/XPath) & [XQuery](https://en.wikipedia.org/wiki/XQuery), [XSD](https://en.wikipedia.org/wiki/XML_Schema_(W3C)) [описание](https://bdpx.github.io/xml/lab3/xsd.html)). А также [EXPath](http://expath.org/), [XSL](https://en.wikipedia.org/wiki/XSL), [XSLT](https://en.wikipedia.org/wiki/XSLT), [EXSLT](https://en.wikipedia.org/wiki/EXSLT), [Relax NG](https://en.wikipedia.org/wiki/RELAX_NG), [XSpec](https://github.com/expath/xspec/tree/master), [XLink](https://en.wikipedia.org/wiki/XLink), [XMark](https://projects.cwi.nl/xmark/index.html), [XInclude](https://www.w3.org/TR/xinclude/), [XProc](https://en.wikipedia.org/wiki/XProc), [OPML](https://en.wikipedia.org/wiki/OPML), [XQL](http://www.ibiblio.org/xql/xql-proposal.html)

**SQL** и **XML** по отдельности имеют много разной критики, но по полноте функционала замены им пока не наблюдается. Есть определенные ограничения в преобразовании типов данных по цепочке `Python <-> SQL <-> XML`, так как типы данных из пространств имен XSD, XQuery аскетичнее и не перекрываются полностью. Есть сложности в возврате результата работы (кода возврата) функции (хранимой процедуры) `XPath & XQuery -> SQL -> Python`. Это важный момент, так как если ничего не предпринять дополнительно, то SQL Server при возрастании нагрузки не собирает запросы от прикладной программы в очередь, а откидывает их в том числе по взаимоблокировке и недогружается. Разрабатывается собственный [функционал](https://docs.sqlalchemy.org/en/14/dialects/mssql.html#module-sqlalchemy.dialects.mssql.pyodbc) Python-а для работы с SQL Server-ом, но нет плагина или интеграции [Saxon](https://www.saxonica.com/about/about.xml)-а, [Schematron](https://en.wikipedia.org/wiki/Schematron)-а и возможностей [BaseX](https://en.wikipedia.org/wiki/BaseX) внутри ядра баз данных. Таким образом для достижения красоты и гармонии в прикладном программировании усилий разработчиков мало. Требуется также прогресс в развитии SQL Server-а.

Много разрозненных наработок, использующих возможности только **XML** для работы с данными недоведены, устарели и стали историей.

[**Объектно-ориентированные базы данных**](https://en.wikipedia.org/wiki/Object_database) в виде составных и пользовательских типов данных с неограниченной гибкостью как продолжение темы [**объектно-ориентированного программирования (сокращенно ООП)**](https://en.wikipedia.org/wiki/Object-oriented_programming), начиная со списков и словарей с их срезами, DataFrame-ы как главный козырь [Pandas](https://en.wikipedia.org/wiki/Pandas_(software)) и заканчивая классами с их композицией и наследованием, к которым подводят мысль во многих книгах, пока к сожалению не обрели своих СУБД и используются в университетской среде насколько позволяет оперативная память операционной системы и только в однопользовательском режиме. В **DataScience** с разным успехом применяют богатые возможности DataFrame-ов для импорта моментальных снимков баз данных и их анализа, но перегонять снимок в память - это очень круто даже для их серверов.

[**не-SQL-ные СУБД**](https://aws.amazon.com/ru/nosql/), числу которых сейчас нет счета, по сравнению с **SQL-ными** имеют столько преимуществ сколько и неудобств. Какая-то одна в чем-то лучше и в чем-то хуже какой-то другой. Большинство из них в разных модификациях являются продолжением темы [JSON](https://en.wikipedia.org/wiki/JSON) + двоичные поля и [BLOB](https://en.wikipedia.org/wiki/Binary_large_object)-ы. Кстати, могли бы сразу за основу взять [YAML](https://en.wikipedia.org/wiki/YAML). Но видимо разработчики - сторонники JavaScript-а. Не заменят XML, так как есть принципиальное отличие:
 - `*.xml` - ветвление, топология, структура,
 - `*.dat, *.ini, *.json, *.yaml` - словарь, конфигурация, настройка.

Есть коммерческие платформы для работы с данными непонятно на чем, например [MarkLogic](https://www.marklogic.com/), но они сами в себе

![007 001 001](https://user-images.githubusercontent.com/104857185/209877366-3c1a9309-736c-49ce-9bb3-709e16110020.jpg)

- Замена бумажного и электронного документооборота, а также замена коммерческих консультантов

Руководящие документы (Руководства, Нормативы, Стандарты, Приказы, Инструкции) необходимо перестать распечатывать на бумаге, а также гонять их копии разной давности с ЭЦП и без по электронной почте, ватсапам, телегам и соцсетям. Необходимо дать доступ к ним только из единственного авторитетного источника не в виде художественного текста, а в виде чистого императива, который может определенно и однозначно восприниматься прикладными программами для принятия решений и возврата отчетов о выполнении. Для этого их вероятно потребуется **переосмыслить**, перенеся повествовательную часть в комментарии, и **продумать их структуру ветвления** с данными, параметрами и ссылками на другие источники в зависимости от типа документа и его отрасли, затем **сохранить в формате XML**, чтобы упорядоченно **записать в поля** `XML(CONTENT dbo.XSD-схема)` таблиц баз данных и **парсить** как [DOM](https://ru.wikipedia.org/wiki/Document_Object_Model) или [SAX](https://en.wikipedia.org/wiki/Simple_API_for_XML) запросами на XPath & XQuery **вручную** или **программно** в прикладных задачах. Таким образом документы и вносимые в них изменения смогут быстро и просто исполняться без перечитывания их текста, без сравнения с предыдущими редакциями и без трактования их разными людьми в разных контекстах и ситуациях.

###### Хранение информации в файлах различных типов и их использование

![1 001 001](https://user-images.githubusercontent.com/104857185/167037090-9cd548c0-9643-4903-adce-13e2a039226d.jpg)

 - API-шки сопряжения с автоматикой смежных систем

[API-шки](https://en.wikipedia.org/wiki/API) в широком понимании модели [Клиент - Сервер](https://en.wikipedia.org/wiki/Client%E2%80%93server_model) локально или по сети применяются для облегчения внесения изменений и для обеспечения единообразия в повторном применении исходных текстов (функции, интерфейсы, статические и динамические библиотеки) на всех клиентах в обращениях к службам, предоставляемым серверными компонентами в [Сервисном слое](https://en.wikipedia.org/wiki/Service_layer), который сопоставляется с прикладным слоем в [Модели OSI](https://en.wikipedia.org/wiki/OSI_model) разной степени гибкости [Сервис-ориентированной архитектуры](https://en.wikipedia.org/wiki/Service-oriented_architecture) и который пока относят к стороннему (часто закрытому) программному обеспечению, дописанному дополнительно к общеизвестным прикладным протоколам. Этот слой в полном варианте состоит из пары - сервер состояний (в идеале внешний сервер СУБД) и сервер сообщений о событиях (например OPC-сервер).

Фирмы-изготовители оборудования и программного обеспечения для работы с ним, к которому они не прилагают исчерпывающее описание состояний и событий, свои DDK и SDK, а также и исходные тексты для написания API-шек, в эту идею к сожалению не вписываются, так как этим исключают интеграцию с ними прикладных задач. Они закрываются, применяя сертификаты, программные и аппаратные ключи, смарт-лицензии и активацию по сети, а к широкому сообществу обращаются лишь раз от разу при потребности в свежих идеях, которых это сообщество без глубокого вовлечения вероятно дает недостаточно. Они чрезмерно увлеклись переносом функционала на [Облака](https://en.wikipedia.org/wiki/Cloud_computing), увеличивая вероятность отказов при разрывах соединения с первичным оборудованием. Таким образом, без проникновения концепции [Open Source](https://en.wikipedia.org/wiki/Open_source) технический прогресс в этой отрасли смещается в сторону налаживания межоблачного взаимодействия и наблюдается замедление в развитии программной части для первичного оборудования (прошивки, операционные системы, языки программирования, конфигураторы) и соответственно самого первичного оборудования. Ситуация вынуждает опытных разработчиков искать простора для полета их творческой мысли в стартапах на более мелких задачах. Требуется политическое решение

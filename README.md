Тарасов Сергей Владимирович
----------------------------

 - Прототипирование

В принципе практически все наработки являются прототипами и склоняются к циклу "Анализ - Дизайн - Разработка - Тестирование - Эксплуатация - Анализ", поэтому для поддержания актуальности требуют постоянного совершенствования (UX/UI и CI/CD).

 - Расчеты и математическое моделирование

С появлением вычислительной техники в 1990-х многие эмпирические методы в прикладной математике с номограммами потеряли свою практическую пользу. Стало возможно посчитать аналитические формулы напрямую, используя конечно-разностные формы их записи. Посчитали различные задачи оптимизации, которые ждали своего решения еще с 1960-х годов. Для удобства восприятия решение как правило стремились получить в виде экстремума градиента на поверхности или на облаке точек, подбирая диапазоны итерации вручную или более осторожно методом последовательного приближения.

 - Прикладное программирование на **[C++](https://en.wikipedia.org/wiki/C%2B%2B)**, **[Tcl/Tk](https://en.wikipedia.org/wiki/Tcl)**, **[Python](https://en.wikipedia.org/wiki/Python_(programming_language))** (текстовые и графические оболочки)

Для простой прикладной задачи вполне подходит скрипт, работающий в командной строке с ключами и с путями. Для одновременного обозревания нескольких параметров в прикладной задаче разрабатывается и применяется графическая оболочка (окно с диалогами или диалог с диалогами). Если нужно что-то явить миру, поверх прикладной компоненты (серверной или клиентской) делается ВЭБ-сайт (выполняется отдельно, в объем данных репозиториев может входить в виде подмодуля как внешняя разработка).

- Разработка и администрирование баз данных на **MS SQL Server**-е в части **[SQL](https://en.wikipedia.org/wiki/SQL) + [XML](https://en.wikipedia.org/wiki/XML)** [описание](http://www.chernyshov.com/SPPO_6/theory/wt_xml.htm) ([XPath](https://en.wikipedia.org/wiki/XPath) & [XQuery](https://en.wikipedia.org/wiki/XQuery), [XSD](https://en.wikipedia.org/wiki/XML_Schema_(W3C)) [описание](https://bdpx.github.io/xml/lab3/xsd.html)). А также [EXPath](http://expath.org/), [XSL](https://ru.wikipedia.org/wiki/XSL), [XSLT](https://en.wikipedia.org/wiki/XSLT), [EXSLT](https://ru.wikipedia.org/wiki/EXSLT), [Relax NG](https://en.wikipedia.org/wiki/RELAX_NG), [XSpec](https://github.com/expath/xspec/tree/master), [XLink](https://en.wikipedia.org/wiki/XLink), [XMark](https://projects.cwi.nl/xmark/index.html), [XInclude](https://www.w3.org/TR/xinclude/), [XProc](https://en.wikipedia.org/wiki/XProc), [OPML](https://en.wikipedia.org/wiki/OPML), [XQL](http://www.ibiblio.org/xql/xql-proposal.html)

**SQL** и **XML** по отдельности имеют много разной критики, но по полноте функционала замены пока не наблюдается. Есть определенные ограничения в преобразовании типов данных `Python -> SQL -> XML` и обратно, так как типы данных из пространств имен XSD, XQuery беднее и аскетичнее. Есть сложности в передаче результата работы (кода возврата) функции (хранимой процедуры) `Python -> SQL -> XPath & XQuery` по цепочке и обратно. Это важный момент, так как если ничего не предпринять дополнительно, то SQL Server при возрастании нагрузки не собирает запросы от прикладной программы в очередь, а откидывает их по взаимоблокировке и недогружается. Разрабатывается собственный [функционал](https://docs.sqlalchemy.org/en/14/dialects/mssql.html#module-sqlalchemy.dialects.mssql.pyodbc) Python-а для работы с SQL Server-ом, но нет плагина или интеграции [Saxon](https://www.saxonica.com/about/about.xml)-а, [Schematron](https://en.wikipedia.org/wiki/Schematron)-а и возможностей [BaseX](https://ru.wikipedia.org/wiki/BaseX) внутри ядра баз данных. Таким образом для достижения красоты и гармонии в прикладном программировании усилий разработчиков мало. Требуется также прогресс в развитии SQL Server-а.

Много разрозненных наработок, использующих возможности только **XML** для работы с данными недоведены, устарели и стали историей.

**Объектно-ориентированные базы данных** в виде составных и пользовательских типов данных с неограниченной гибкостью как продолжение темы **объектно-ориентированного программирования (сокращенно ООП)**, начиная со списков и словарей с их срезами, DataFrame-ы как главный козырь [pandas](https://en.wikipedia.org/wiki/Pandas_(software)) и заканчивая классами с их композицией и наследованием, к которым подводят мысль во многих книгах, пока к сожалению не получили своих СУБД и используются в университетской среде для небольших и несложных объемов данных настолько, насколько позволяет оперативная память операционной системы, на которой их исполняют и только в однопользовательском режиме. В **DataScience** с разным успехом применяют богатые возможности DataFrame-ов для импорта моментальных снимков баз данных и их анализа, но перегонять снимок в память - это очень круто даже для их серверов.

**не-SQL-ные СУБД**, числу которых сейчас нет счета, по сравнению с **SQL-ными** имеют столько преимуществ сколько и неудобств. Какая-то одна в чем-то лучше и в чем-то хуже какой-то другой. Большинство из них в разных модификациях являются продолжением темы JSON + двоичные поля и BLOB-ы. Кстати, могли бы сразу за основу взять YAML. Но видимо разработчики - сторонники JavaScript-а. Не заменят XML, так как есть принципиальное отличие:
 - `*.xml` - ветвление, топология, структура,
 - `*.dat, *.ini, *.json, *.yaml` - словарь, конфигурация, настройка.

Есть коммерческие платформы для работы с данными непонятно на чем, например [MarkLogic](https://www.marklogic.com/), но они сами в себе

![007 001 001](https://user-images.githubusercontent.com/104857185/209877366-3c1a9309-736c-49ce-9bb3-709e16110020.jpg)

 - API-шки

[API-шки](https://en.wikipedia.org/wiki/API) в широком понимании, как продолжение идеи [распределенных вычислений](https://en.wikipedia.org/wiki/Distributed_computing) в прикладном программировании, применяются для обеспечения работы модели [Клиент - Сервер](https://en.wikipedia.org/wiki/Client%E2%80%93server_model) локально или по сети для единообразного повторного применения исходных текстов (функции, интерфейсы, статические и динамические библиотеки) клиентами в обращениях к службам, предоставляемым серверными компонентами (в полном варианте - сервер состояний и сервер сообщений) в [сервисном слое](https://en.wikipedia.org/wiki/Service_layer), который сопоставляется с прикладным слоем [модели OSI](https://en.wikipedia.org/wiki/OSI_model) разной степени гибкости [Сервис-ориентированной архитектуры](https://en.wikipedia.org/wiki/Service-oriented_architecture) и который пока относят к стороннему (часто закрытому) программному обеспечению, дописанному дополнительно к общеизвестным прикладным протоколам

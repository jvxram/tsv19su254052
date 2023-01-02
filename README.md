Тарасов Сергей Владимирович
----------------------------

 - Прототипирование

В принципе практически все наработки являются прототипами и соответсвуют циклу "Анализ - Дизайн - Разработка - Тестирование - Эксплуатация - Анализ" и требуют постоянного совершенствования (UX/UI и CI/CD).

 - Расчеты и математическое моделирование

С появлением вычислительной техники в 1990-х многие императивные и приближенные методы в математике с номограммами потеряли свою практическую пользу. Стало возможно посчитать аналитические формулы напрямую, использую конечно-разностные методы, не теряя точности. Посчитали многие прикладные математические задачи в том числе различные оптимизации, которые ждали своего решения еще с 1960-х годов. В основном решение получали в виде экстремума на поверхности или на облаке точек.

 - Прикладное программирование на **[C++](https://en.wikipedia.org/wiki/C%2B%2B)**, **[Tcl/Tk](https://en.wikipedia.org/wiki/Tcl)**, **[Python](https://en.wikipedia.org/wiki/Python_(programming_language))** (Текстовые приложения, Графические оболочки)

Для простой прикладной задачи вполне подходит скрипт, работающий в командной строке с ключами и путями. Для одновременного обозревания нескольких параметров в том числе для работы с данными из СУБД в прикладной задаче разрабатывается и применяется графическая оболочка (диалог и окно). Если нужно что-то явить миру, поверх прикладной компоненты (серверной или клиентской) делается ВЭБ-сайт (выполняется отдельно, в объем данных репозиториев может входить в виде подмодуля как внешняя разработка).

- Разработка и администрирование баз данных на **MS SQL Server**-е в части **[SQL](https://en.wikipedia.org/wiki/SQL) + [XML](https://en.wikipedia.org/wiki/XML)** [описание](http://www.chernyshov.com/SPPO_6/theory/wt_xml.htm) ([XPath](https://en.wikipedia.org/wiki/XPath) & [XQuery](https://en.wikipedia.org/wiki/XQuery), [EXPath](http://expath.org/), [XSD](https://en.wikipedia.org/wiki/XML_Schema_(W3C)) [описание](https://bdpx.github.io/xml/lab3/xsd.html), [XSL](https://ru.wikipedia.org/wiki/XSL), [XSLT](https://en.wikipedia.org/wiki/XSLT). [EXSLT](https://ru.wikipedia.org/wiki/EXSLT), [Relax NG](https://en.wikipedia.org/wiki/RELAX_NG), [XSpec](https://github.com/expath/xspec/tree/master), [XLink](https://en.wikipedia.org/wiki/XLink), [XMark](https://projects.cwi.nl/xmark/index.html), [XInclude](https://www.w3.org/TR/xinclude/), [XProc](https://en.wikipedia.org/wiki/XProc), [OPML](https://en.wikipedia.org/wiki/OPML), [XQL](http://www.ibiblio.org/xql/xql-proposal.html))

**SQL** и **XML** по отдельности имеют много разной критики, но по полноте функционала замены пока не наблюдается. Есть определенные ограничения в преобразовании типов данных `Python -> SQL -> XML` и обратно, так как типы данных из пространств имен XSD, XQuery беднее и аскетичнее. Есть сложности в передаче результата работы (кода возврата) функции (хранимой процедуры) `Python -> SQL -> XPath & XQuery` по цепочке и обратно. Это важный момент, так как если ничего не предпринять дополнительно, то SQL Server при возрастании нагрузки не собирает запросы от прикладной программы в очередь, а откидывает их в том числе по взаимоблокировке и недогружается. Разрабатывается собственный [функционал](https://docs.sqlalchemy.org/en/14/dialects/mssql.html#module-sqlalchemy.dialects.mssql.pyodbc) Python-а для работы с SQL Server-ом, но нет плагина или интеграции [Saxon-а](https://www.saxonica.com/about/about.xml), [Schematron-а](https://en.wikipedia.org/wiki/Schematron) и возможностей [BaseX](https://ru.wikipedia.org/wiki/BaseX) внутри ядра баз данных. Таким образом для достижения красоты и гармонии в прикладном программировании усилий разработчиков мало. Требуется также прогресс в развитии SQL Server-а.

Много разрозненных наработок, использующих возможности только **XML** для работы с данными недоведены, устарели и стали историей.

**Объектно-ориентированные базы данных** в виде составных и пользовательских типов данных с неограниченной гибкостью как продолжение темы **объектно-ориентированного программирования (сокращенно ООП)**, начиная со списков и словарей с их срезами, DataFrame-ы как главный козырь [pandas](https://en.wikipedia.org/wiki/Pandas_(software)) и заканчивая классами с их композицией и наследованием, к которым подводят мысль во многих книгах, пока к сожалению не имеют своих СУБД и используются в университетской среде для небольших и несложных объемов данных настолько, насколько позволяет оперативная память операционной системы, на которой их исполняют и только в однопользовательском режиме. В **DataScience** с разным успехом применяют богатые возможности DataFrame-ов для импорта моментальных снимков баз данных и их анализа, но перегонять снимок в память - это очень круто даже для их серверов.

**не-SQL-ные СУБД**, числу которых сейчас нет счета, по сравнению с **SQL-ными** имеют столько преимуществ сколько и неудобств. Какая-то одна в чем-то лучше и в чем-то хуже какой-то другой. Большинство из них в разных модификациях являются продолжением темы JSON + двоичные поля и BLOB-ы. Кстати, могли бы сразу за основу взять YAML. Но видимо разработчики - сторонники JavaScript-а. Не заменят XML, так как есть принципиальное отличие:
 - `*.xml` - ветвление, топология, структура,
 - `*.dat, *.ini, *.json, *.yaml` - словарь, конфигурация, настройка.

Есть коммерческие платформы для работы с данными непонятно на чем, например [MarkLogic](https://www.marklogic.com/), но они сами в себе

![007 001 001](https://user-images.githubusercontent.com/104857185/209877366-3c1a9309-736c-49ce-9bb3-709e16110020.jpg)

 - API-шки

API-шки в своем широком понимании применяются для обеспечения работы модели "Клиент - Сервер" локально или по локальным сетям в пользовательских типах данных для многократного применения исходных текстов (статические и динамические библиотеки, интерфейсы, технологии СОМ и DCOM) разной степени гибкости

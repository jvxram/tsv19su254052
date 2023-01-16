[Объемы выполняемых работ и способы их выполнения](https://github.com/tsv19su254052/tsv19su254052/blob/main/Works.md)

[Применяемые языки программирования и их библиотеки](https://github.com/tsv19su254052/tsv19su254052/blob/main/Languages.md)

Примечания:

Репозитории индувидуальной разработки здесь и в организациях являются так сказать неполными **бэкапами с оригиналов проектов** (только отслеживаемые на `Git`-е файлы проекта). Функция `GitHub`-а ограничена возможностью:
 - выбрать текущую ветку,
 - почитать текстовые и графические пояснения к проекту,
 - ознакомиться с математическим обеспечением,
 - посмотреть исходники,
 - почитать объемы доработок,
 - предложить правку с помощью `Pull Request`-а, предварительно уточнив ветку для внесения правок,
 - склонировать исходники себе или ответвить их у себя (клон или ветка со временем устареет или разойдется с оригиналом -> будет конфликт слияния).

Синхронизировать (привести в соответствие версии) подмодули на репозитории и его клонах средствами `GitHub`-а не получится, потому что они импортированы внутри среды разработки в проект асинхронно как дубликаты (синхронизируются с их оригиналами в окошке терминала командами `Git`-а) и соответственно не отслеживаются на `Git`-е (не дублируются дважды) для экономии места на репозитории (там только неактивные ссылки на их оригиналы в их репозиториях).

При добавлении участника в `Contributor`-ы его активность на `GitHub`-е (если она ему так важна и нужна) не видна ни у него, ни у остальных.

Оригиналы проектов хранятся в сетевой папке на файловом сервере, полностью функциональны только внутри инфраструктуры и могут запускаться на исполнение:
 - из внешней сети по RDP на терминальном сервере с одним набором интерпретаторов и библиотек для всех клиентов,
 - в локальной подсетке на клиенте c подключенной сетевой папки (интерпретатор и библиотеки, устанавливаются дополнительно).

Настройки серверов, базы данных на них и их бэкапы, конфигурация и топология аппаратуры, настройки локальной сети (адреса, шлюзы, сервера, vlan-ы и прочее), прошивки аппаратуры и остальные технические тонкости на `GitHub`-е как правило не даются, так как он их не понимает (их можно открыть и прочитать только на аппаратуре или в конфигураторе аппаратуры) и в этом нет практической пользы. Если есть необходимость обмениваться ими, то эти действия осуществляются напрямую через файловый сервер мимо `GitHub`-а, чтобы не делать лишние ходы.

----
Связаться со мной можно в обсуждениях на репозиториях. К критике отношусь конструктивно. Буду благодарен за замечания.

Проспонсировать :sparkling_heart: можно на карточку :credit_card: СберБанка 2202 2023 9940 1326

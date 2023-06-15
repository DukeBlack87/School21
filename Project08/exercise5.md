# POWERSHELL

## Что такое PowerShell?

**Windows PowerShell** позволяет системным администраторам автоматизировать большинство рутинных задач. С ее помощью можно менять настройки, останавливать и запускать сервисы, а также производить обслуживание большинства установленных приложений. Воспринимать синее окошко как еще один интерпретатор команд было бы неправильно. Такой подход не отражает сути предложенных корпорацией Microsoft инноваций. На самом деле возможности Windows PowerShell гораздо шире: в небольшом цикле статей мы попробуем разобраться, чем решение Microsoft отличается от более привычных нам средств.

В 2003 году корпорация Microsoft начала разработку нового инструмента — Microsoft Shell (MSH), или Monad. Спустя три года и три бета-версии Monad была официально выпущена под новым названием Windows PowerShell 1.0 на Windows XP и Windows Vista. По ходу развития командная оболочка меняла свои названия на PowerShell Core и PowerShell.

При создании PowerShell разработчики задались целью создать инструмент, который позволил бы с легкостью использовать множество разнородных интерфейсов, предоставляемых операционной системой. Новый инструмент должен быть консистентным и легким для администратора, несмотря на количество технологий «под капотом». Например, PowerShell предоставляет доступ к API .NET-фреймворка, но не требует от администратора знания .NET.

Как и любой командный интерпретатор, PowerShell умеет запускать исполняемые файлы и имеет встроенные команды. Однако у PowerShell встроенные команды имеют название «командлет», появившееся от английского cmdlet.

## Возможности PowerShell

Windows PowerShell — это в первую очередь командная оболочка с языком сценариев, изначально созданная на основе платформы .NET Framework, а позднее — на .NET Core. В отличие от принимающих и возвращающих текстовые данные оболочек, Windows PowerShell работает с классами .NET, у которых есть свойства и методы. PowerShell позволяет выполнять обычные команды, а также дает доступ к объектам COM, WMI и ADSI. В ней используются различные хранилища, вроде файловой системы или реестра Windows, для доступа к которым созданы т.н. поставщики (providers). Стоит отметить возможность встраивания исполняемых компонентов PowerShell в другие приложения для реализации различных операций, в т.ч. через графический интерфейс. Верно и обратное: многие приложения для Windows предоставляют доступ к своим интерфейсам управления через PowerShell.

Windows PowerShell позволяет:

- Менять настройки операционной системы;
- Управлять службами и процессами;
- Настраивать роли и компоненты сервера;
- Устанавливать программное обеспечение;
- Управлять установленным ПО через специальные интерфейсы;
- Встраивать исполняемые компоненты в сторонние программы;
- Создавать сценарии для автоматизации задач администрирования;
- Работать с файловой системой, реестром Windows, хранилищем сертификатов и т.д.

## Открытие журнала событий в PowerShell

Журнал событий Windows PowerShell можно просмотреть в Просмотр событий или с помощью Get-EventLog командлетов и Get-WmiObject . Чтобы просмотреть содержимое журнала Windows PowerShell, ввести следующее:

    Get-EventLog -LogName "Windows PowerShell"

Чтобы изучить события и их свойства, используйте Sort-Object командлет, Group-Object командлет и командлеты, содержащие Format команду ( Format командлеты ).
Например, чтобы просмотреть события в журнале, сгруппированные по идентификатору события, ввести:

    Get-EventLog "Windows PowerShell" | Format-Table -GroupBy EventID

Или ввести:

    Get-EventLog "Windows PowerShell" |
    Sort-Object EventID |
    Group-Object EventID

Чтобы просмотреть все классические журналы событий, ввести:

    Get-EventLog -List

- *На данный момент в Windows доступны два командлета для доступа к событиям в Event Log: Get-EventLog и Get-WinEvent. В подавляющем большинстве случаев рекомендуется использовать именно Get-WinEvent, т.к. он более производителен, особенно в сценариях обработки большого количества событий с удаленных компьютеров. Командлет Get-EventLog является устаревшим и использовался для получения логов в более ранних версиях Windows. Кроме того, Get-EventLog не поддерживается в современных версиях PowerShell Core 7.x.*

    *Для получения списка событий из определенного журнала, нужно указать его имя. В данном примере мы выведем последние 20 событий из журнала System:*

        Get-WinEvent -LogName Application -MaxEvents 20

    *Чаще всего вам нужно будет получать информацию из журналов System, Application, Security или Setup. Но вы можете указать и другие журналы. Полный список журналов событий в Windows можно получить с помощью команды:*

        Get-WinEvent -ListLog *

Вы также можете использовать Get-WmiObject командлет , чтобы использовать связанные с событиями классы инструментария управления Windows (WMI) для проверки журнала событий. Например, чтобы просмотреть все свойства файла журнала событий, ввести:

    Get-WmiObject Win32_NTEventlogFile |
      where LogFileName -EQ "Windows PowerShell" |
      Format-List -Property *

Чтобы найти классы WMI, связанные с событиями Win32, ввести:

    Get-WmiObject -List | where Name -Like "win32*event*"

Для получения дополнительных сведений ввести:

    Get-Help Get-EventLog и Get-Help Get-WmiObject.

- *По умолчанию PowerShell поставляется с командлетами для использования вместе с другими технологиями, такими как инструментарий управления Windows (WMI). Существует несколько собственных командлетов WMI, которые используются в PowerShell без необходимости установки дополнительного программного обеспечения или модулей.*

    *PowerShell поставляется с командлетами для работы с инструментарием WMI с момента выпуска. Get-Command можно использовать для определения командлетов WMI, существующих в PowerShell.*

        Get-Command -Noun WMI*

    *Командлеты модели CIM появились в PowerShell версии 3.0. Командлеты CIM разработаны так, чтобы их можно было использовать на компьютерах под управлением Windows и других ОС. Командлеты WMI являются устаревшими, поэтому вместо них рекомендуется использовать командлеты CIM.*

    *Все командлеты CIM содержатся в модуле. Чтобы получить список командлетов CIM, используйте Get-Command вместе с параметром Module, как показано в следующем примере.*

        Get-Command -Module CimCmdlets

## Отличия cmd от PowerShell

По сравнению с **cmd, Powershell** может гораздо больше, и это на фоне того факта, что практически всё, что может cmd, прокатит и в **PowerShell**. Однако для работы с shell придётся использовать уже **отдельный вид команд**, которые, дабы на русском не звучало косноязычно, переводчики назвали **«командлетами»**. В отличие от cmd, **в shell команды исполняются по нескольким каналам. Это значит, что выход одной команды (в смысле, командлета) может быть одновременно входом в другую**. И всё потому, что **командлеты  PowerShell** — это вполне себе определённые объекты, представители конкретной структуры данных. Даже те командлеты, которые встречают в ответе shell на запрос пользователя. Выражаясь языком программистов, **PSH — объектно-ориентированный**, а **cmd обрабатывает только символы или последовательность символов.** Проще говоря, **PowerShell позволяет работать с некоторыми программами изнутри, в режиме реального времени, интерактивно. Cmd, в сущности, может только запускать утилиты, которые в Windows уже существуют (почти все они в папке C:\Windows).**

Более того, **PowerShell** — это вполне себе законченная среда для написания и исполнения скрипта. Так что можно создавать очень сложные и объёмные скрипты для управления системой, чем те, на какие была способна консоль cmd.

Основная разница между PowerShell и cmd в том, что последняя — **это обновлённая версия «отжившей» в своё время программной оболочки DOS**, а в первую, как видно, Windows вдыхает новую жизнь. Очевидно демонстрируя, что от DOS команд разработчики отказываться вообще не собираются. Сравнение с DOS уже неверно, та очень ограничена в своих возможностях; **cmd существовала в Windows как «наследие DOS для избранных» или ремонтный, прямой вариант самых необходимых команд.** А ввод в работу **PowerShell — это как своеобразное предложение, если не покопаться во внутренностях системы, то поучаствовать в изучении её возможностей и способ заняться её модификацией вполне официально:** интеграция в среду .Net тому подтверждение.
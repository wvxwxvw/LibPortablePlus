# LibPortablePlus
  
[Скачать сборку Firefox_ESR.91.x.x.x32-64.(22.07.12)](https://github.com/wvxwxvw/LibPortablePlus/raw/main/Firefox_ESR.91.x.x.x32-64.(22.07.12).7z)  
Также имеется преднастроенный профиль:  
[Почитать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/README.md) | [Скачать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/raw/main/Firefox.91.ESR.LPP.profile.220714.7z) | [Посмотреть с TST](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/tstex-screen.md) | [Посмотреть без TST](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/ntfex-screen.md)  
  
## Портативная версия Firefox ESR (32-64)  
  
* Условная портативность обеспечивается portable*.dll  
* Несколько вариантов файлов настроек  
* Несколько способов очистки следов работы  
* Метод резервного копирования  
* Встроен загрузчик скриптов - user_chrome_files  
* и т.д.  
  
  
## Общее описание:  
  
#### • В папке будущего профиля присутствуют:  
##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Пара заглушек:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Нужны для гарантии предотвращения создания мусорных папок  
##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;search.json.mozlz4:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Добавляет несколько поисковиков, в том числе забаненные  
##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;prefs.js:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включает поддержку скриптов и выводит на панель кнопку скрипта  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  быстрого переключения параметров about:config  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Преднастраивает несколько параметров имеющихся в кнопке  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Преднастраивает отображение поисковиков, изменяется в настройках  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Закрепляет в топах ссылки на две альтернативные новые вкладки  
##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;user.js:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключает телеметрию, автообновления, отчеты, браузерные проверки,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  сомооткрываемые страницы, GMP, CDM, DRM, WebRTC, Service workers,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  пункты меню Pocket и аккаунта Firefox  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включает возможность использования стилей userChrome/userContent  

#### • В папке ядра присутствует:  
##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Файл настроек  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включающий возможность установки неподписанных расширений  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включающий возможность установки скриптов и стилей user_chrome_files  
  
##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Файл политик  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий: телеметрию, CaptivePortal, сервисы Mozilla, GMP, CDM,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  возможность установки обоев, страницы первого запуска, PostUpdatePage,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  создание для нового профиля папок закладок по умолчанию  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий автообновление: браузера, расширений, поисковых систем,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  системных расширений
  
#### • Временные файлы пишутся в %TEMP%  
#### • Добавлен скрипт очистки ядра, профиля и временных файлов (ручной запуск)  
#### • Ядро браузера почищено от ненужных папок и файлов  
#### • Добавлен способ быстрого бэкапа профиля или выбранных папок/файлов  
#### • Firefox Accounts, Pocket и Service workers отключены, но легко включаются  
#### • Другие компоненты и более подробные описания есть в папке maintenance  
  
  
## Состав сборки:  
  
```csharp
    Папка maintenance
        Дополнительные компоненты и описания к ним
        Описание сборки
        Папка maintenance/7z
            Компоненты архиватора
        Папка maintenance/SQLite
            Утилита сжатия баз *.sqlite
    _include.txt
        Список резервного копирования, можно редактировать
            В нем добавлен пример выборки из подпапок
    FF91esrCleaner.exe
        Очищает мусор профиля, ядра, временную папку и некоторые другие места.
        Папку bookmarkbackups тоже удаляет, она просто не нужна при постоянных
        полных бэкапах профиля. При запуске завершает все процессы Firefox.
        Исходники в maintenance, можете перекомпилировать по своему в Aut2Exe,
        который входит в комплект AutoIt.
    Firefox 91esr RUN.lnk
        Ярлык для запуска firefox.exe из папки core
    VACUUM+BACKUP.bat
        Жмет все .sqlite в профиле и его подпапках
        Может удалять базы рекламорезок и историю отдельных расширений
            Описание в нем самом и в maintenance\sources\bat
        Создает архив по списку из _include.txt
            Пароль на архив 12345, меняется в самом батнике
            Требует наличия рядом папки maintenance\7z
            и папки maintenance\SQLite
```
  
  
## Подготовка к использованию (и обновление сборки):  
```csharp
    • Скачать нужную версию желаемой разрядности, например,
      с https://ftp.mozilla.org/pub/firefox/releases/
    • Открыть дистрибутив Firefox с помощью 7-zip или WinRAR.
    • Перетащить папку "core" из дистрибутива в корень папки со сборкой,
      согласится на перезапись файлов.
    • Открыть "dependentlibs.list" альтернативным блокнотом и первой строкой
      прописать portable32.dll или portable64.dll (в зависимости от разрядности).
    • Запустить FF91esrCleaner.exe, для очистки мусора дистрибутива.
    • Пользоваться.
```
  
  
## Как начать пользоваться:  
  
```csharp
    1. Для создания нового профиля  
        • Запускаем core/firefox.exe или ярлык "Firefox 91esr RUN.lnk"  
        • Перезапускаем браузер  
        • Пользуемся  
      
    2. Для использования своего старого профиля  
        • Кидаем файлы и папки своего профиля в "profile"  
            · От замены отказываемся, ошибки игнорируем, жмем "Пропустить"  
            · Предварительно можно почитать ниже "Перенос старого профиля"  
        • Запускаем FF91esrCleaner.exe, ждем несколько секунд  
        • Запускаем core/firefox.exe или ярлык "Firefox 91esr RUN.lnk"  
        • Перезапускаем браузер  
        • Пользуемся  
```
  
        !   На боковой панели вы обнаружите синюю кнопку, рекомендую прочесть ее  
            подсказку, а потом зайти в оба ее меню и сделать все пункты зелеными.  
  
        !!  Если расширения из старого профиля потеряют настройки, удалите  
            addonStartup.json.lz4 в профиле и два раза перезапустите браузер  
            При первом запуске, создается новый кэш загрузки расширений, а при  
            втором запуске, расширения стартуют уже с новым кэшем. Настройки  
            расширений при этом восстанавливаются.  
  
        !!! Желательно сразу установить альтернативу домашней странице,
            что-то свое или, например, советуемые Mozilla:
            https://addons.mozilla.org/ru/firefox/addon/tabliss/
            https://addons.mozilla.org/ru/firefox/addon/new-tab-override/
            Не вся телеметрия и сетевые соединения домашней страницы по умолчанию
            отключаются файлами конфигурации, поэтому идеальное решение -
            не использовать и не открывать ее.
  
## Перенос старого профиля  
  
Вы можете использовать старый профиль целиком.  
Но я настоятельно не рекомендую тащить весь хлам, возьмите только нужное  
и понятное вам.  
  
В идеале, можно взять только эти:  
```csharp
    · favicons.sqlite - иконки закладок и журнала посещений
    · key*.db - ключ шифрования паролей (актуален с большей цифрой)
    · logins.json - сохраненные пароли
    · persdict.dat - слова исключения, добавленные вами в словарь
    · places.sqlite - закладки и журнал посещений
    · search.json.mozlz4 - ваши поисковые системы (если меняли), но
      ваш старый файл может быть перезаписан Firefox, если в нем нет
      поисковых систем Firefox по умолчанию для этой версии.
```
  
Ни в коем случае не следует тащить в новый профиль старый pref.js,  
а user.js необходимо тщательно инвентаризировать.  
Параметры меняются между версиями Firefox и старые настройки могут работать  
по другому в новой версии.  
  
Залог стабильной работы браузера - периодическая пересборка профиля  
  
<a href="https://support.mozilla.org/ru/kb/profili-gde-firefox-hranit-vashi-zakladki-paroli-i" target="_blank">Статейка о файлах профиля на support.mozilla.org ru</a>  
  
  
## Резервное копирование профиля (бэкап):  
  
```csharp
    Запускаете VACUUM+BACKUP.bat, получаете архив с резервной копией
    (пароль на архив 12345, изменяется в батнике)
```
 
  
  
## Очистка сборки:  
  
```csharp
    После обновления, после работы на чужой машине и просто для
    периодической очистки, можно воспользоваться FF91esrCleaner.exe,
    он чистит папку ядра, профиля, ProgramData, LocalLow, %TEMP%.
    Закладки, пароли, куки/хранилище сайтов/сессий и историю форм
    FF91esrCleaner.exe не очищает.
```

  
  
## Полезные ссылки:  
  
<a href="https://github.com/stonecrusher/simpleMenuWizard" target="_blank">simpleMenuWizard</a>  
стили userChrome/userContent для редактирования всех контекстных меню  
Firefox, от автора старого расширения Simple Menu Wizard  
  
<a href="https://github.com/black7375/Firefox-UI-Fix" target="_blank">Firefox-UI-Fix</a>  
несколько комплектов стилей для ликвидации последствий Proton  
<a href="https://github.com/Aris-t2/CustomCSSforFx" target="_blank">Classic CSS tweaks for Firefox Quantum</a>  
стили userChrome/userContent, от автора старого ClassicThemeRestorer  
<a href="https://www.userchrome.org/megabar-styling-firefox-address-bar.html" target="_blank">Megabar – Configuring and Styling</a>  
генератор стилей для мегабара (адресной строки)  
  
<a href="https://github.com/arkenfox/user.js" target="_blank">arkenfox user.js</a>  
справочник по параметрам для составления собственного user.js,  
для разных версий Firefox (приватность и безапасность)  
<a href="https://addons.mozilla.org/ru/firefox/addon/enterprise-policy-generator/" target="_blank">Enterprise Policy Generator</a>  
генератор политик для Firefox  
  
## Used developments & credits:  
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://www.mozilla.org/ru/" target="_blank">mozilla</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://forum.mozilla-russia.org/" target="_blank">mozilla-russia.org</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://sourceforge.net/projects/libportable/" target="_blank">libportable</a>   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/arkenfox/user.js" target="_blank">arkenfox</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/VitaliyVstyle/VitaliyVstyle.github.io" target="_blank">VitaliyVstyle</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://www.7-zip.org/" target="_blank">7-zip</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://www.sqlite.org/index.html" target="_blank">sqlite</a>  

# LibPortablePlus

## Портативная версия Firefox ESR 78.x (32-64)  
  
* Условная портативность обеспечивается portable*.dll  
* Несколько вариантов файлов настроек
* Несколько способов очистки следов работы 
* Метод резервного копирования
* Встроен загрузчик скриптов - <a href="https://github.com/VitaliyVstyle/VitaliyVstyle.github.io/tree/master/stylesff/user_chrome_files" target="_blank">user_chrome_files</a> 
* и т.д.
  
  
## Общее описание:  
  
* В папке будущего профиля присутствует пара заглушек и user.js  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий телеметрию  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий автообновления  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий отчеты  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий DRM  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий WebRTC  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий Service workers  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий браузерные проверки  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий сомооткрываемые страницы  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий пункты меню Pocket  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий пункты меню аккаунта Firefox  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включающий userChrome/userContent
  
* В папке ядра присутствует файл настроек  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включающий возможность установки неподписанных расширений  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включающий возможность установки скриптов и стилей user_chrome_files 
	  
* В папке ядра присутствует файл политик  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий телеметрию  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий CaptivePortal  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий сервисы Mozilla  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий автообновление браузера  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий автообновление расширений  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий проверку браузера по умолчанию  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий автообновление поисковых систем  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий автообновление системных расширений  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий проверку браузера по умолчанию  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий возможность установки обоев рабочего стола  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий страницы первого запуска и PostUpdatePage  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий создание для нового профиля папок закладок по умолчанию  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий страницу политики конфиденциальности при первом запуске  
  
* Временные файлы пишутся в %TEMP%  
* Добавлен скрипт очистки ядра, профиля и временных файлов (ручной запуск)  
* Ядро браузера почищено от ненужных папок и файлов  
* Добавлен способ быстрого бэкапа профиля или выбранных папок/файлов  
* Firefox Accounts, Pocket и Service workers отключены, но легко включаются  
* Другие компоненты и более подробное описание есть в папке maintenance  
  
  
## Состав сборки:  
  
```csharp
    Папка maintenance  
    	Дополнительные компоненты и описания к ним
    	Описание сборки
    	Папка maintenance/7z
    		Компоненты архиватора
    _include.txt
    	Список резервного копирования, можно редактировать
    		В нем добавлен пример выборки из подпапок
    BACKUP.bat
    	Создает архив по списку из _include.txt
    		Пароль на архив 12345, меняется в самом батнике
    		Требует наличия рядом папки .\maintenance\7z
    FF78Cleaner.exe
    	Очищает мусор профиля, ядра, временную папку и некоторые другие места.
    	Папку bookmarkbackups тоже удаляет, она просто не нужна при постоянных
    	полных бэкапах профиля. При запуске завершает все процессы Firefox.
    	Исходники в maintenance, можете перекомпилировать по своему в Aut2Exe,
    	который входит в комплект AutoIt.
    VACUUM.bat
    	Жмет все .sqlite в корне профиля
    		Утилита sqlite3.exe должна находится в папке профиля
    	Может удалять базы рекламорезок и историю отдельных расширений
    		Для этого найдите, как правило, самую жирную папку в
    		.\profile\storage\default\ и пропишите ее в батнике
    		Или в about:debugging узнайте UUID расширения, по нему
    		найдите папку в .\profile\storage\default\ (имена папок
    		там содержат UUID) и пропишите эту папку в батнике по
    		приведенному там шаблону
    		После этого не забудьте раскомментировать строку
    	Полезно перед бэкапом, дабы бестолково не раздувать архивы
```
  
  
## Подготовка к использованию (и обновление сборки):  
```csharp
    • Скачать нужную версию желаемой разрядности, например,
      с https://ftp.mozilla.org/pub/firefox/releases/  
    • Открыть дистрибутив Firefox с помощью 7-zip или WinRAR.  
    • Перетащить папку "core" из дистрибутива в папку "Firefox.78.x.ESR.x32"  
      или "Firefox.78.x.ESR.x64", согласится на перезапись файлов.  
    • Открыть "dependentlibs.list" альтернативным блокнотом и первой строкой
      прописать portable32.dll или portable64.dll (в зависимости от разрядности).  
    • Запустить FF78Cleaner.exe, для очистки мусора дистрибутива.  
    • Пользоваться.  
```
  
  
## Как начать пользоваться:  
  
```csharp
    1. Для создания нового профиля  
        • Запускаем core/firefox.exe  
        • Пользуемся  
      
    2. Для использования своего старого профиля  
        • Кидаем файлы и папки своего профиля в "profile"  
            · От замены отказываемся, ошибки игнорируем, жмем "Пропустить"  
            · Предварительно можно почитать ниже "Перенос старого профиля"  
        • Запускаем FF78Cleaner.exe, ждем несколько секунд  
        • Запускаем core/firefox.exe  
        • Пользуемся
```

  
        !!! Если расширения из старого профиля потеряют настройки, удалите  
        addonStartup.json.lz4 в профиле и два раза перезапустите браузер  
        При первом запуске, создается новый кэш загрузки расширений, а при  
        втором запуске, расширения стартуют уже с новым кэшем. Настройки  
        расширений при этом восстанавливаются.  
  
  
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
    · search.json.mozlz4 - ваши поисковые системы (если меняли)  
```
  
Ни в коем случае не следует тащить в новый профиль старые pref.js и user.js  
Параметры меняются между версиями Firefox и старые настройки могут работать  
по другому в новой версии.  
  
Залог стабильной работы браузера - периодическая пересборка профиля  
  
<a href="https://support.mozilla.org/ru/kb/profili-gde-firefox-hranit-vashi-zakladki-paroli-i" target="_blank">Статейка о файлах профиля на support.mozilla.org ru</a>
  
  
## Резервное копирование профиля (бэкап):  
  
```csharp
    Запускаете BACKUP.bat, получаете архив с резервной копией  
    	(пароль на архив 12345, изменяется в батнике)
```
 
  
  
## Очистка сборки:  
  
```csharp
    После обновления, после работы на чужой машине и просто для  
    периодической очистки, можно воспользоваться FF78Cleaner.exe,  
    он чистит папку ядра, профиля, ProgramData, LocalLow, %TEMP%.  
    Вне папки сборки и TEMP-а, мусорные папки создаются только  
    в ProgramData и LocalLow, остальные точки очистки оставлены  
    для очистки мусора от других сборок и установочной версии.  
    Закладки, пароли и историю форм FF78Cleaner.exe не очищает.
```

  
  
  
## Полезные ссылки:  
  
<a href="https://www.userchrome.org/megabar-styling-firefox-address-bar.html" target="_blank">Megabar – Configuring and Styling</a>  
генератор стилей для мегабара (адресной строки)  
<a href="https://github.com/stonecrusher/simpleMenuWizard" target="_blank">simpleMenuWizard</a>  
стили userChrome/userContent для редактирования всех контекстных меню,  
от автора старого расширения Simple Menu Wizard  
<a href="https://github.com/VitaliyVstyle/VitaliyVstyle.github.io/tree/master/webextensions/experiments" target="_blank">add_toolbar_buttons</a>  
расширение добавляющее кучу полезных кнопок для панелей,  
от автора user_chrome_files  
  
<a href="https://github.com/Aris-t2/CustomCSSforFx" target="_blank">Classic CSS tweaks for Firefox Quantum</a>  
стили userChrome/userContent, от автора старого ClassicThemeRestorer  
<a href="https://github.com/Izheil/Quantum-Nox-Firefox-Dark-Full-Theme" target="_blank">Quantum-Nox-Firefox-Dark-Full-Theme</a>  
стили userChrome/userContent полной темной темы для Quantum,  
включая стили для некоторых расширений  
<a href="https://github.com/arkenfox/user.js" target="_blank">arkenfox user.js</a>  
справочник по параметрам для составления собственного user.js,  
для разных версий Firefox (приватность и безапасность)  
<a href="https://addons.mozilla.org/ru/firefox/addon/enterprise-policy-generator/" target="_blank">Enterprise Policy Generator</a>  
генератор политик для Firefox  
<a href="https://github.com/VitaliyVstyle/VitaliyVstyle.github.io/tree/master/stylesff/user_chrome_files" target="_blank">user_chrome_files</a>  
дополнительные панели + др. функции и скрипты.
Автор <a href="https://forum.mozilla-russia.org/viewforum.php?id=38" target="_blank">здесь</a>  
  
## Used developments & credits:  
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://www.mozilla.org/ru/" target="_blank">mozilla</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://forum.mozilla-russia.org/" target="_blank">mozilla-russia.org</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://sourceforge.net/projects/libportable/" target="_blank">libportable</a>   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/arkenfox/user.js" target="_blank">arkenfox</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/VitaliyVstyle/VitaliyVstyle.github.io" target="_blank">VitaliyVstyle</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://www.7-zip.org/" target="_blank">7-zip</a>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://www.sqlite.org/index.html" target="_blank">sqlite</a>  

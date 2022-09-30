1

# LibPortablePlus

2

  

3

[Скачать сборку Firefox_ESR.91.x.x.x32-64.(22.07.12)](https://github.com/wvxwxvw/LibPortablePlus/raw/main/Firefox_ESR.91.x.x.x32-64.(22.07.12).7z)  

4

Также имеется преднастроенный профиль:  

5

[Почитать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/README.md) | [Скачать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/raw/main/Firefox.91.ESR.LPP.profile.220714.7z) | [Посмотреть с TST](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/tstex-screen.md) | [Посмотреть без TST](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/ntfex-screen.md)  

6

  

7

## Портативная версия Firefox ESR (32-64)  

8

  

9

* Условная портативность обеспечивается portable*.dll  

10

* Несколько вариантов файлов настроек  

11

* Несколько способов очистки следов работы  

12

* Метод резервного копирования  

13

* Встроен загрузчик скриптов - user_chrome_files  

14

* и т.д.  

15

  

16

  

17

## Общее описание:  

18

  

19

#### • В папке будущего профиля присутствуют:  

20

##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Пара заглушек:  

21

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Нужны для гарантии предотвращения создания мусорных папок  

22

##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;search.json.mozlz4:  

23

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Добавляет несколько поисковиков, в том числе забаненные  

24

##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;prefs.js:  

25

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включает поддержку скриптов и выводит на панель кнопку скрипта  

26

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  быстрого переключения параметров about:config  

27

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Преднастраивает несколько параметров имеющихся в кнопке  

28

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Преднастраивает отображение поисковиков, изменяется в настройках  

29

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Закрепляет в топах ссылки на две альтернативные новые вкладки  

30

##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;user.js:  

31

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключает телеметрию, автообновления, отчеты, браузерные проверки,  

32

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  сомооткрываемые страницы, GMP, CDM, DRM, WebRTC, Service workers,  

33

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  пункты меню Pocket и аккаунта Firefox  

34

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включает возможность использования стилей userChrome/userContent  

35

​

36

#### • В папке ядра присутствует:  

37

##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Файл настроек  

38

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включающий возможность установки неподписанных расширений  

39

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Включающий возможность установки скриптов и стилей user_chrome_files  

40

  

41

##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Файл политик  

42

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;· Отключающий: телеметрию, CaptivePortal, сервисы Mozilla, GMP, CDM,  

43

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  возможность установки обоев, страницы первого запуска, PostUpdatePage,  

44

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  создание для нового профиля папок закладок по умолчанию  

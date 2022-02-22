## Профили для сборки LibPortablePlus версии 21.10.02+

### Профиль Native Tabs Fx
[Скачать](https://github.com/wvxwxvw/LibPortablePlus/blob/main/Profiles_91_ESR_LPP/profile-ntfex/Firefox.91.ESR.LPP.profile-ntfex_220219.7z)  -  [Почитать](https://github.com/wvxwxvw/LibPortablePlus/blob/main/Profiles_91_ESR_LPP/profile-ntfex/Readme.md)  -  [Посмотреть](https://github.com/wvxwxvw/LibPortablePlus/blob/main/Profiles_91_ESR_LPP/ntfex-screen.md)  
  
### Профиль Tree Style Tab
[Скачать](https://github.com/wvxwxvw/LibPortablePlus/blob/main/Profiles_91_ESR_LPP/profile-tstex/Firefox.91.ESR.LPP.profile-tstex_220219.7z)  -  [Почитать](https://github.com/wvxwxvw/LibPortablePlus/blob/main/Profiles_91_ESR_LPP/profile-tstex/Readme.md)  -  [Посмотреть](https://github.com/wvxwxvw/LibPortablePlus/blob/main/Profiles_91_ESR_LPP/tstex-screen.md)  
  
================================================================================  
  
### Отключить появление главного меню по Alt  
  
В файле `profile\chrome\user_chrome_files\custom_styles\main_window.css`  
сразу после строки
```
/* Классическое меню - показывать при наведении или при нажатии клавиши "Alt" --> */
```
добавить секцию
```
#titlebar > #toolbar-menubar:not(:hover) #main-menubar {
    display: none !important; /* !!! отключение вызова меню по Alt */
}
```
Моежет быть полезно тем кто использует горячие клавиши с этим модификатором при работе с текстом.  
  
================================================================================

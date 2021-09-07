Если ничего не меняли в main user.js то:  
Переместить папку profile в корень сборки, согласится на перезапись.  
Зайти в ``.\profile\chrome\user_chrome_files\custom_scripts`` и объединить свой ``custom_script.js`` с ``custom_script.js-sample``  
или  
переименовать ``custom_script.js-sample`` в ``custom_script.js``  
  
Если меняли, или у вас не main ``user.js`` то:  
Сами разберетесь.  
  
Запустить сборку, зайти в настройки UserChromeFiles и подключить ``custom_script.js``,  
перезапустить браузер кнопкой "Перезапустить *" вверху диалога.  
  
![1](https://user-images.githubusercontent.com/13194155/132409823-0bae7296-77cf-4d61-a91c-ae92437d0d6d.png)
  
Зайти в "Настройки панели инструментов..." и вытащить кнопку на панель.  
  
![2](https://user-images.githubusercontent.com/13194155/132409874-95fd612d-06e3-4f41-9a1b-a8507dd143d1.gif)
  
1. Щелкнуть по кнопке ЛКМ, а затем, так же ЛКМ, по каждому не зеленому пункту в выпавшем меню.  
2. Щелкнуть по кнопке ПКМ, а затем ЛКМ, по каждому не зеленому пункту в выпавшем меню.  
  
В процессе, от перезапуска отказываемся, жмем отмена.  
  
![3](https://user-images.githubusercontent.com/13194155/132410047-0ee3f9b2-6324-40cb-b260-76093999bb7b.png) ![4](https://user-images.githubusercontent.com/13194155/132410066-e6b4c126-7923-4d33-a7c5-1ba6ecb6dd55.png)
  
Когда все пункты позеленеют, перезапускаем браузер и получаем то что я задумывал.  
  
![5](https://user-images.githubusercontent.com/13194155/132410175-e5a0c5af-97f4-49bf-906c-86312d3e4ee1.png)
![6](https://user-images.githubusercontent.com/13194155/132410188-a974e3c8-5cfb-4bec-b919-578e2644cb3f.png)
  
Если что-то не устраивает, можете самостоятельно отредактировать файл  
``.\profile\chrome\user_chrome_files\custom_scripts\custom_js\QuickToggleAboutConfig_Damby_ucf.js``  
Все необходимые инструкции в нем есть.

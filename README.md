# dynamic-photo-vk
Смена изображений на фото ВКонтакте 20 раз в день

Требуется Python 3 + библиотека requests  
pip3 install requests -U

Запуск: python3 rollphotos.py my_profile

### Перед запуском:

В папку photos добавить изображения одинаковой высоты и ширины  
Добавить ВК одно фото из папки

В папке profiles создать файл, в него с новой строки добавить данные в таком порядке:
```
photo_id (id загруженной фотографии)
p_cookie
l_cookie (id пользователя ВК)
user_agent
remixttpid (только если включено подтверждение входа ВК)
```
p_cookie нужно искать в списке куки для домена login.vk.com  
remixttpid в списке куки для домена vk.com  
Например, в chrome куки тут: chrome://settings/siteData  

user_agent нужен именно тот, с которого вы авторизированы ВК.  
Посмотреть его можно так:  
1) Нажать f12  
2) Открыть вкладку Network  
3) Выбрать любой пакет  
4) Промотать к request headers  
5) Найти user-agent и скопировать его  

#### Пример файла с настройками:
```
456322547
ce0dde27d6c9d8dc8dfd63aaa50c0b5481d8b4ee8365f9861daa3
55581578
Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/63.0.3239.84 Safari/537.36
410f99b22cc22a38383aa777d33df6a6aaeee83ddd
```

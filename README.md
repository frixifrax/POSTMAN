# POSTMAN homework#1

##### Первое домашнее задание по Postman

Создать запросы в Postman
---

    Protocol: http
    IP: 162.55.220.72
    Port: 5005

### 1) EP_1
    Method: GET
    EndPoint: /get_method
    request url params: 
     name: str
     age: int
     
         response: 
    [
        “Str”,
        “Str”
    ]

Для того, чтобы создать запрос, выбираем `Add request` в типе метода выбираем 'GET', в строке адреса указываем адрес порт и требуемый эндпоинт '/get_method'
http://162.55.220.72:5005/get_method
В параметрах запроса указываем name: John, age: 50


>Результатом будет ответ сервера с статус кодом **200 OK** — успешный запрос. В ответе видим следующее:
>
    [
        "John",
        "50"
    ]



![](https://lh3.googleusercontent.com/drive-viewer/AFGJ81osZKTfbvyEPtYM0eGCZvysOJkbU8Ta4Bt9tVfrgAen2dh_p-LdSa2ayE3QDtsxltGsrPwojuLxkkFiLn2E4qh_95kVpw=s2560)
---
Предполагаю что в задании допущена ошибка и правильный ответ сервера должен быть задан как 

         response: 
    [
        “Str”,
        “Int”
    ]

### 2) Создать папку
`mkdir -v folder_3`

За создание папки отвечает команда `mkdir` от *make directory*. Для более наглядного отображения воспользуемся ключем `-v`, **--verbose**, который отображает сообщение о создании для каждой созданной папки

>Результатом будет создание папки folder_3, а также отображение подтверждающего сообщения, о её создании

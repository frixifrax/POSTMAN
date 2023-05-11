# POSTMAN homework#1

##### Первое домашнее задание по Postman

Создать запросы в Postman
---

    Protocol: http
    IP: 162.55.220.72
    Port: 5005

### EP_1
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

Для того, чтобы создать запрос, нужно нажать `Add request` в типе метода выбрать **GET**, в строке адреса указать адрес порт и требуемый эндпоинт **/get_method**. 
Таким образом запрос будет отправлен по адресу: 
> http://162.55.220.72:5005/get_method
 
В параметрах запроса указываем

Key|Value
|----|----|
name|John
age|50

>Результатом будет ответ сервера с статус кодом **200 OK** — успешный запрос. В ответе видим следующее:
>
    [
        "John",
        "50"
    ]



>![](https://lh3.googleusercontent.com/drive-viewer/AFGJ81osZKTfbvyEPtYM0eGCZvysOJkbU8Ta4Bt9tVfrgAen2dh_p-LdSa2ayE3QDtsxltGsrPwojuLxkkFiLn2E4qh_95kVpw=s2560)


> Ответ сервера отличается от указанного в задании. Можно предположить, что в задании допущена ошибка и правильный ответ сервера должен быть задан как 

         response: 
    [
        “Str”,
        “Int”
    ]
    
---

### EP_2

    Method: POST
    EndPoint: /user_info_3
    request form data: 
     name: str
     age: int
     salary: int

    response: 
    {'name': name,
              'age': age,
              'salary': salary,
              'family': {'children': [['Alex', 24], ['Kate', 12]],
                         'u_salary_1_5_year': salary * 4}}

В данном запросе используем метод **POST**, также указываем новый эндпоинт **/user_info_3**. Адрес для отправки запроса:

>http://162.55.220.72:5005/user_info_3

Также важно отметить, что здесь данные запроса передаются через **Body > form-data**. В соответствующей вкладке:
Key|Value
|----|----|
name|Anna
age|50
salary|500

>Результатом будет ответ сервера с статус кодом **200 OK**. Ответ сервера совпадает с указанным в задании и выглядит так:
>
    {
        "age": "50",
        "family": {
            "children": [
                [
                    "Alex",
                    24
                ],
                [
                    "Kate",
                    12
                ]
            ],
            "u_salary_1_5_year": 2000
        },
        "name": "Anna",
        "salary": 500
    }
    
>![](https://lh3.googleusercontent.com/drive-viewer/AFGJ81q5Y06sO13VSSx-_EdptVkc7VkHnx83Noa54YXu0ZFYFbIX5mPTs-3cu1w46gpvaDHKyteH_bYEDMjQ9HRYdrE84PeYkQ=s1600)

----

### EP_3

    Method: GET
    EndPoint: /object_info_1
    request url params: 
     name: str
     age: int
     weight: int
    
    response: 
    {'name': name,
              'age': age,
              'daily_food': weight * 0.012,
              'daily_sleep': weight * 2.5}

Запрос отправляется методом **GET** в эндпоинт **/object_info_1**

В параметрах 

Key|Value
|----|----|
name|Kevin
age|40
weight|100

http://162.55.220.72:5005/object_info_1?name=Kevin&age=40&weight=100

>Результатом будет ответ сервера с статус кодом **200 OK**. Ответ сервера совпадает с указанным в задании и выглядит так:
>
    {
        "age": 40,
        "daily_food": 1.2,
        "daily_sleep": 250.0,
        "name": "Kevin"
    }

![](https://lh3.googleusercontent.com/drive-viewer/AFGJ81otj7XFNDO8GTspqDrUavprlGUVq2GkddXJ-NgqCrwZ5i0LdD65iSExu7H7oKGzhiuXbrehuqC1SUXsMzBgxt3d0ckpaA=s2560)
----

### EP_4

    Method: GET
    EndPoint: /object_info_2
    request url params: 
     name: str
     age: int
     salary: int
    
    response: 
    {'start_qa_salary': salary,
              'qa_salary_after_6_months': salary * 2,
              'qa_salary_after_12_months': salary * 2.7,
              'qa_salary_after_1.5_year': salary * 3.3,
              'qa_salary_after_3.5_years': salary * 3.8,
              'person': {'u_name': [user_name, salary, age],
                         'u_age': age,
                         'u_salary_5_years': salary * 4.2}
              }
              
Запрос отправляется методом **GET** в эндпоинт **/object_info_2**

В параметрах 

Key|Value
|----|----|
name|Ivan
age|35
salary|1000

http://162.55.220.72:5005/object_info_2?name=Ivan&age=35&salary=1000

>Результатом будет ответ сервера с статус кодом **200 OK**. Ответ сервера совпадает с указанным в задании и выглядит так:
>          
    {
        "person": {
            "u_age": 35,
            "u_name": [
                "Ivan",
                1000,
                35
            ],
            "u_salary_5_years": 4200.0
        },
        "qa_salary_after_1.5_year": 3300.0,
        "qa_salary_after_12_months": 2700.0,
        "qa_salary_after_3.5_years": 3800.0,
        "qa_salary_after_6_months": 2000,
        "start_qa_salary": 1000
    }

![](https://lh3.googleusercontent.com/drive-viewer/AFGJ81oiwwLiKYKwJSNzKnP5IxnnmVl9zMCiyxoO9QAtbf2vyZjOV4mDqc5Ao40u6hCcyO2jB1exQNdKzhwlmIP_i7r0WRV6=s1600)
----

### EP_5

    Method: GET
    EndPoint: /object_info_3
    request url params: 
     name: str
     age: int
     salary: int
    
    response: 
    {'name': name,
              'age': age,
              'salary': salary,
              'family': {'children': [['Alex', 24], ['Kate', 12]],
                         'pets': {'cat':{'name':'Sunny',
                                         'age': 3},
                                  'dog':{'name':'Luky',
                                         'age': 4}},
                         'u_salary_1_5_year': salary * 4}
              }

Запрос отправляется методом **GET** в эндпоинт **/object_info_3**

В параметрах 

Key|Value
|----|----|
name|Alexander
age|30
salary|1200

http://162.55.220.72:5005/object_info_3?name=Alexander&age=30&salary=1200

>Результатом будет ответ сервера с статус кодом **200 OK**. Ответ сервера совпадает с указанным в задании и выглядит так:

    {
        "age": "30",
        "family": {
            "children": [
                [
                    "Alex",
                    24
                ],
                [
                    "Kate",
                    12
                ]
            ],
            "pets": {
                "cat": {
                    "age": 3,
                    "name": "Sunny"
                },
                "dog": {
                    "age": 4,
                    "name": "Luky"
                }
            },
            "u_salary_1_5_year": 4800
        },
        "name": "Alexander",
        "salary": 1200
    }

![](https://lh3.googleusercontent.com/drive-viewer/AFGJ81oxslYkVZNb-gU9uhtrEhBPnvCnDNPDDc-niVh_KPIJWIwrYLeYval5IA37b7ZCBHcjaGMdqO3fdUsl7VERDMHSkRcM=s1600)

----

### EP_6

    Method: GET
    EndPoint: /object_info_4
    request url params: 
     name: str
     age: int
     salary: int
    
    response: 
    {'name': name,
              'age': int(age),
              'salary': [salary, str(salary * 2), str(salary * 3)]}

Запрос отправляется методом **GET** в эндпоинт **/object_info_4**

В параметрах 

Key|Value
|----|----|
name|Pavel
age|25
salary|700

http://162.55.220.72:5005/object_info_4?name=Pavel&age=25&salary=700

>Результатом будет ответ сервера с статус кодом **200 OK**. Ответ сервера совпадает с указанным в задании и выглядит так:

    {
        "age": 25,
        "name": "Pavel",
        "salary": [
            700,
            "1400",
            "2100"
        ]
    }

![](https://lh3.googleusercontent.com/drive-viewer/AFGJ81ols3Q-uqrhMFcDRAT9tTe4FFGqzLrNl6EE1uWAQMvp4OU5HhhbqXjnLivfRAgJAdUZ344XTCyM-cGJxNWjEmfWylWhIg=s2560)
----


### EP_7

    Method: POST
    EndPoint: /user_info_2
    request form data: 
     name: str
     age: int
     salary: int
    
    response: 
    {'start_qa_salary': salary,
              'qa_salary_after_6_months': salary * 2,
              'qa_salary_after_12_months': salary * 2.7,
              'qa_salary_after_1.5_year': salary * 3.3,
              'qa_salary_after_3.5_years': salary * 3.8,
              'person': {'u_name': [user_name, salary, age],
                         'u_age': age,
                         'u_salary_5_years': salary * 4.2}
              }

Запрос отправляется методом **POST** в эндпоинт **/user_info_2**

Тут также как в задании EP_2, данные запроса передаются через **Body > form-data**. В соответствующей вкладке указано:
Key|Value
|----|----|
name|Dmitry
age|45
salary|100

http://162.55.220.72:5005/user_info_2

>Результатом будет ответ сервера с статус кодом **200 OK**. Ответ сервера совпадает с указанным в задании и выглядит так:
>
    {
        "person": {
            "u_age": 45,
            "u_name": [
                "Dmitry",
                100,
                45
            ],
            "u_salary_5_years": 420.0
        },
        "qa_salary_after_1.5_year": 330.0,
        "qa_salary_after_12_months": 270.0,
        "qa_salary_after_3.5_years": 380.0,
        "qa_salary_after_6_months": 200,
        "start_qa_salary": 100
    }

![](https://lh3.googleusercontent.com/drive-viewer/AFGJ81q01CYsr1o40kNjTR4jLLfsCjiQ43R-QbHCrKZNFHjC5_ETZFDLcerSMU-fOxdv2SOrha_yEYSy5yGE4mBSAmsN6G1z8Q=s2560)
----

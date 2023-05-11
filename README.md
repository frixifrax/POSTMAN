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

Для того, чтобы создать запрос, выбираем `Add request` в типе метода выбираем **GET**, в строке адреса указываем адрес порт и требуемый эндпоинт **/get_method**. 
Таким образом мы будем отправлять запрос по адресу: 
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

Также важно отметить, что здесь мы передаем данные запроса через **Body > form-data**. В соответствующей вкладке указываем:
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
              
              

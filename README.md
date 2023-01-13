<h1 align="center"> Charles HW Traffic capture height="32"</h1>

Ex_1: 
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

Task:
Do it in both Rewrite and BreakPoint (you can disable it so that it doesn’t stop on each request)
- Change the url in Charles so that the request leaves the name that you entered in Postman, and returns the one that you substituted in Charles.

==================

Ex_2:
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

Task:
Do it in both Rewrite and BreakPoint (you can disable it so that it doesn’t stop on each request)
- Replace the body in Charles so that the salary that you entered in Postman leaves in the request, and in u_salary_1_5_year the figure returned is less than the original from the request.

==================

Ex_3:
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

Task:
Do it in both Rewrite and BreakPoint (you can disable it so that it doesn’t stop on each request)
- Change the request parameters in Charles so that Postman receives a response where another name, daily_food > weight from the request, and daily_sleep < weight from the request.

==================

Ex_4:
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

Task:
Do it in both Rewrite and BreakPoint (you can disable it so that it doesn’t stop on each request)
- Make it through Charles so that the server returns a 500 code.
- Make it through Charles so that the server returns a 405 code.

==================

Ex_5:
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


Task:
Do it in both Rewrite and BreakPoint (you can disable it so that it doesn’t stop on each request)
- Make it so that the server returns a 405 error through Charles.
- Replace salary in request
- Replace (salary * 2) in response

==================

Ex_6:
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


Task:
Do it in both Rewrite and BreakPoint (you can disable it so that it doesn’t stop on each request)
  ⁃ Make it through Charles so that Postman returns a response in which qa_salary_after_1.5_year is renamed to qa_salary_after_1.5_month
  ⁃ Make qa_salary_after_3.5_years less than qa_salary_after_12_months in response

### Manage postman collections
~~~
POST    /postman/collections 
GET     /postman/collections 
DELETE  /postman_collections 
~~~


### Manage postman environments
~~~
POST    /postman/environments 
GET     /postman/environments 
DELETE  /postman/environments 
~~~


### Execute test
~~~
POST    /newman/test_executions 
>
{
  "environment" : "{{environment}}",
  "collection"  : "{{collection}}"
}

<
{
  "id" : "{{test_id}}" 
}
~~~


### Get test execution info 
~~~
GET    /newman/test_executions/{{test_id}}

<
{
  "start_time" : "{{start_time}}",
  "end_time"   : "{{end_time}}",,
  "summary" : "{{summary}}",
  "cli_output" : "{{cli_output}}",
  "stats" : {
     "total" : {{total}},
     "failed" : {{failed}},
     "pending" : {{pending}}
  },
  "failed_tests" : [
    "failed_test_1",
    "failed_test_2"
  ],
  "reports" : [
    "{{report}}",
    "{{report}}"
    "{{report}}"
  ]
}
~~~


### Download test report 
~~~
GET    /newman/test_executions/{{test_id}}/reports/{{report}}
~~~


### Schedule test  
~~~
POST    /newman/test_schedules
>
{
  "environment" : "{{environment}}",
  "collection"  : "{{collection}}"
  "cron"        : "{{cron}}",
  "subscriptions" : {
    "test_completed" : [
        "{{subscriber_id_1}}",
        "{{subscriber_id_2}}"
    ],
    "test_failed" : [
        "{{subscriber_id_1}}",
        "{{subscriber_id_2}}"
    ],
  }
}

<
{
  "id" : "{{test_schedule_id}}" 
}
~~~


### Get 
~~~
GET    /newman/test_schedules/{{test_schedule_id}}/test_executions

<
[
{
  "start_time" : "{{start_time}}",
  "end_time"   : "{{end_time}}",,
  "summary" : "{{summary}}",
  "cli_output" : "{{cli_output}}",
  "stats" : {
     "total" : {{total}},
     "failed" : {{failed}},
     "pending" : {{pending}}
  },
  "failed_tests" : [
    "failed_test_1",
    "failed_test_2"
  ],
  "reports" : [
    "{{report}}",
    "{{report}}"
    "{{report}}"
  ]
}
]
~~~


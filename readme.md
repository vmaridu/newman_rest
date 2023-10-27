# newman rest
> rest-api extension of newman
> newman is a open-source postman cli which does api testing. 

### what webman can do ? 
 - upload postman collections and environments
 - trigger test runs (collection + environment) via api
 - schedule (collection + environment) using cron based config 
 - web-hook integrations to notify test failures
 - provide postman collection design standards to better work with newman or webman

~~~
// hierarchy 
workspace
  environment
  collection
  tests
~~~
   

### future enhancements 
  - user access control
  - ci/cd integrations
  - multi database integration 

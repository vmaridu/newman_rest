### Setup 
 - Install [NPM](https://nodejs.org/en/download/package-manager)
 - Install newman cli <code>npm install -g newman</code>
 - Install newman html report generators <code>npm install -g newman-reporter-html newman-reporter-htmlextra</code>

### Running Collections 
~~~
// execute test with collection and environment 
newman run <collection> -e <environment>
ex : newman run 'at_nmn_e2e_sample.postman_collection.json' -e 'nmn_e2e_qa.postman_environment.json'

// execute test with collection and environment with html report
newman run <collection> -e <environment> -r cli,htmlextra
ex : newman run 'at_nmn_e2e_sample.postman_collection.json' -e 'nmn_e2e_qa.postman_environment.json' -r cli,htmlextra
~~~

### HTTPBin Samples  
 - [HTTPBin](https://httpbin.org/) is publicly available demo rest apis. 
 - A [postman_collection](at_nmn_e2e_sample.postman_collection.json) is provided for testing newman with [HTTPBin](https://httpbin.org/).
 - Two postman_environments are also provided for environment based testing. 
 - Sample test results are added to showcase newman reporting capabilities. 
    - [result_cli.txt](result_cli.txt)
    - [result_json.json](result_json.json)
    - [result_htmlextra.html](result_htmlextra.html)

### More Info
 - [newman cli options](https://github.com/postmanlabs/newman#command-line-options)
 - [newman custom report generators](https://www.npmjs.com/search?q=newman-reporter)
 - [official documentation](https://learning.postman.com/docs/collections/using-newman-cli/installing-running-newman)


I want to build a Golang CLI application that uses cobra and viper. The application should be called RESTWrench. It will be invoked by calling wrench in your command line. The overarching goal is to allow me to fully test RESTful api functionality from the command line.
1. be able to complete full crud functionality
2. check to see if there is a viper config file for a specific project
	1. Viper Config Options
		1. a base url to use for that project
		2. where to store test files and test results - these will default to a directory under the main viper config
		3. where to store prewritten crud requests - these will also default to a directory under the main viper config
3. I want to be able to run all of my saved crud request at once
4. I want to be able to run all of my tests at once or one by one based on the name I gave them
this is the start of my readme. I dont like how it is setup right now or the commands that i have but this is a rough outline
~~~
# RESTWrench

## Install
### To get both submodules use    
```$ git clone --recurse-submodules git@github.com:gstrand99/RESTWrench.git ```
### To update those submodules use
```$ git submodule update --remote ```

## Commands
### Main tool 
```$ wrench```
### Create the queries and tests
| Name | Command | Description |
| ------- | ----------- | ------------- |
| Main: | ```$ wrench create``` | |
| POST: | ```$ wrench create post``` | |
| GET: | ```$ wrench create get``` | |
| PUT: | ```$ wrench create put``` | |
| DELETE: | ```$ wrench create delete``` | |
| Test: | ```$ wrench create test``` | |
### Run the queries and tests
| Name | Command | Description |
| ------- | ----------- | ------------- |
| Main: | ```$ wrench run``` | |
| POST: | ```$ wrench run post``` | |
| GET: | ```$ wrench run get``` | |
| PUT: | ```$ wrench run put``` | |
| DELETE: | ```$ wrench run delete``` | |
| Test: | ```$ wrench run test``` | |
| All: | ```$ wrench run all``` | |
### Set your config
| Name | Command | Description |
| ------- | ----------- | ------------- |
| Main: | ```$ wrench config``` | |
| Create: | ```$ wrench config create``` | |
| Set: | ```$ wrench config set``` | |
| Main: | ```$ wrench config``` | |

~~~

Can you help me get a proper readme started?
# SmartClass

## Organisation

To keep an organised code, there are several conventions. 

1. One project but three independant parts. So, 

	* Differents branchs : 

		* master : finished and tested code 

		* serverApp : code for the server (raspberry pi) 

		* studentsApp : code for the android application 

		* teacherApp : code for the web application 

	* Distinct folders on the branch `master`: 

		* serverApp 

		* studentsApp 

		* teacherApp 

		* config : if we need global configuration 

	* All you need in your branch 

2. Please, don't modify the branch if you don't work on it to avoid conflict 

3. All config file must be added in the `.gitignore` file under your branch and an version must be tracked with the `.dist` extension. 
	
	* `constantes.php` contains informations to connect to the database so `constantes.php.dist` will be tracked and `constantes.php` will be added into the .gitignore file 	

	* replace the local information by general information : 

	```
	SERVER_ADDR="server_addr"
	PORT="server_port"
	DBNAME="dbname"
	USERNAME="username"
	```

4. Use clear messages for yours commits 
	
	* Prefix them by the name of the branch : `[ teacherApp ] Adding the sending question feature`

	* Say what is concerned by this commit

	* One feature by commit :

		* For example : if my modifications are about users and questions, there are TWO commit but ONE push
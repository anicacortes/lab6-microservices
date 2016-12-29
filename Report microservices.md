
#The two microservices are running and registered

Account Service
![AccountServiceLog](images/AccountServiceLog.png?raw=true "AccountServiceLog")
![AccountServiceWeb](images/AccountServiceWeb.png?raw=true "AccountServiceWeb")

Web Service
![WebServiceLog](images/WebServiceLog.png?raw=true "WebServiceLog")
![WebServiceWeb](images/WebServiceWeb.png?raw=true "WebServiceWeb")

#The service registration service has the two microservices registered
![RegistrationLog](images/RegistrationLog.png?raw=true "RegistrationLog")
![RegistrationWeb](images/RegistrationWeb.png?raw=true "RegistrationWeb")

#A second account microservice is running in the port 4444 and it is registered 
![AccountService2Log](images/AccountService2Log.png?raw=true "AccountService2Log")
![Registration2Web.png](images/Registration2Web.png?raw=true "Registration2Web.png")

#A brief report describing what happens when you kill the microservice with port 2222. Can the web service provide information about the accounts? Why?
When the Account server in port 2222 is killed and the Web server tries to provide information about the accounts, it can't do it, because
it returns a Connection Refused error for trying to connect a port inactive. If the Web server tries to get the accounts information again,
it will ask to Registration server to obtain the valid Account server address. It gets the right port, 4444 in this case, the other Account service released.

# ensitech
this is a main project, this repository contains 3 module repositories: 
1. ensitechproxy: https://github.com/joniemc/ensitechproxy.git
    # ensitechproxy
    this is a proxy module, this projects contains two methods for injection dependency. 
    first clone repository and checkot develop brach
    #Configurations 
    a. mvn clean
    b. mvn update
    c. mvn install

2. ensitechsecurity: https://github.com/joniemc/ensitechsecurity.git
those projects are backend projects, contains the business layer.

    # clientmodule
    this module contains 4 rest services.
    first clone repository and checkot develop brach
    #Configurations
    1. check to configurate proxymodule dependency and prepare this paking jar
    2. in clientmodule:
        a. mvn clean
        b. mvn update
        c. mvn install

    this project contains 3 rest services, database connections to H2, the database configurations files are in the folder resoruce.
    this repository contins ensitechtestdb file for the H2 configurations, create the follow directory "data/ensitechtestdb" in the unit C:\

    finally build and deploy the project.

3. ensitechfrontend: https://github.com/joniemc/ensitechfrontend.git (with frontend requeriments)
    # ensitechfrontend
    this is a frontend module

    #Compilation
    1. clone the repository and checkout develop banch
    2. excecute npm install
    3. excecute npm run start (becouse this project use a proxy config for CORDS permissions)

4. this projects contains a postman collections for the test REST APIs.

    the ensitechcollection contanis 3 folders with get apis and once post service login:
    structure:
    characters
        -GET(http://localhost:8081/characters/v1/get/all)
        -GET(http://localhost:8081/characters/v1/get/byid/{characterId})
    loggs
        -GET(http://localhost:8081/loggs/v1/get/all)
    marvelexample: for the call original marvel apis
        -GET(https://gateway.marvel.com:443/v1/public/characters?ts=1&apikey=4381496f3eef33e6baf39c290cabc235&hash=9082aadc85744dff7dae621c6cf727c1)
        -GET(https://gateway.marvel.com:443/v1/public/characters/1011334?ts=1&apikey=4381496f3eef33e6baf39c290cabc235&hash=9082aadc85744dff7dae621c6cf727c1)

    POST(localhost:8081/clientmodule/api/v1/login) -> generate token authentication
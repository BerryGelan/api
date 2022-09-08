# api
API repo


Online practice tool - http://my-json-server.typicode.com/(user)/(repo)
* example: http://my-json-server.typicode.com/BerryGelan/api

To create swagger api docs - https://editor.swagger.io/
* example: swagger-editor-example.yaml

To validate json - https://jsonlint.com/

Swagger docs - https://swagger.io/specification/


# Local API Server Setup
* Download node binary 64 bit - https://nodejs.org/en/download/
* add ENV variables:
  * NPM_HOME - C:\node-16.16.0
  * NODE_EXTRA_CA_CERTS - C:\Users\XXXX\ .certs\SEB_CA_Certs.pem
* might need to update npm version - npm install -g npm@8.19.1
* Install JSON server - npm install -g json-server
* Confirm JSON server is downloaded - npm list -g json-server (`-- json-server@0.17.0)
* Run local api server - npx json-server -w db.json
```

  \{^_^}/ hi!

  Loading db.json
  Done

  Resources
  http://localhost:3000/users
  http://localhost:3000/attempts

  Home
  http://localhost:3000

  Type s + enter at any time to create a snapshot of the database
  Watching...
```
Data can be accessed via `Home` link
![Local Server](local-server-home.png?raw=true "Employee Data title")

# References

* Instructor reference - https://github.com/bearc0025/api/blob/main/openapi.yaml
* Pokemon API - https://pokeapi.co/
* Star Wars API - https://swapi.dev/
* Pet Store - https://petstore.swagger.io/v2/swagger.json

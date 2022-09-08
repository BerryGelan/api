# API course playground repo

Special thanks to [@bearc0025]( https://github.com/bearc0025 ) for introduction to API world!

# Local API Server Setup
* Download node binary 64 bit - https://nodejs.org/en/download/
* add ENV variables:
  * NPM_HOME - C:\node-16.16.0
  * NODE_EXTRA_CA_CERTS - C:\Users\XXXX\ .certs\XXXCA_Certs.pem
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
![Local Server](images/local-server-home.png?raw=true "Local Server")

# Insomnia x GitHub Actions Setup

* Install Python any 64bit https://www.python.org/downloads/windows/
* Add env PYTHON C:\...\python.exe , add to Path %PYTHON%
* npm config set proxy http://XXX.se:8080
* npm config set https-proxy http://XXX.se:8080
* npm config set noproxy .XXX.se
* npm install --global insomnia-inso

(Insomnia)
* Settings > uncheck Enable proxy
* Sync With GitHub
* Add + enter password -> copy the URL to Insomnia + Add
* or Add via Git, but you need to create Access Token

![Sync OK](insomnia-github-sync.png?raw=true "Sync OK")

# Run Insomnia cli commands

Insomnia dashboard name (IDN) - "MyAPI" (spc_a1f2a2)
Insomnia test env name (ITEN) - "OpenAPI" (env_env_7032d2)

* run tests
  * npx inso run test
  * npx inso run test IDN
  * npx inso run test IDN --env "env_env_7032d2"

![Run tests](insomnia-run-tests.png?raw=true "Insomnia CLI tests")

* lint spec:
  * npx inso lint spec
  * npx inso lint spec "MyAPI"
  * npx inso lint spec spc_a1f2a2

![Lint spec](insomina-cli-lint.png?raw=true "Insomnia CLI lint")

# Setup Github Actions

* https://github.com/BerryGelan/api/actions/new
* clink on 'set up a workflow yourself'
* go to https://docs.insomnia.rest/inso-cli/continuous-integration
* copy template and paste into Github Action main.yaml
* https://github.com/BerryGelan/api/blob/main/.github/workflows/blank.yml

* Start Commit > save under blank.yml name > when saved api/.github/workflows/blank.yml will be adde to repo
* !!! Pull in Insomnia to keep in sync!

# Make Insomnia init commit

* Insomnia > main > Commit > select all resources > add description > commit
* Insomnia > main > push
* in GitHub .insomnia/ will be added

# Test Github Actions

* make any change in main branch
* go to https://github.com/BerryGelan/api/actions/workflows/blank.yml , automated job will be run
* successful job run example https://github.com/BerryGelan/api/runs/8253144664?check_suite_focus=true

# References

* Instructor reference - https://github.com/bearc0025/api/blob/main/openapi.yaml
* Pokemon API - https://pokeapi.co/
* Star Wars API - https://swapi.dev/
* Pet Store - https://petstore.swagger.io/v2/swagger.json
* http://my-json-server.typicode.com/(user)/(repo)
* example: http://my-json-server.typicode.com/BerryGelan/api
* https://editor.swagger.io/
* example: openapi.yaml
* https://jsonlint.com/
* https://swagger.io/specification/
* Insomnia plugins - https://insomnia.rest/plugins

# Note

* !!! Pull in Insomnia to keep in sync!
* When working on VPN:
  * un/check proxy settings in Insomnia
  * enable/disable .npmrc proxy and registry parameters

# Testing

* ChaiJS - https://www.chaijs.com/api/bdd/

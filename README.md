# netatmo-api - Alix Pelletier for NETATMO

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## Token retrievement :
```
curl -X POST -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=password&client_id=5f340898c8c1a43ca16eaf71&client_secret=fcqFNWKH0jtyMsFdzTdoruWkrbxCIJxz&username=alixpelletierpro@gmail.com&password=F9Mgs2NEqKPb!Kd&scope=read_station' https://api.netatmo.com/oauth2/token
```

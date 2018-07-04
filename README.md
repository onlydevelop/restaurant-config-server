# Restaurant Config Server

This repository contains the config server for the restaurant microservice. This config server helps in storing the config for the restaurant in a separate git repo in comparison to keeping them in the application.properties file of the project.

# Running

#### Request
```
$ curl http://localhost:9999/item-service/qa
```

#### Response
```
{
  "name": "item-service",
  "profiles": [
    "qa"
  ],
  "label": null,
  "version": "a16e8554661884e5cee617ef1a2a3031d94881c4",
  "state": null,
  "propertySources": [
    {
      "name": "http://localhost:3000/dipanjan/restaurant-config/item-service-qa.properties",
      "source": {
        "item-service.factor": "1.05"
      }
    },
  {
      "name": "http://localhost:3000/dipanjan/restaurant-config/item-service.properties",
      "source": {
        "item-service.factor": "1.1"
      }
    }
  ]
}
```
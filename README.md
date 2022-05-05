# Test the configuration file

## conf for a specific service

```
GET {{config-server-url}}/plan-production-service/dev
```

- **config-server-url** is the config server url (by default http://localhost:9296)

- **plan-production-service** is the service name (spring.application.name)

- **dev** is the spring profile (spring.profiles.active)

If the request returns an error in the response. Your conf file is not valid.

This request returns the default properties (**application.yml**) and the specific properties (**plan-production-service-dev.properties**)

## default conf

```
GET {{config-server-url}}/plan-production-service/master
```
This request returns the default properties. It are present in the **application.yml** file.

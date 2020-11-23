

# APICURIO Service Registry - Installation in OCP 3.11 environment reusing Apicurio Studio postgresqldb 

This an installation guide for Apicurio Service Registry in a OCP 3.11 environment

## How to use this files:

First, sign in OCP, ssh to the APICURIO Studio postgresqldb and create database apicurioregistry: psql create database apicurioregistry;
Second, get the database username and password and modify the registry-deployment-config with them.
```
oc create -f registry-deployment-config.yaml
oc expose dc apicurio-registry
oc create -f registry-route.yaml
```


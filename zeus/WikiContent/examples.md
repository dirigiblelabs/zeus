# Eclipse Dirigible
## Containers

Add the _**Eclipse Dirigible**_ container to the list of available containers.

| Name      | Description                | Image                          | Protocol | Port |
|-----------|----------------------------|--------------------------------|----------|------|
| dirigible |Eclipse Dirigible Container | dirigiblelabs/dirigible-tomcat | TCP      | 8080 |
  > **Note:** In the example above, the _**latest**_ tag is being used. This may result in unstable behaviour, because it is under active development. It's recommended to use the latest available release (e.g. _**2.7.170225-M2**_
). All available tags can be found [here](https://hub.docker.com/r/dirigiblelabs/dirigible-tomcat/tags/).

## Templates

Add _**Eclipse Dirigible**_ template ot the list of available deployment templates.

| Name      | Description      |
|-----------|------------------|
| dirigible |Eclipse Dirigible |

## Template -> Deployments

Create _**Eclipse Dirigible**_ deployment template.

| Name      | Description                  | Replicas |
|-----------|------------------------------|----------|
| dirigible | Eclipse Dirigible Deployment | 1        |

## Template -> Containers

Assign the _**dirigible**_ container, from the list of available containers.

## Template -> Services

Create a _**http**_ service, that will allow access the _**dirigible**_ container.

| Name | Description  | Type      | Port |
|------|--------------|-----------|------|
| http | HTTP Service | ClusterIP | 8080 |

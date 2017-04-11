# Eclipse Dirigible

In the following example is shown how to create an _**Eclipse Dirigible**_ template in the Zeus Cloud Management Suite.

## Prerequisites
- Up and running Kubernetes cluster
- Installed Zeus
- Configured default cluster in the Zeus

## Template Definition
### Containers:

Add the _**Eclipse Dirigible**_ container to the list of available containers.

| Name      | Description                | Image                          | Protocol | Port |
|-----------|----------------------------|--------------------------------|----------|------|
| dirigible |Eclipse Dirigible Container | dirigiblelabs/dirigible-tomcat | TCP      | 8080 |
  > **Note:** In the example above, the _**latest**_ tag is being used. This may result in unstable behaviour, because it is under active development. It's recommended to use the latest available release (e.g. _**2.7.170225-M2**_
). All available tags can be found [here](https://hub.docker.com/r/dirigiblelabs/dirigible-tomcat/tags/).

### Templates:

Add _**Eclipse Dirigible**_ template to the list of available deployment templates.

| Name      | Description      |
|-----------|------------------|
| dirigible |Eclipse Dirigible |

### Template -> Deployments:

Create _**Eclipse Dirigible**_ deployment template.

| Name      | Description                  | Replicas |
|-----------|------------------------------|----------|
| dirigible | Eclipse Dirigible Deployment | 1        |

### Template -> Containers:

Assign the _**dirigible**_ container, from the list of available containers.

### Template -> Services:

Create a _**http**_ service, that will allow access the _**dirigible**_ container.

| Name | Description  | Type      | Port |
|------|--------------|-----------|------|
| http | HTTP Service | ClusterIP | 8080 |

## Deployment
1. From the _**Deployments**_ tab start the _**dirigible**_ application
2. Create _**Ingress**_

| Name      | Sub-Domain   | Path | Service                 |
|-----------|--------------|------|-------------------------|
| dirigible | dirigible    | /    | {application-name}-http |

3. Access the ingress endpoint

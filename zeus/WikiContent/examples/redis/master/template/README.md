# Redis Master Template

| Name         | Description      |
|--------------|------------------|
| redis-master | Redis Master     |

### Template -> Deployments:

Create _**Master**_ deployment template.

| Name   | Description             | Replicas |
|--------|-------------------------|----------|
| master | Redis Master Deployment | 1        |

### Template -> Containers:

Assign the _**redis-master**_ container, from the list of available containers.

### Template -> Services:

Create a _**master**_ service, that will allow access the _**redis-master**_ container.

| Name   | Description  | Type      | Port |
|--------|--------------|-----------|------|
| master | -            | ClusterIP | 6379 |

[Back](https://github.com/dirigiblelabs/zeus/tree/master/zeus/WikiContent/examples/redis)

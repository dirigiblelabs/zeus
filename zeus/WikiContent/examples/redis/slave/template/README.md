# Redis Slave Template

| Name        | Description      |
|-------------|------------------|
| redis-slave | Redis Slave      |

### Template -> Deployments:

Create _**Slave**_ deployment template.

| Name  | Description            | Replicas |
|-------|------------------------|----------|
| slave | Redis Slave Deployment | 2        |

### Template -> Containers:

Assign the _**redis-slave**_ container, from the list of available containers.

### Template -> Services:

Create a _**slave**_ service, that will allow access the _**redis-slave**_ container.

| Name  | Description  | Type      | Port |
|-------|--------------|-----------|------|
| slave | -            | ClusterIP | 6379 |

[Back](https://github.com/dirigiblelabs/zeus/tree/master/zeus/WikiContent/examples/redis)

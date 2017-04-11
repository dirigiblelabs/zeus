# PHP Redis Frontend Template

| Name     | Description            |
|----------|------------------------|
| frontend | PHP Redis Frontend     |

### Template -> Deployments:

Create _**frontend**_ deployment template.

| Name     | Description                   | Replicas |
|----------|-------------------------------|----------|
| frontend | PHP Redis Frontend Deployment | 3        |

### Template -> Containers:

Assign the _**php-redis**_ container, from the list of available containers.

### Template -> Services:

Create a _**slave**_ service, that will allow access the _**redis-slave**_ container.

| Name | Description  | Type      | Port |
|------|--------------|-----------|------|
| http | -            | ClusterIP | 80   |

[Back](https://github.com/dirigiblelabs/zeus/tree/master/zeus/WikiContent/examples/redis)

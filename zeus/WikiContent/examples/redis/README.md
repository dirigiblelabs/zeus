# Redis - Guestbook

In the following example is shown how to create an _**Redis - Guestbook**_ template in the Zeus Cloud Management Suite. The original example can be found [here](https://github.com/kubernetes/kubernetes/blob/master/examples/guestbook/all-in-one/guestbook-all-in-one.yaml).

## Prerequisites
- Up and running Kubernetes cluster
- Installed Zeus
- Configured default cluster in the Zeus

## Template Definition
### Containers:

1. Add _**Redis Master**_ container - see container [template](https://github.com/dirigiblelabs/zeus/tree/master/zeus/WikiContent/examples/redis/master/container).

2. Add _**Redis Slave**_ container - see container [template](https://github.com/dirigiblelabs/zeus/tree/master/zeus/WikiContent/examples/redis/slave/container).

3. Add _**PHP Redis**_ container - see container [template](https://github.com/dirigiblelabs/zeus/tree/master/zeus/WikiContent/examples/redis/php/container).

### Templates:

1. Add _**Redis Master**_ template - see [definition](https://github.com/dirigiblelabs/zeus/tree/master/zeus/WikiContent/examples/redis/master/template).

2. Add _**Redis Slave**_ template - see [definition](https://github.com/dirigiblelabs/zeus/tree/master/zeus/WikiContent/examples/redis/slave/template).

3. Add _**Frontend**_ template - see [definition](https://github.com/dirigiblelabs/zeus/tree/master/zeus/WikiContent/examples/redis/php/template).

## Deployment
1. From the _**Deployments**_ tab, start the _**redis-master**_ deployment template as _**master**_
2. From the _**Deployments**_ tab, start the _**redis-slave**_ deployment template as _**slave**_
3. From the _**Deployments**_ tab, start the _**frontend**_ deployment template as _**frontend**_
4. Create _**Ingress**_ for the _**frontend**_ application

| Name      | Sub-Domain   | Path | Service                 |
|-----------|--------------|------|-------------------------|
| frontend  | frontend     | /    | frontend-http           |

5. Access the ingress endpoint

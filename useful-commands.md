# Useful commands

When pushing to local minikube registry, need to disable tls:

```bash
podman push localhost:5000/imagename:tagname --tls-verify=false
```

When starting Minikube, need to run:

```bash
minikube start config set driver hyperkit --insecure-registry "10.0.0.0/24"
```

To enable access to registry from `localhost` on host machine, run:

```bash
docker run --rm -it --network=host alpine ash -c "apk add socat && socat TCP-LISTEN:5000,reuseaddr,fork TCP:$(minikube ip):5000"
```

*[source](https://minikube.sigs.k8s.io/docs/handbook/registry/)*

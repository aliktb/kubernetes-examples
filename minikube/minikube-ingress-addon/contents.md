# Contents

This is a slightly modified manifest from the [Minikube ingress-dns addon](https://minikube.sigs.k8s.io/docs/handbook/addons/ingress-dns/).

By default, the load balancer within Minikube is configured in a round-robin fashion. In order to demonstrate the round-robin config, the `--no-keepalive` cURL flag is used.

E.g.

```bash
curl --no-keepalive http://10.97.130.165
```

Browsers may use the `keep-alive` header by default so may not demonstrate the round-robined nature accurately.

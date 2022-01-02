# PRPO Kubernetes Config

[prpo-auth](https://github.com/zigapk/prpo-auth) and [prpo-chargers](https://github.com/zigapk/prpo-chargers) microservices can be found at [67.207.79.81/auth](http://67.207.79.81/auth) and [67.207.79.81/char](http://67.207.79.81/char) respectively.

Docs for both are avaiable at:

- docs for [prpo-auth](http://67.207.79.81/auth/docs/index.html) and
- docs for [prpo-chargers](http://67.207.79.81/char/docs/index.html)

Nginx ingress configuration is available in [ingress-configuration.yaml](ingress-configuration.yaml).

Each kubernetes config file can be applied using

```bash
kubectl apply -f [file_name]
```

# TODO: user interface

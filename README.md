# PRPO Docs

This project was implemented as an excercise in microservice development for PRPO subject at UNI LJ.

There are two microservices, both written in Go:
-  [prpo-auth](https://github.com/zigapk/prpo-auth) for handling of the users and user credentials as well as
-  [prpo-chargers](https://github.com/zigapk/prpo-chargers) for handling chargers and charger reservations.

Both are available at [67.207.79.81/auth](http://67.207.79.81/auth) and [67.207.79.81/char](http://67.207.79.81/char) respectively.

OpenAPI docs for each can be found at:
- [prpo-auth docs](http://67.207.79.81/auth/docs/index.html) and
- [prpo-chargers docs](http://67.207.79.81/char/docs/index.html)

A Nginx ingress controller is configured to route traffic to the desired backend. Its configuration can be found [here](ingress-configuration.yaml).

Each kubernetes config file can be applied using:

```bash
kubectl apply -f [file_name]
```

The entire stack was deployed to [Digitalocean's Kubernetes Service](https://www.digitalocean.com/products/kubernetes/) to evaluate their service and documentation. I was rather pleased with the simplicity and price performance of this solution, especially compared to alternatives such as AWS and Azure.

A sample [user interface](https://github.com/zigapk/prpo-ui) was developed to demonstrate some of the functionalities. It is deployed at [164.92.240.87](http://164.92.240.87).

Sample user's credentials:
- username: `test@prpo.si`
- password: `asdfasdf`

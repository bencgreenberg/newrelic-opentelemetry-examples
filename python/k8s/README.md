# Flask App Deployed on Kubernetes

## Installation

First, clone this repository then build the container and register it:

```bash
$ docker build -f Dockerfile -t newrelic-hello-world:v1 .

$ docker image tag newrelic-hello-world:v1 PUT_YOUR_USERNAME_HERE/newrelic-hello-world:v1

$ docker push YOUR_USERNAME_HERE/newrelic-hello-world:v1
```

Now, you are ready to create your Kubernetes deployment:

```bash
$ kubectl create -f deployment.yaml

$ kubectl create -f service.yaml
```

## Access the Application

You can test the app by going to it with the Node's public IP address, which is `localhost` if you are using docker-desktop:

```bash
$ curl http://localhost:30000
```

## Credit

Thanks to this [open source repository](https://github.com/anrajme/k8s-demo) for providing the starter code and instructions for this demo application deployed on Kubernetes.
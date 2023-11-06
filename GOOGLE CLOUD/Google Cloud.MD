# Google Cloud

## Kubernetes

- Pod is the smallest unit that can be created or deployed
- Represents a running process on the cluster as either a component of an application or an entire app
- Generally, you only have one container per Pod
  - However if you have hard dependencies, you can package them into a single Pod and share networking and storage resources between them
- Pod provides a unique network IP and set of ports
- One way to run a container in a Pod in K8s is to use the `kubectl run` command, which starts a Deployment with a container running inside a Pod
- Deployment represents a group of replicas of the same Pod and keeps your Pods running even when the nodes they run on fail
- Deployment can represent a component of an application or even an entire app

![K8s overview](img/1-k8s-overview.png)


## Cloud Run

- Managed compute platform that runs stateless containers via web requests or Pub/Sub events
- It's serverless, so don't require any infrastructure management from you
- It's build on Knative, an API and runtime environment built on Kubernetes
- It scales very quickly, near instantaneously, and you pay only for what you used
- You can use both container-based and sourcecode-based workflow
  - Source code approach deploys the source code instead of container image.\
  Cloud run then builds and packages the image (using Buildpacks)
![image](https://user-images.githubusercontent.com/88156993/135858556-7c830304-b288-48ff-a137-e442f2d35f33.png)
# Kubernetes
## What is Kubernetes?
Kubernetes, also known as K8s, is an open-source system for automating deployment, scaling, and management of containerized applications.

It groups containers that make up an application into logical units for easy management and discovery. Kubernetes builds upon 15 years of experience of running production workloads at Google, combined with best-of-breed ideas and practices from the community.

## Why Kubernetes?
### Benefits

- Flexibility: Kubernetes is highly configurable. It works with almost any container runtime and any infrastructure, whether it’s a public cloud, private cloud, or on-premises server. 
- Multi-cloud friendly: Given its flexibility, Kubernetes is able to host workloads spread across several clouds, making it an excellent tool for companies taking a multi-cloud approach.
- Increased productivity: Kubernetes facilitates declarative configuration and allows for GitOps, enabling teams to scale and deploy faster than ever before. 
- Open source: Kubernetes is community-led and fully open-source, helping developers and engineers to collaborate and innovate quicker. 
- Widely-used: Most developers and engineers know Kubernetes, which helps lower the learning curve for companies new to the platform. 

## K8 Architecture
![image](https://user-images.githubusercontent.com/88156993/135858803-7f4e107f-1584-4ad8-9bfc-1b120cb1ca15.png)
## Features

- Automated rollouts and rollbacks<br>
Kubernetes progressively rolls out changes to your application or its configuration, while monitoring application health to ensure it doesn't kill all your instances at the same time. If something goes wrong, Kubernetes will rollback the change for you. Take advantage of a growing ecosystem of deployment solutions.
- Service discovery and load balancing
No need to modify your application to use an unfamiliar service discovery mechanism. Kubernetes gives Pods their own IP addresses and a single DNS name for a set of Pods, and can load-balance across them.
- Storage orchestration
Automatically mount the storage system of your choice, whether from local storage, a public cloud provider such as GCP or AWS, or a network storage system such as NFS, iSCSI, Gluster, Ceph, Cinder, or Flocker.
- Secret and configuration management
Deploy and update secrets and application configuration without rebuilding your image and without exposing secrets in your stack configuration.
- Automatic bin packing
Automatically places containers based on their resource requirements and other constraints, while not sacrificing availability. Mix critical and best-effort workloads in order to drive up utilization and save even more resources.
- Batch execution
In addition to services, Kubernetes can manage your batch and CI workloads, replacing containers that fail, if desired.
- IPv4/IPv6 dual-stack
Allocation of IPv4 and IPv6 addresses to Pods and Services
- Horizontal scaling
Scale your application up and down with a simple command, with a UI, or automatically based on CPU usage.
- Self-healing
Restarts containers that fail, replaces and reschedules containers when nodes die, kills containers that don't respond to your user-defined health check, and doesn't advertise them to clients until they are ready to serve.
- Designed for extensibility
Add features to your Kubernetes cluster without changing upstream source code.

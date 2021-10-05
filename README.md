![image](https://user-images.githubusercontent.com/88156993/135986966-d371e89b-1a8c-4417-9114-8e7506248e22.png)

# Kubernetes
## What is Kubernetes?
Kubernetes, also known as K8s, is an open-source system for automating deployment, scaling, and management of containerized applications.

It groups containers that make up an application into logical units for easy management and discovery. Kubernetes builds upon 15 years of experience of running production workloads at Google, combined with best-of-breed ideas and practices from the community.

## Why Kubernetes?
### Benefits

- **Flexibility**: Kubernetes is highly configurable. It works with almost any container runtime and any infrastructure, whether it’s a public cloud, private cloud, or on-premises server. 
- **Multi-cloud friendly**: Given its flexibility, Kubernetes is able to host workloads spread across several clouds, making it an excellent tool for companies taking a multi-cloud approach.
- **Increased productivity**: Kubernetes facilitates declarative configuration and allows for GitOps, enabling teams to scale and deploy faster than ever before. 
- **Open source**: Kubernetes is community-led and fully open-source, helping developers and engineers to collaborate and innovate quicker. 
- **Widely-used**: Most developers and engineers know Kubernetes, which helps lower the learning curve for companies new to the platform. 

## K8 Architecture
![image](https://user-images.githubusercontent.com/88156993/135858803-7f4e107f-1584-4ad8-9bfc-1b120cb1ca15.png)
## Features

### Automated rollouts and rollbacks
Kubernetes progressively rolls out changes to your application or its configuration, while monitoring application health to ensure it doesn't kill all your instances at the same time. If something goes wrong, Kubernetes will rollback the change for you. Take advantage of a growing ecosystem of deployment solutions.
### Service discovery and load balancing
No need to modify your application to use an unfamiliar service discovery mechanism. Kubernetes gives Pods their own IP addresses and a single DNS name for a set of Pods, and can load-balance across them.
### Storage orchestration
Automatically mount the storage system of your choice, whether from local storage, a public cloud provider such as GCP or AWS, or a network storage system such as NFS, iSCSI, Gluster, Ceph, Cinder, or Flocker.
### Secret and configuration management
Deploy and update secrets and application configuration without rebuilding your image and without exposing secrets in your stack configuration.
### Automatic bin packing
Automatically places containers based on their resource requirements and other constraints, while not sacrificing availability. Mix critical and best-effort workloads in order to drive up utilization and save even more resources.
### Batch execution
In addition to services, Kubernetes can manage your batch and CI workloads, replacing containers that fail, if desired.
### IPv4/IPv6 dual-stack
Allocation of IPv4 and IPv6 addresses to Pods and Services
### Horizontal scaling
Scale your application up and down with a simple command, with a UI, or automatically based on CPU usage.
### Self-healing
Restarts containers that fail, replaces and reschedules containers when nodes die, kills containers that don't respond to your user-defined health check, and doesn't advertise them to clients until they are ready to serve.
### Designed for extensibility
Add features to your Kubernetes cluster without changing upstream source code.

## Commands

```
 Find more information at: https://kubernetes.io/docs/reference/kubectl/overview/

Basic Commands (Beginner):
  create        Create a resource from a file or from stdin.
  expose        Take a replication controller, service, deployment or pod and expose it as a new Kubernetes Service
  run           Run a particular image on the cluster
  set           Set specific features on objects

Basic Commands (Intermediate):
  explain       Documentation of resources
  get           Display one or many resources
  edit          Edit a resource on the server
  delete        Delete resources by filenames, stdin, resources and names, or by resources and label selector      

Deploy Commands:
  rollout       Manage the rollout of a resource
  scale         Set a new size for a Deployment, ReplicaSet or Replication Controller
  autoscale     Auto-scale a Deployment, ReplicaSet, StatefulSet, or ReplicationController

Cluster Management Commands:
  certificate   Modify certificate resources.
  cluster-info  Display cluster info
  top           Display Resource (CPU/Memory) usage.
  cordon        Mark node as unschedulable
  uncordon      Mark node as schedulable
  drain         Drain node in preparation for maintenance
  taint         Update the taints on one or more nodes

Troubleshooting and Debugging Commands:
  describe      Show details of a specific resource or group of resources
  logs          Print the logs for a container in a pod
  attach        Attach to a running container
  exec          Execute a command in a container
  port-forward  Forward one or more local ports to a pod
  proxy         Run a proxy to the Kubernetes API server
  cp            Copy files and directories to and from containers.
  auth          Inspect authorization
  debug         Create debugging sessions for troubleshooting workloads and nodes

Advanced Commands:
  diff          Diff live version against would-be applied version
  apply         Apply a configuration to a resource by filename or stdin
  patch         Update field(s) of a resource
  replace       Replace a resource by filename or stdin
  wait          Experimental: Wait for a specific condition on one or many resources.
  kustomize     Build a kustomization target from a directory or URL.

Settings Commands:
  label         Update the labels on a resource
  annotate      Update the annotations on a resource
  completion    Output shell completion code for the specified shell (bash or zsh)   

Other Commands:
  api-resources Print the supported API resources on the server                      /version"
  api-versions  Print the supported API versions on the server, in the form of "group/version"
  config        Modify kubeconfig files
  plugin        Provides utilities for interacting with plugins.
  version       Print the client and server version information

Usage:
  kubectl [flags] [options]
                                                                                     nds).
Use "kubectl <command> --help" for more information about a given command.
Use "kubectl options" for a list of global command-line options (applies to all commands).
```
### List available services
`kubectl get service` or `kubectl get svc`
### Create a resource from a file or from stdin
`kubectl create -f file.yml`<br>
*JSON and YAML formats are accepted*
### Display one or many resources
`kubectl get deploy`<br>
`kubectl get pods`<br>
*Prints a table of the most important information about the specified resources. You can filter the list using a label selector and the --selector flag. If the desired resource type is namespaced you will only see results in your current namespace unless you pass --all-namespaces.*
### Show details of a specific resource or group of resources
`kubectl describe deploy deployment-name`<br>
`kubectl describe pod pod-name`<br>
*Print a detailed description of the selected resources, including related resources such as events or controllers. You may select a single object by name, all objects of that type, provide a name prefix, or label selector.*
### Delete resources by file names, stdin, resources and names, or by resources and label selector
`kubectl delete pod pod-name`<br>
*JSON and YAML formats are accepted. Only one type of argument may be specified: file names, resources and names, or resources and label selector*
### Edit a resource from the default editor
`kubectl edit deploy deployment-name`<br>
*The edit command allows you to directly edit any API resource you can retrieve via the command-line tools. It will open the editor defined by your KUBE_EDITOR, or EDITOR environment variables, or fall back to 'vi' for Linux or 'notepad' for Windows. You can edit multiple objects, although changes are applied one at a time. The command accepts file names as well as command-line arguments, although the files you point to must be previously saved versions of resources.*

![image](https://user-images.githubusercontent.com/88156993/136014381-ae02de0f-dad7-4b62-a95b-8104fc308c72.png)

# Kubernete Security

## Image
### scaning
<b>Trivy</b>
- Scanners that look for security issues, and targets where it can find those issues.
- Terget: Container Image, Filesystem, Git repo, VM Image, Kubernetes
- Command: trivy image python:3.4-alpine, trivy k8s --report summary cluster
 
<b>Clair</b> or <b>Anchore</b>

### Immutability, container and pod level enforcement

Immutable Containers: Containers should be built in such a way that their environment, configuration, and file system cannot be modified after they start. Once a container is running, you can restrict changes by mounting volumes as read-only or by preventing changes to files and configurations.

Immutable Container Images: Containers are typically run from immutable images. These images should not be changed once they're created. Instead, a new image is built and deployed when updates are necessary.

Read-only File Systems: You can configure containers to use a read-only file system, ensuring that no changes can be made to the container during runtime, preventing unauthorized modifications.

### minimal base images (alpain, busybox)
### signing and verification

## Runtime
	- Seccomp (Security Compute Mode) - restrict syscolls
	- AppArmor / SELinux - MAC (Mandatory Access Control)
	- Namespaces - for network and PID

## Pods
	- Pod Security Admissio (PSA)
	- Servicea Account and RBAC
	- NetPol
	- Secrets

## Nodes
	- update
	- minimum OS images
	- firewalling and isolation

## Kubelet
	- strong authentication and authorizatio, communications should be HTTPS and 

## Communication:
	- TLS - Transport Layer Security - cryptografic protocol
	- mTLS - Mutual TLS - TLS+mutual authenetication, common use for microservices, where both side need authenticated (API).
	- TCP - Transmission Control Protocol - realiable, ordered and error-free delivery
	- UDP - User Datagram Protocol - fast but without gurantee delivery common used in video, steraming, anline game anc voice.

## NodeToNode communication
	- TLS encryption
	- API Server authentication and authorization
	- Audit Logging
	- NetworkSecurity: Service Mesh, NetPol
	- Hardering CIS Benchamrk - config cerretcly and encrypt etcd

## Container Runtime Security
	- limit privilages for containerd use Falco

# Kubernete Security

## Image
### scaning
> Trivy
> -Scanners that look for security issues, and targets where it can find those issues.
> -Terget: Container Image, Filesystem, Git repo, VM Image, Kubernetes
> -Command: trivy image python:3.4-alpine, trivy k8s --report summary cluster
 
 , clair ar anchore
	> immutble
	> minimal base images (alpain, busybox)
	> signing and verification

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

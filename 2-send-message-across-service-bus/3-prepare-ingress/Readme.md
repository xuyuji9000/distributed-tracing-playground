# Introduction

This file documents the learning about adding ingress, so sender service sending out message can be triggered from public Internet.

# Commands

- Check target context, 
  before executing command

  ``` shell
  kubectl config get-contexts
  ```

- Create ingress

  ``` shell
  kubectl apply -f ./distributed-tracing-ingress.yaml
  ```


# Reference

- [kubernetes/ingress-nginx](https://github.com/kubernetes/ingress-nginx)
  
  Github repo for `kubernetes/ingress-nginx`

- [ NGINX Ingress Controller ](https://kubernetes.github.io/ingress-nginx/deploy/)
  
  Get started with with `k8s.io/ingress-nginx` ingress controller.

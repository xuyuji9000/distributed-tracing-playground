This folder contains the steps to setup Jaeger backend.


# Steps

1. Install Jaeger Operator

    ``` shell
    kubectl create namespace observability 

    kubectl create -f https://github.com/jaegertracing/jaeger-operator/releases/download/v1.35.0/jaeger-operator.yaml -n observability 

    ```

2. Install a Jaeger instance

    ``` shell
    kubectl apply -n observability ./simplest.yaml
    ```

3. Add missing ingressclass annotation. So the nginx ingress controller can pick the ingress instance up.

    ``` shell
    kubectl edit ingress simplest-query -n observability
    ```

    ``` shell
    # Add missing ingress.class annotation
    annotations:
      kubernetes.io/ingress.class: nginx
    ```

# Reference

- [Operator for Kubernetes](https://www.jaegertracing.io/docs/1.35/operator/)

  > This introduces Operator pattern in Jaeger context.

- [jaegertracing/jaeger-operator](https://github.com/jaegertracing/jaeger-operator)
  
  > This introduce how to install simplest Jaeger instance.

- [How to view ingress](https://github.com/jaegertracing/jaeger-operator/issues/1135)

  > This help fixes the missing public ip problem for ingress

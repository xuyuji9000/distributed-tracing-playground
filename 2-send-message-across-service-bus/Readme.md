This folder contains learning about sending message across service bus.

# Steps

1. [distributed-tracing-receiver](https://github.com/xuyuji9000/distributed-tracing-receiver)

2. [distributed-tracing-sender](https://github.com/xuyuji9000/distributed-tracing-sender)

3. [prepare-ingress](./3-prepare-ingress.md)

# Conclusion 

A receiving service cannot automatically collect the traces to Jaeger backend, when it receives message across service bus.

![Only sender service showed up](./images/Screen%20Shot%202022-06-29%20at%204.58.29%20PM.png)
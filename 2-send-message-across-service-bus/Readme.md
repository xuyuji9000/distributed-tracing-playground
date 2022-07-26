This folder contains learning about sending message across service bus.

# Services

- [receiver](receiver/Readme.md)

- [distributed-tracing-sender](https://github.com/xuyuji9000/distributed-tracing-sender)

# Conclusion 

A receiving service cannot automatically collect the traces to Jaeger backend, when it receives message across service bus.

![Only sender service showed up](./images/Screen%20Shot%202022-06-29%20at%204.58.29%20PM.png)
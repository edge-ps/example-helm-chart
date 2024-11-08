# Example Nginx Chart

This example helm chart deploys two nginx webservers which are exposed via Emissary to the store network, one mapping TCP traffic and the other mapping HTTPS traffic.
The example includes the required Emissary/Linkerd resources to successfully mesh and expose the service:
- [TCPMapping](https://www.getambassador.io/docs/emissary/latest/topics/using/tcpmappings)/[Mapping](https://www.getambassador.io/docs/emissary/latest/topics/using/intro-mappings)
- [Server](https://linkerd.io/2-edge/reference/authorization-policy/#server)
- [AuthorizationPolicy](https://linkerd.io/2-edge/reference/authorization-policy/#authorizationpolicy)
- [NetworkAuthentication](https://linkerd.io/2-edge/reference/authorization-policy/#networkauthentication)
- Annotations/labels to be included to workload namespace
    - [Linkerd injection annotation](https://linkerd.io/2-edge/features/proxy-injection/)

## Prerequisites

- Ensure that Emissary is running successfully on the store.
- Ensure that Linkerd is running successfully on the store.

## Installation

```helm install nginx .```

## Uninstall

```helm uninstall nginx```


# EPIC is an external API Gateway  

It is designed for use with Kubernetes but can also be used with Linux hosts.

By external, the k8s cluster that runs the Gateway consisting of Envoy proxy instances is external to the k8s clusters it serves.

An external gateway has the benefit of isolation from application and data contained in the cluster.  EPIC also has the ability to share a single gateway over multiple clusters
allowing application endpoints to be distributed among multiple clusters and hosts.

A Gateway Controller, based upon the k8s Gateway API is installed on a cluster so cluster users can create API gateway on demand based upon templates 
defined in the Gateway Cluster

Gateways can also be created on Linux hosts using an agent installed on the host.


The key components of the EPIC platform are:

1. EPIC - The external gateway.  Its a purpose built k8s cluster that hosts uService Gateways
2. k8s Gateway Controller.  The gateway controller use the Gateway API to create gateways and http or TCP routes
3. Linux Gateway Controller.  This controller uses the same model as the Gateway API but does not require Kubernetes
4. Gateway Service Manager. A User interface that can be used to provide Gateway as a Service.





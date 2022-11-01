<h1 align="center">
    <img src="https://user-images.githubusercontent.com/6763318/199222816-f1238884-48b0-42ff-8ec1-9b958154a4f4.png" alt="Higress" width="240" height="72.5">
  <br>
  Next-generation Cloud Native Gateway
</h1>

Higress is a next-generation cloud-native gateway based on Alibaba's internal gateway practices. 

Powered by [Istio](https://github.com/istio/istio) and [Envoy](https://github.com/envoyproxy/envoy), Higress realizes the integration of the triple gateway architecture of traffic gateway, microservice gateway and security gateway, thereby greatly reducing the costs of deployment, operation and maintenance.

<BR><center><img src="https://img.alicdn.com/imgextra/i4/O1CN01dqXHDi27RhjAtZyNp_!!6000000007794-0-tps-1794-1446.jpg" alt="Higress Architecture"></center>

## Summary

- [**Use Cases**](#use-cases)
- [**Higress Features**](#higress-features)


## Use Cases

- **Kubernetes ingress controller**: 

  Higress can function as a feature-rich ingress controller, which is compatible with many annotations of K8s' nginx ingress controller.
  
  [Gateway API](https://gateway-api.sigs.k8s.io/) support is in progress and will support smooth migration from Ingress API to Gateway API.
  
- **Microservice gateway**: 

  Higress can function as a microservice gateway, which can discovery microservices from various service registries, such as Nacos, ZooKeeper, Consul, etc.
  
  It deeply integrates of [Dubbo](https://github.com/apache/dubbo), [Nacos](https://github.com/alibaba/nacos), [Sentinel](https://github.com/alibaba/Sentinel) and other microservice technology stacks.
  
- **Security gateway**:

  Higress can be used as a security gateway, supporting WAF and various authentication strategies, such as key-auth, hmac-auth, jwt-auth, basic-auth, oidc, etc.  
  

## Higress Features

   （TODO）
  
  
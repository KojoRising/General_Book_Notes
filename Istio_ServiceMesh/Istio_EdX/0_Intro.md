# Istio Service Mesh

## Links
- https://learning.edx.org/course/course-v1:LinuxFoundationX+LFS144x+3T2022/home

## Objectives
- Install Istio on a Kubernetes cluster.
- Configure Ingress.
- Understand how sidecar injection works.
- Monitor your services using Grafana, Zipkin, and Kiali.
- Route traffic between multiple service versions.
- Perform blue-green and canary deployments.
- Inject failures and use resiliency features.
- Understand the concept of workload identity and “zero trust” architectures.
- Control access to your workloads.
- Extend the Istio mesh functionality using WebAssembly.

## Course Outline
● Welcome!
This section provides an introduction to the course, including important information on
how to take the course.
● Chapter 1. Overview of Service Mesh and Istio
This section examines the problems that stemmed from the shift to cloud-native
applications and how these problems were mitigated before service meshes existed. It
focuses on how service meshes address these problems and the design and
architecture of Istio.
● Chapter 2. Installing Istio
This section discusses different ways to install Istio on a Kubernetes cluster. It focuses
on the basics of the Istio Operator API, different Helm charts used for installation, and
the differences between Istio installation profiles
● Chapter 3. Observability
This section examines the difference between monitoring and observability and the value
that Istio provides with respect to metrics collection and observability. It focuses on how
metrics are collected in Istio and delves into topics such as Prometheus, Grafana, and
Kiali.
● Chapter 4. Traffic Management
This section discusses how to expose services from a cluster and Istio traffic routing. It
focuses on request properties, service resilience, failure injection, and circuit breaking.
● Chapter 5. Security
This section focuses on authentication, authorization, and access control. It delves into
mTLS and how to configure TLS configuration for sidecar proxies and gateways, as well
as service and user authentication.
● Chapter 6. Extending the Mesh
This section discusses the basic building blocks of the Envoy proxy and how to
customize the Envoy proxy configuration using the EnvoyFilter resource. It examines
how to build a basic Wasm plugin using Go and Proxy-Wasm SDK as well as how to use
WasmPlugin resource to deploy a Wasm plugin to Istio service mesh.
● Chapter 7. Advanced Topics
This section discusses the purpose of the Sidecar resource, the process of onboarding
virtual machines to the mesh, and the different facets of deploying Istio in multi-cluster
scenarios.
● Chapter 8. Istio Community
This chapter delves into the importance of the Istio community, different channels to
interact with the Istio community, and major Istio events.
● Final Exam (Verified Certificate track only)

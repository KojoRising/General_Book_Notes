# 1 Overview of Service Mesh And Istio

## Links
- https://learning.edx.org/course/course-v1:LinuxFoundationX+LFS144x+3T2022/block-v1:LinuxFoundationX+LFS144x+3T2022+type@sequential+block@8bdd612c3a1942ba9f9f8001ffad60a9
- [Twelve-Factor App](https://12factor.net/)
- [Beyond the Twelve-Factor App](https://tanzu.vmware.com/content/blog/beyond-the-twelve-factor-app)

## Chapter Objectives
- What problems stemmed from the shift to cloud-native applications.
- How these problems were mitigated before service meshes existed.
- How service meshes address these problems.
- The design and architecture of Istio.

### 1 Shift to Cloud-Native Applications
- Businesses shifting from Monoliths to Micro-Service based architecture
- Companies shared their experience around these technologies, publishing [Twelve-Factor App](https://12factor.net/)

### 2 New Problems/Challenges Presented by New Architecture
- As codebases shrank, method calls became -> network calls
- Address of target service in an increasingly dynamic environment became difficult to resolve
- How does one service know if another is available?

#### Challenge List
1 Service discovery:
- How does a service discover the network address of other services?

2 Load balancing:
- Given that each service is scaled horizontally, the problem of load-balancing was no longer an ingress-only problem.

3 Service call handling:
- How to deal with situations where calls to other services fail or take an inordinately long time?
- An increasing portion of developers' codebases had to be dedicated to handling the failures and dealing with long response times, by sprinkling in retries and network timeouts.

4 Resilience:
- Developers had to learn (perhaps the hard way) to build distributed applications that are resilient and that prevent cascading failures.

5 Security:
- How do we secure our systems given this new architecture has a much larger attack surface?
- Can a service trust calls from other services?
- How does a service identify its caller?

6 Programming models:
- Developers began exploring alternative models to traditional multithreading to deal more efficiently with network IO (input and output, see ReactiveX).

7 Diagnosis and troubleshooting:
- Stack traces no longer provided complete context for diagnosing an issue. Logs were now distributed. How does a developer diagnose issues that span multiple microservices?

8 Resource utilization:
- Managing resource utilization efficiently became a challenge, given the larger deployment footprint of a system made up of numerous smaller services.

9 Automated testing:
- End-to-end testing became more difficult.

10 Traffic management:
- The ability to route requests flexibly to different services under different conditions started becoming a necessity.

### 3 Early Solutions

#### Netflix
- Had to rapidly move to the cloud
- Wrote many projects such as Eureka Service Registry (Service Discovery), Ribbon for client-side load-balancing, Hystrix library (for cascading failures), and Zuul Proxy for routing flexibility for bg deployments
- Spring Engineering team adapted these projects to popular Spring Framework

#### Certain Constraints were implied
- Services had to be written for JVM + had to use Spring Framework

### 4 Service Meshes

#### Lyft Approach | Service Meshes
- Route requests in/out of a given application through its proxy
- Proxy could be configured - With specific network timeouts, retry logic, circuit-breaking logic, etc.
- Security Upgrades - Connections could be upgraded from plain HTTP to encrypted traffic
- Project was open-sourced & called [`Envoy`](https://envoyproxy.io/)

#### Istio & Envoy
- Istio project was started at Google
- Envoy was the perfect building block for Istio
- Istio controlplane - Would automate configuration/synchronization of proxies deployed onto K8s as sidecars inside each Pos
- K8s API-Server - Could be leveraged to automate service discovery & communicate locations of servicew endpoints directly to each proxy


### 5 Istio Architecture

**Istio Basic Idea** 
- Push microservices concerns into infrastructure by leveraging Kubernetes
- Implemented by - Bundling Envoy proxy as a sidecar container directly inside every Pod

#### Istio Main Concerns
- Ensuring that each time a workload is deployed, an Envoy sidecar is deployed alongside it.
- Ensuring traffic into and out of the application is transparently diverted through the proxy.
- Assigning each workload a cryptographic identity as the basis for a more secure computing environment.
- Configuring the proxies with all the information they need to handle incoming and outgoing traffic.

### 6 Sidecar Injection
### 7 
### 8 
### 9 
### 10 
### 11 
### 12 
### 13 
### 14 
### 15 
### 16 
### 17 
### 18 
### 19 
### 20 




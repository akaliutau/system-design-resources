About
======

This is a list of web resources on technologies tied (directly or proximitly) with architecture and design of microservices.

Total more than 100 resources aggregated

I chose mostly those technologies created on the basis of Java/Scala, but this is a sort of personal choice - microservices, as well as all related services, can be written in any language. 

Overview
=========

Microservice architecture is a vast topic, so I created a hierarchical content to get a high-level grasp of this realm as the whole. 
All resources are divided on groups, containing several topics. Each topic in its turn contains a few references.


General topics:

- REST libraries/frameworks
- Asynchronicity
- Messaging
- Security
- CI/CD
- Deployment/Orchestration


Microservice cloud's components:

- Configuration
- Service discovery
- API gateway
- Load balancing
- Resilience

Observability:

- Metrics
- Distributed Tracing
- Monitoring
- Alerting
- Log management


Testing:

- Unit Tesing
- Integration Tesing
- Load testing
- Security testing


Resources
==========

# General topics
---

## REST libraries/frameworks
- [Apache CXF](https://cxf.apache.org/) | used to build and develop services using frontend programming APIs, like JAX-WS and JAX-RS
- [Dropwizard](https://www.dropwizard.io/) | out-of-the-box support for configuration, application metrics, logging, operational tools, and more
- [Spark](https://sparkjava.com/) | a micro framework for creating web applications in Java with a minimal efforts, through DSL
- [Play Framework](https://www.playframework.com/) | is a high velocity, hyper-productive web framework for Java and Scala, with powerful templating engine and other features
- [Akka HTTP](https://akka.io/akka-http/) | a full server-side and client-side HTTP stack implemented on top of actor model

## Asynchronicity
- [Reactive Programming](https://en.wikipedia.org/wiki/Reactive_programming) | a standard for asynchronous stream processing with non-blocking back pressure, general information
- [Spring WebFlux](https://docs.spring.io/spring/docs/current/spring-framework-reference/web-reactive.html) | Reactive programming for Spring Boot
- [AsyncHttpClient](https://github.com/AsyncHttpClient/async-http-client) | lightweight async client for microservices

## Messaging
- [Axon Framework](https://axoniq.io/) | a lightweight, open-source Java framework to build scalable, extensible event-driven applications
- [Lagom](https://www.lightbend.com/lagom-framework) | an opinionated, open source framework for building reactive microservice systems in Java/Scala
- [Akka](https://akka.io/) | a toolkit for building highly concurrent, distributed, and resilient message-driven applications for Java and Scala
- [ZeroMQ](https://zeromq.org/) | a brokerless messaging middleware (allows to connect sockets N-to-N with patterns like fan-out, pub-sub, task distribution, and request-reply)
- [Apache Kafka](https://kafka.apache.org/) | <em>the</em> message broker: horizontally scalable, fault-tolerant, super-fast, and is able to digest fantabulously massive volumes of messages.
- [RabbitMQ](https://www.rabbitmq.com/) | a classical examples of the message brokers which speak AMQP protocol.
- [NATS](https://nats.io/) | a simple, high performance open source messaging system for cloud-native applications, IoT messaging, and microservice architectures. It implements a highly scalable and elegant publish-subscribe message distribution model
- [NSQ](https://nsq.io/) | an open-source realtime distributed messaging platform, designed to operate at scale and handle billions of messages per day. It also follows a broker-less model and as such has no single point of failure, supports high-availability and horizontal scalability.

## Security
- [Spring security](https://spring.io/projects/spring-security) | a powerful and highly customizable authentication and access-control framework. It is the de-facto standard for securing Spring-based applications.
- [Secret Vault project](https://www.vaultproject.io/) | secures, stores, and tightly controls access to tokens, passwords, certificates, API keys, and other secrets in modern computing, see also https://learn.hashicorp.com/vault/#getting-started
- [Clair](https://github.com/coreos/clair) | an open source project for the static analysis of vulnerabilities in application containers
- [KMS (Google)](https://cloud.google.com/kms/) | a dedicated service to manage encryption keys, Key Management Service
- [AWS Security products](https://aws.amazon.com/products/security/) | 
- [AirTasker](https://www.airtasker.com/careers/) | 

## Identity providers
- [Keycloak](https://www.keycloak.org/) | an open source Identity and Access Management solution aimed at modern applications and services. It makes it easy to secure applications and services with little to no code.
- [WSO2 Identity Server](https://wso2.com/identity-and-access-management/) | an extensible, open source IAM solution to federate and manage identities across both enterprise and
cloud environments including APIs, mobile, and Internet of Things devices

## CI/CD
- [Jenkins](https://jenkins.io/doc/) | one of the most widely deployed continuous integration (and continuous delivery) platforms
- [Bazel](https://bazel.build/) | an open-source build and test tool similar to Make, Maven, and Gradle. It uses a human-readable, high-level build language. Bazel supports projects in multiple languages and builds outputs for multiple platforms. Bazel supports large codebases across multiple repositories, and large numbers of users.
- [Buildbot](https://buildbot.net/) | a job scheduling system which supports distributed, parallel execution of jobs across multiple platforms, flexible integration with different source control systems and extensive job status reporting
- [Jenkins](https://jenkins.io/doc/) | one of the most widely deployed continuous integration (and continuous delivery) platforms

## Deployment/Orchestration
- [Docker](https://www.docker.com/) | an exceptionally lightweight (comparing to traditional virtual machines) architecture, with little to no overhead, allowing to share the same operating system kernel without extra hardware support. Docker can be served as a replacement of virtual machines in 99% cases
- [Apache Mesos](https://mesos.apache.org/) | a cluster-management platform, which abstracts CPU, memory, storage, and other compute resources away from machines (physical or virtual), enabling fault-tolerant and elastic distributed systems to easily be built and run effectively
- [Titus](https://github.com/Netflix/titus/) | is a framework on the top of Apache Mesos. It is a container management platform that provides scalable and reliable container execution and cloud-native integration with Amazon AWS. Titus was built internally at Netflix and is used in production to power Netflix streaming, recommendation, and content systems.
- [Nomad](https://www.nomadproject.io/) | is a highly available, distributed, data-center aware cluster and application scheduler designed to support the modern datacenter with support for long-running services, batch jobs, and more. It makes sense to use it with other products of HashiCorp, because it has outstanding native integration with Consul and Vault to complement the service discovery and secret management
- [Kubernetes (K8s)](https://kubernetes.io/) | is an open-source system for automating deployment, scaling, and management of containerized applications.
- [Service Meshes Pattern](https://medium.com/solo-io/https-medium-com-solo-io-supergloo-ff2aae1fb96f) | service mesh is an infrastructure layer that handles service-to-service communication, freeing applications from being aware of the complex communication network. The mesh provides advanced capabilities, including encryption, authentication and authorization, routing, monitoring and tracing.
- [Linkerd](https://linkerd.io/) | is a light service mesh for Kubernetes with observability, reliability, and security without requiring any code changes.
- [Istio](https://istio.io/) | an open source service mesh that layers transparently onto existing distributed applications. It is also a platform, including APIs that let it integrate into any logging platform, or telemetry or policy system.
- [Consul Connect](https://www.consul.io/docs/connect/) | provides service-to-service connection authorization and encryption using mutual Transport Layer Security (mTLS).
- [SuperGloo](https://supergloo.solo.io/) | an open-source project to manage and orchestrate service meshes at scale.

# Microservice cloud's components:
---

## Configuration
- [Spring Cloud Config](https://spring.io/projects/spring-cloud-config) | built on top of the Spring Platform, then Spring Cloud Config is the one of the most accessible configuration management options to start with. It provides both server-side and client-side support (the communication is based on HTTP protocol), is exceptionally easy to integrate with and even to embed into existing services.
- [Archaius](https://github.com/Netflix/archaius) | yet another excellent product from Netflix family

## Service discovery
- [Atomix](https://atomix.io/) | provides capabilities for cluster management, communicating across nodes, asynchronous messaging, group membership, leader election, distributed concurrency control, partitioning, replication and state changes coordination in distributed systems.
- [Eureka](https://github.com/Netflix/eureka) | a REST-based service that is dedicated to be primarily used for service discovery purposes (with an emphasis on AWS support). It is written purely in Java and includes server and client components
- [Apache Zookeeper](https://zookeeper.apache.org/) | a centralized, highly available service for managing configuration and distributed coordination.
- [Etcd](https://coreos.com/etcd/) | a distributed, consistent and highly-available key value store, with emphasis to use for service discovery and configuration management.
- [Consul](https://www.consul.io/) | a distributed, highly available, and data center aware solution for service discovery and configuration.

## API gateway
- [Zuul/Zuul2](https://github.com/Netflix/zuul) | serves as the front door for all requests coming to their streaming backends. It is a gateway service (also sometimes called edge service) that provides dynamic routing, monitoring, resiliency, security, and more
- [Spring Cloud Gateway](https://spring.io/projects/spring-cloud-gateway) | a library to facilitate building your own API gateways leveraging Spring MVC and Spring WebFlux. The first generation of Spring Cloud Gateway was built on top of Zuul, but the next one has migrated to Spring’s Project Reactor
- [Microgateway](https://github.com/strongloop/microgateway) | a developer-focused, extensible gateway framework written in Node.js for enforcing access to Microservices and APIs.
- [Gloo](https://gloo.solo.io/) | an advanced Kubernetes-native API gateway, the next generation implementation of software from that category. Gloo is exceptional in its function level routing; its support for legacy apps, microservices and serverless; its discovery capabilities; its numerous features; and its tight integration with leading open-source projects.
- [Apache Camel](https://github.com/apache/camel) | a collection of base components to build your own api gateway system

## Load balancing
- [Nginx](https://nginx.org/) | an open source software for web serving, reverse proxying, caching, load balancing of TCP/ HTTP/ UDP traffic (including HTTP/2 and gRPC as well), media streaming, and much more. What makes nginx extremely popular choice is the fact that its capabilities go way beyond just load balancing. In fact, it's often used as a de-factor web-server. Also it can be served as a static API gateway.
- [HAProxy](https://www.haproxy.org/) | is a free, very fast, reliable, high performance TCP/ HTTP (including HTTP/2 and gRPC) load balancer. In some sense it can be the 100% replacement for nginx and suitable for the most kinds of deployment environments and workloads. Also (as well as nginx) it can be served as a static API gateway.
- [Traefik](https://traefik.io/) | a reverse proxy and load balancer, it exposes metrics, access logs, bundles web UI and REST(ful) web APIs
- [Synapse](https://github.com/airbnb/synapse) | a system for service discovery, developed and open sourced by Airbnb.
- [Envoy](https://www.envoyproxy.io/) | a representative of the new generation of edge and service proxies. It supports advanced load balancing features (including retries, circuit breaking, rate limiting, request shadowing, zone local load balancing, etc) and has first class support for HTTP/2 and gRPC.
- [Ribbon](https://github.com/Netflix/ribbon) | a client-side IPC library with built-in software load balancing. It supports TCP, UDP and HTTP protocols and integrates with Eureka.

## Resilience patterns
- [Health check pattern](https://microservices.io/patterns/observability/health-check-api.html) | infrastructure and orchestration layers to probe the service
- [Spring-retry](https://github.com/spring-projects/spring-retry) | retrying the request to the service in case of intermittent failures
- [failsafe](https://github.com/jhalterman/failsafe) | offering a range of retry and back-off policies
- [resilience4j](https://github.com/resilience4j/resilience4j) | offering a range of retry and back-off policies
- [Bulkhead](https://en.wikipedia.org/wiki/Bulkhead_(partition)) | minimize the impact of the failures in the applications
- [Rate limiting](https://en.wikipedia.org/wiki/Rate_limiting) | a technique to control the rate of requests


# Observability:
---

## Metrics
- [Graphite](https://graphiteapp.org/) | is an enterprise-ready monitoring tool that runs equally well on cheap hardware or Cloud infrastructure to store, retrieve, share, and visualize timeseries data.
- [OpenTSDB](https://opentsdb.net/) | is a distributed, scalable Time Series Database (TSDB) written on top of HBase addressing the need to store, index and serve metrics collected from computer systems (network gear, operating systems, applications) at a large scale, and make this data easily accessible and graphable.
- [TimescaleDB](https://www.timescale.com/) | yet another time series database optimized for fast ingest and complex queries.
- [Prometheus](https://github.com/prometheus) | is an open-source systems monitoring and alerting toolkit
- [Atlas](https://github.com/Netflix/atlas) | used to manage dimensional time series data for near real-time operational insight.


## Distributed Tracing
- [OpenZipkin](https://zipkin.io/) | a distributed tracing system. It helps gather timing data needed to troubleshoot latency problems in service architectures.
- [OpenTracing](https://opentracing.io/) | is comprised of an API specification, frameworks and libraries that have implemented the specification, and documentation for the project.
- [Brave](https://github.com/openzipkin/brave) | is a distributed tracing instrumentation library. Brave typically intercepts production requests to gather timing data, correlate and propagate trace contexts.
- [Jaeger](https://www.jaegertracing.io/) | a distributed tracing system
- [OpenSensus](https://opencensus.io/) | a set of libraries for various languages that allow you to collect application metrics and distributed traces, then transfer the data to a backend of your choice in real time.
- [Haystack](https://expediadotcom.github.io/haystack/) | an Expedia -backed open source distributed tracing project to facilitate detection and remediation of problems in microservices and websites.
- [Apache SkyWalking](https://skywalking.apache.org/) | an open source observability platform to collect, analyze, aggregate and visualize data from services and cloud native infrastructures

## Monitoring
- [Graphana](https://grafana.com/) | a visualization tool with its own alert engine and alert rules.
- [Chronograf](https://www.influxdata.com/time-series-platform/chronograf) | a user interface for Kapacitor - a native data processing engine that can process both stream and batch data from InfluxDB (all from TICK Stack)

## Alerting
- [Alertmanager](https://prometheus.io/docs/alerting/alertmanager/) | used to handle alerts sent by client applications such as the Prometheus server. It takes care of deduplicating, grouping, and routing them to the correct receiver

## Log management
- [ELK](https://www.elastic.co/what-is/elk-stack) | is a distributed, RESTful search and analytics engine to centrally store data
- [Graylog](https://www.graylog.org/) | a leading centralized log management solution built to open standards for capturing, storing, and enabling real-time analysis of terabytes of machine data, built on the top of Elasticsearch and MongoDB.
- [GoAccess](https://goaccess.io/) | an open source real-time web log analyzer and interactive viewer that runs in a terminal in
- [Apache Flume](https://flume.apache.org/) | a distributed, reliable, and available system for efficiently collecting, aggregating and moving large amounts of log data from many different sources to a centralized data store.


# Testing:
---

## Unit Tesing
- [Unit testing as a pattern](https://martinfowler.com/bliki/UnitTest.html) | definition of Unit Tesing

## Integration Tesing
- [Mockito](https://site.mockito.org/) | a java library for functional and internal integration testing
- [Test containers](https://www.testcontainers.org/) | docker for integration testing
- [Arquillian](https://arquillian.org/) | a java library for functional testing
- [Spring boot test](https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-testing.html) | integration tests for Spring Boot apps
- [End-to-end testing](https://martinfowler.com/articles/practical-test-pyramid.html) | designed after the workflows performed by the users, from the beginning to the end
- [Selenium](https://www.seleniumhq.org/) | a framework for UI testing and RPA

## Load testing
- [Apache Jmeter](https://jmeter.apache.org/) | the UI-based approach to create and manage quite sophisticated test plans, designed to load test functional behavior and measure performance.
- [Gatling](https://gatling.io/) | a highly capable load testing tool. It is designed for ease of use, maintainability and high performance
- [Apache Bench](https://httpd.apache.org/docs/current/programs/ab.html) | a cli a tool for benchmarking HTTP-based services and applications.
- [Locust](https://locust.io/) | an easy-to-use, distributed, scalable load testing framework written in Python

## Security testing
- [Sonar Qube](https://www.sonarqube.org/) | an open source platform to perform automatic reviews with static analysis of code to detect bugs, code smells and security vulnerabilities on 25+ programming languages including Java, C#, JavaScript, TypeScript, C/C++, COBOL and more
- [PMD](https://github.com/pmd/pmd) | static analysis of vulnerabilities in source code
- [Find security bugs](https://find-sec-bugs.github.io/) | code security audits for Java
- [Zed Attack Proxy](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project) | used to automatically find security vulnerabilities in web applications
- [XSStrike](https://github.com/s0md3v/XSStrike) | a Cross Site Scripting detection suite equipped with four hand written parsers, an intelligent payload generator, a powerful fuzzing engine and a fast crawler
- [Archery](https://github.com/archerysec/archerysec) | an opensource vulnerability assessment and management tool which helps developers and pentesters to perform scans and manage vulnerabilities. Archery uses popular opensource tools to perform comprehensive scanning for web application and network.
- [Security Monkey](https://github.com/Netflix/security_monkey) | monitors your AWS and GCP accounts for policy changes and alerts on insecure configurations

## Chaos Engineering
- [Principles of chaos](https://principlesofchaos.org/) | definition of Chaos Engineering
- [Chaos Engineering intro](https://blog.codecentric.de/en/2018/07/chaos-engineering/) | a very good intro




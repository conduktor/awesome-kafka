# Awesome Kafka [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of awesome Apache Kafka resources, tools, libraries, and applications.

> **Last verified:** December 31, 2025
>
> **Legend:** ⚠️ Inactive (no commits in 2+ years) · 📦 Archived

> See also: [awesome-kafka-connect](https://github.com/conduktor/awesome-kafka-connect) - A comprehensive list of Kafka Connect connectors
>
> See also: [Kafka Security Controls](https://conduktor.github.io/kafka-security-controls/) - Kafka security controls mapping to CWE, NIST 800-53, and PCI-DSS standards. Integrates with OpenCRE.

- [Awesome Kafka](#awesome-kafka)
  - [Kafka](#kafka)
  - [Clients](#clients)
  - [Stream Processing](#stream-processing)
  - [Kafka Connect](#kafka-connect)
  - [Schema Registry](#schema-registry)
  - [Management & Monitoring](#management--monitoring)
  - [CLI Tools](#cli-tools)
  - [Security](#security)
  - [Testing & Development](#testing--development)
  - [Observability & Tracing](#observability--tracing)
  - [Kafka on Kubernetes](#kafka-on-kubernetes)
  - [Use Cases & Case Studies](#use-cases--case-studies)
  - [Best Practices & Patterns](#best-practices--patterns)
  - [Troubleshooting & Performance](#troubleshooting--performance)
  - [Internals & Architecture](#internals--architecture)
  - [Disaster Recovery](#disaster-recovery)
  - [Migration Guides](#migration-guides)
  - [AI/ML Integration](#aiml-integration)
  - [Data Lakehouse Integration](#data-lakehouse-integration)
  - [Notable KIPs](#notable-kips)
  - [Kafka-Compatible Alternatives](#kafka-compatible-alternatives)
  - [Managed Services](#managed-services)
  - [Learning Resources](#learning-resources)
  - [Conferences & Events](#conferences--events)
  - [Newsletters & Community](#newsletters--community)
  - [Books](#books)

## Kafka

- [Apache Kafka](https://kafka.apache.org/) - Distributed event streaming platform capable of handling trillions of events a day.
- [Kafka Documentation](https://kafka.apache.org/documentation/) - Official documentation covering architecture, APIs, and operations.
- [Kafka Quickstart](https://kafka.apache.org/quickstart/) - Get up and running with Kafka in minutes.
- [KIPs](https://cwiki.apache.org/confluence/display/KAFKA/Kafka+Improvement+Proposals) - Kafka Improvement Proposals tracking upcoming features and changes.

## Clients

### Java
- [Apache Kafka Client](https://github.com/apache/kafka) - Official Java client with Producer, Consumer, Streams, and Admin APIs.
- [Spring for Apache Kafka](https://spring.io/projects/spring-kafka) - Spring Boot integration for Kafka producers, consumers, and transactions.
- [Vert.x Kafka Client](https://vertx.io/docs/vertx-kafka-client/java/) - Reactive Kafka client for Vert.x applications.
- [SmallRye Reactive Messaging](https://smallrye.io/smallrye-reactive-messaging/) - MicroProfile reactive messaging with first-class Kafka connector used by Quarkus and Helidon.

### C/C++
- [librdkafka](https://github.com/confluentinc/librdkafka) - High-performance C/C++ library, foundation for many language bindings.
- [cppkafka](https://github.com/mfontanini/cppkafka) - Modern C++11 wrapper for librdkafka.

### Python
- [confluent-kafka-python](https://github.com/confluentinc/confluent-kafka-python) - High-performance client based on librdkafka with AsyncIO support.
- [aiokafka](https://github.com/aio-libs/aiokafka) - Native asyncio client for Python async applications.
- [kafka-python](https://github.com/dpkp/kafka-python) - Pure Python client (not actively maintained).
- [Faust](https://github.com/faust-streaming/faust) - Stream processing library, Python equivalent of Kafka Streams.

### Go
- [franz-go](https://github.com/twmb/franz-go) - Feature-complete high-performance pure Go client.
- [kafka-go](https://github.com/segmentio/kafka-go) - Go-idiomatic Kafka library by Segment.
- [Sarama](https://github.com/IBM/sarama) - Most popular Go client, pure Go implementation.
- [confluent-kafka-go](https://github.com/confluentinc/confluent-kafka-go) - CGo wrapper around librdkafka with official Confluent support.

### Rust
- [rust-rdkafka](https://github.com/fede1024/rust-rdkafka) - Async futures-based client built on librdkafka.
- [kafka-rust](https://github.com/kafka-rust/kafka-rust) - Pure Rust Kafka protocol implementation.

### Node.js / TypeScript
- [confluent-kafka-javascript](https://github.com/confluentinc/confluent-kafka-javascript) - Official Confluent client with TypeScript support.
- [KafkaJS](https://github.com/tulios/kafkajs) - Pure JavaScript client with clean API (not actively maintained).
- [node-rdkafka](https://github.com/Blizzard/node-rdkafka) - Node.js bindings for librdkafka.

### .NET / C#
- [confluent-kafka-dotnet](https://github.com/confluentinc/confluent-kafka-dotnet) - Official .NET client based on librdkafka.
- [KafkaFlow](https://github.com/Farfetch/KafkaFlow) - High-level .NET framework for building Kafka applications.
- [Streamiz](https://github.com/LGouellec/kafka-streams-dotnet) - Kafka Streams implementation for .NET.

### Ruby
- [rdkafka-ruby](https://github.com/karafka/rdkafka-ruby) - Modern Ruby client based on librdkafka.
- [Karafka](https://github.com/karafka/karafka) - Ruby and Rails framework for Kafka with Web UI.
- [ruby-kafka](https://github.com/zendesk/ruby-kafka) - Pure Ruby client (deprecated).

### PHP
- [php-rdkafka](https://github.com/arnaud-lb/php-rdkafka) - PHP extension wrapping librdkafka.
- [enqueue/rdkafka](https://github.com/php-enqueue/rdkafka) - Queue Interop compliant PHP wrapper.

### Scala
- [Alpakka Kafka](https://github.com/akka/alpakka-kafka) - Reactive Streams connector for Akka Streams.
- [ZIO Kafka](https://github.com/zio/zio-kafka) - ZIO-based Kafka client for functional Scala.
- ⚠️ [Greyhound](https://github.com/wix/greyhound) - Wix's high-level Kafka SDK with ZIO, used in 1,500+ microservices.

### Kotlin
- [kotlin-kafka](https://github.com/nomisRev/kotlin-kafka) - Kotlin Coroutines and Arrow integration for Kafka.

### Elixir / Erlang
- [brod](https://github.com/kafka4beam/brod) - Robust Erlang/Elixir client with consumer groups support.
- [Kaffe](https://github.com/spreedly/kaffe) - Opinionated Elixir wrapper around brod.
- [KafkaEx](https://github.com/kafkaex/kafka_ex) - Pure Elixir Kafka client.

### Swift
- [swift-kafka-client](https://github.com/swift-server/swift-kafka-client) - Swift Server Working Group client with modern concurrency.

### Clojure
- [Jackdaw](https://github.com/FundingCircle/jackdaw) - Comprehensive Kafka library for Clojure.
- ⚠️ [kafka.clj](https://github.com/helins/kafka.clj) - Clojure wrapper with Kafka Streams support.

### Haskell
- [hw-kafka-client](https://github.com/haskell-works/hw-kafka-client) - Haskell client based on librdkafka.

### HTTP / REST
- [Kafka REST Proxy](https://github.com/confluentinc/kafka-rest) - RESTful interface to produce and consume messages via HTTP.
- [Strimzi Kafka Bridge](https://github.com/strimzi/strimzi-kafka-bridge) - HTTP and AMQP bridge for Kubernetes.

## Stream Processing

### Kafka-Native
- [Kafka Streams](https://kafka.apache.org/documentation/streams/) - Client library for building stream processing applications.
- [ksqlDB](https://ksqldb.io/) - Event streaming database with SQL interface built on Kafka Streams.
- [Interactive Queries](https://docs.confluent.io/platform/current/streams/developer-guide/interactive-queries.html) - Query state stores in Kafka Streams applications.
- [StreamT](https://github.com/conduktor/streamt) - Conduktor's dbt for streaming, transforming data in Kafka with SQL.

### Frameworks
- [Apache Flink](https://flink.apache.org/) - Distributed stream processing framework with exactly-once semantics.
- [Apache Spark Streaming](https://spark.apache.org/streaming/) - Micro-batch stream processing on Spark.
- [Apache Samza](https://samza.apache.org/) - Stream processing framework with deep Kafka integration.
- [Apache Storm](https://storm.apache.org/) - Distributed real-time computation system.
- [Apache Beam](https://beam.apache.org/) - Unified batch and streaming API portable across runners.

### Streaming Databases
- [RisingWave](https://github.com/risingwavelabs/risingwave) - PostgreSQL-compatible streaming database with materialized views.
- [Materialize](https://github.com/MaterializeInc/materialize) - Streaming database with incremental view maintenance.
- [Apache Pinot](https://pinot.apache.org/) - Real-time OLAP datastore with sub-second queries on Kafka topics.
- [Apache Druid](https://druid.apache.org/) - Distributed data store for real-time analytics with Kafka ingestion.
- [Timeplus Proton](https://github.com/timeplus-io/proton) - Fast streaming SQL engine for real-time analytics.
- [DeltaStream](https://deltastream.io/) - Serverless stream processing using Flink SQL (commercial).
- [StarRocks](https://docs.starrocks.io/en-us/latest/loading/RoutineLoad) - MPP database with continuous Kafka routine load for lakehouse analytics.

### Python Libraries
- [Faust](https://github.com/faust-streaming/faust) - Stream processing library porting Kafka Streams to Python.
- [Quix Streams](https://github.com/quixio/quix-streams) - Python library for high-volume time-series streaming.
- [Bytewax](https://github.com/bytewax/bytewax) - Python stream processing with Rust performance.
- [Pathway](https://github.com/pathwaycom/pathway) - Python ETL framework with Rust engine for real-time processing.
- [kstreams](https://github.com/kpn/kstreams) - Lightweight Kafka Streams implementation for Python.

### Other
- [Hazelcast](https://hazelcast.com/) - In-memory data grid with Jet stream processing engine.
- [Redpanda Connect](https://github.com/redpanda-data/connect) - Declarative stream processor with 100+ connectors (formerly Benthos).

## Kafka Connect

### CDC (Change Data Capture)
- [Debezium](https://debezium.io/) - CDC platform for MySQL, PostgreSQL, MongoDB, SQL Server, Oracle, and more.

### Databases
- [JDBC Connector](https://www.confluent.io/hub/confluentinc/kafka-connect-jdbc) - Source and sink for JDBC-compatible databases.
- [MongoDB Connector](https://www.mongodb.com/docs/kafka-connector/current/) - Official MongoDB source and sink connector.
- [Neo4j Connector](https://neo4j.com/docs/kafka/current/) - Source and sink for Neo4j graph database.
- [Redis Sink](https://github.com/jcustenborder/kafka-connect-redis) - Write data to Redis.
- [ClickHouse Sink](https://github.com/ClickHouse/clickhouse-kafka-connect) - Official ClickHouse connector.

### Cloud Storage
- [S3 Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-s3) - Export data to Amazon S3 in Avro, JSON, or Parquet.

### Data Warehouses
- [BigQuery Sink](https://www.confluent.io/hub/wepay/kafka-connect-bigquery) - Stream data to Google BigQuery with upsert support.
- [Snowflake Sink](https://docs.snowflake.com/en/user-guide/kafka-connector) - Official Snowflake connector with Iceberg support.

### Message Queues
- [JMS Source & Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-jms) - Bridge JMS providers to Kafka topics.

### IoT & Protocols
- [MQTT Connector](https://github.com/johanvandevenne/kafka-connect-mqtt) - Community MQTT source and sink connector for brokers and devices.

### File Transfer
- [SFTP/FTP Source](https://www.confluent.io/hub/confluentinc/kafka-connect-sftp) - Stream files from SFTP/FTP servers into Kafka.

### HTTP & APIs
- [HTTP Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-http) - Send data to HTTP endpoints.
- [HTTP Source](https://github.com/castorm/kafka-connect-http) - Poll HTTP APIs as a Kafka source.
- [WebSocket Source](https://github.com/conduktor/kafka-connect-websocket) - Stream messages from WebSocket endpoints into Kafka.
- [gRPC Source](https://github.com/conduktor/kafka-connect-grpc) - Consume gRPC server-streaming endpoints directly into Kafka topics.

### Observability
- [Splunk Sink](https://www.confluent.io/hub/splunk/kafka-connect-splunk) - Send events to Splunk.
- [OpenTelemetry OTLP Source](https://github.com/conduktor/kafka-connect-opentelemetry) - Receive OTLP traces/metrics/logs and publish them to Kafka topics.

### Tools & Utilities
- [Confluent Hub](https://www.confluent.io/hub/) - Official connector marketplace.
- [Lenses Stream Reactor](https://github.com/lensesio/stream-reactor) - Collection of 25+ open-source connectors.
- [Kafka Connect Datagen](https://github.com/confluentinc/kafka-connect-datagen) - Generate mock data for testing.
- [Voluble](https://github.com/MichaelDrogalis/voluble) - Realistic data generator for Kafka Connect.
- [Spooldir Source](https://github.com/jcustenborder/kafka-connect-spooldir) - Monitor directories for new files.

## Schema Registry

### Implementations
- [Confluent Schema Registry](https://github.com/confluentinc/schema-registry) - Industry standard with Avro, Protobuf, and JSON Schema support.
- [Karapace](https://github.com/Aiven-Open/karapace) - Open-source drop-in replacement for Confluent Schema Registry (Apache 2.0).
- [Apicurio Registry](https://github.com/Apicurio/apicurio-registry) - Multi-format registry supporting OpenAPI, AsyncAPI, GraphQL, Avro, Protobuf.
- [AWS Glue Schema Registry](https://docs.aws.amazon.com/glue/latest/dg/schema-registry.html) - Serverless registry for AWS with Avro and JSON Schema.
- [Redpanda Schema Registry](https://docs.redpanda.com/current/manage/schema-registry/) - Built-in schema registry in Redpanda.

### Serialization
- [Apache Avro](https://avro.apache.org/) - Compact binary format with rich schema evolution support.
- [Protocol Buffers](https://protobuf.dev/) - Google's binary serialization with strong typing.
- [Buf](https://buf.build/) - Modern Protobuf toolchain with linting and breaking change detection.

## Management & Monitoring

### Web UIs
- [Kafka UI](https://github.com/provectus/kafka-ui) - Free open-source UI for managing Kafka clusters, topics, and consumers.
- [Kafbat UI](https://github.com/kafbat/kafka-ui) - Community fork of Kafka UI with active development.
- [Redpanda Console](https://github.com/redpanda-data/console) - Developer-friendly UI with time-travel debugging.
- [AKHQ](https://github.com/tchiotludo/akhq) - Kafka GUI for topics, consumer groups, Schema Registry, and Connect.
- [Kafdrop](https://github.com/obsidiandynamics/kafdrop) - Lightweight web UI for viewing Kafka topics and consumer groups.
- ⚠️ [CMAK](https://github.com/yahoo/CMAK) - Cluster Manager for Apache Kafka by Yahoo.
- [Kouncil](https://github.com/Consdata/kouncil) - Modern web interface with advanced message browsing.
- [Conduktor Console](https://conduktor.io/) - Enterprise control plane for Kafka with access control (commercial).
- [Lenses](https://lenses.io/) - DataOps platform with SQL Studio and data policies (commercial).
- [kPow](https://factorhouse.io/kpow/) - Enterprise Kafka monitoring with RBAC and audit logging (commercial).
- [Confluent Control Center](https://www.confluent.io/product/confluent-platform/) - Monitoring and management for Confluent Platform (commercial).

### Metrics & Exporters
- [Burrow](https://github.com/linkedin/Burrow) - LinkedIn's consumer lag checking and monitoring service.
- [Kafka Exporter](https://github.com/danielqsj/kafka_exporter) - Prometheus exporter for Kafka broker and consumer group metrics.
- [JMX Exporter](https://github.com/prometheus/jmx_exporter) - Prometheus exporter for JMX metrics from Kafka brokers.
- [KMinion](https://github.com/redpanda-data/kminion) - Prometheus exporter for consumer lag and log directory sizes.
- 📦 [Kafka Lag Exporter](https://github.com/seglo/kafka-lag-exporter) - Consumer group latency exporter for Kubernetes.
- [Grafana Kafka Dashboards](https://grafana.com/grafana/dashboards/7589-kafka-overview/) - Curated Grafana dashboards for Kafka broker, topic, and consumer metrics.

### Cluster Management
- [Strimzi](https://strimzi.io/) - Kubernetes operator for running Apache Kafka (CNCF Incubating).
- [Cruise Control](https://github.com/linkedin/cruise-control) - LinkedIn's automated workload rebalancer and self-healing.
- [Cruise Control UI](https://github.com/linkedin/cruise-control-ui) - Web interface for Cruise Control operations.
- [MirrorMaker 2](https://kafka.apache.org/documentation/#georeplication) - Built-in cross-cluster replication using Kafka Connect.
- [Jikkou](https://github.com/streamthoughts/jikkou) - GitOps tool for managing Kafka resources as code.
- [Kafka-Kit](https://github.com/DataDog/kafka-kit) - Datadog's tools for partition mapping, rebalancing, and auto-throttling.

### Infrastructure as Code
- [Terraform Provider for Kafka](https://github.com/Mongey/terraform-provider-kafka) - Manage Kafka topics, ACLs, and quotas with Terraform.
- [Confluent Terraform Provider](https://github.com/confluentinc/terraform-provider-confluent) - Terraform provider for Confluent Cloud resources including Kafka clusters.
- [Conduktor Terraform Provider](https://registry.terraform.io/providers/conduktor/conduktor/latest/docs) - Provision Conduktor Kafka Console resources (workspaces, RBAC, environments) via Terraform.

### Interactive Tools
- [Kafka Options Explorer](https://kafka-options-explorer.conduktor.io/) - Browse and compare Kafka configuration options across versions.

## CLI Tools

- [kcat](https://github.com/edenhill/kcat) - Swiss army knife for Kafka, formerly kafkacat.
- [kafkactl](https://github.com/deviceinsight/kafkactl) - Command-line tool inspired by kubectl with auto-completion.
- [kaf](https://github.com/birdayz/kaf) - Modern CLI for Kafka inspired by kubectl and docker.
- [Zoe](https://github.com/adevinta/zoe) - CLI for humans with time-based consumption and filtering.
- ⚠️ [kcli](https://github.com/cswank/kcli) - Simple Kafka command line browser.
- [trubka](https://github.com/xitonix/trubka) - CLI tool for Kafka with Protobuf support.
- [topicctl](https://github.com/segmentio/topicctl) - Tool for managing Kafka topics with YAML configs.
- ⚠️ [kafka-shell](https://github.com/devshawn/kafka-shell) - Interactive shell for Apache Kafka.

## Security

### Authentication & Authorization
- [Strimzi OAuth](https://github.com/strimzi/strimzi-kafka-oauth) - OAuth2/OIDC authentication for Kafka.
- [Apache Ranger](https://ranger.apache.org/) - Fine-grained authorization and centralized policy management.
- ⚠️ [Kafka Security Manager](https://github.com/conduktor/kafka-security-manager) - Git-based ACL management with auto-revert by Conduktor.
- [Julie](https://github.com/kafka-ops/julie) - GitOps for Kafka RBAC and topologies.
- ⚠️ [kafka-gitops](https://github.com/devshawn/kafka-gitops) - Manage Kafka resources as code with Git.

### Encryption
- ⚠️ [kafka-end-2-end-encryption](https://github.com/salyh/kafka-end-2-end-encryption) - Transparent AES encryption for Kafka messages.
- [kafkacrypto](https://github.com/tmcqueen-materials/kafkacrypto) - End-to-end encryption library for Python and Java.

### Governance
- [Apache Atlas](https://atlas.apache.org/) - Metadata management and data lineage for Kafka.
- [DataHub](https://datahubproject.io/) - Modern data catalog with Kafka metadata and lineage support.
- [OpenMetadata](https://open-metadata.org/) - Open-source metadata platform with Kafka integration.

### Proxies & Gateways
- [Conduktor Gateway](https://conduktor.io/gateway/) - Kafka proxy with encryption, masking, and policy enforcement (commercial).
- [Kroxylicious](https://github.com/kroxylicious/kroxylicious) - Java framework for building Kafka protocol proxies.
- [Gloo Gateway](https://www.solo.io/products/gloo-gateway/) - Kubernetes-native API gateway with Kafka support.
- [Apache APISIX](https://apisix.apache.org/) - API gateway with kafka-proxy plugin.

## Testing & Development

### Local Development
- [Kafka Docker](https://github.com/conduktor/kafka-stack-docker-compose) - Docker Compose for Kafka ecosystem by Conduktor.
- [cp-all-in-one](https://github.com/confluentinc/cp-all-in-one) - Confluent Platform Docker Compose files.
- [kafka-local](https://github.com/factorhouse/kafka-local) - Minimal Docker setup for local Kafka development.
- [Redpanda](https://github.com/redpanda-data/redpanda) - Kafka-compatible broker ideal for local development (no JVM).

### Testing Frameworks
- [Testcontainers Kafka](https://java.testcontainers.org/modules/kafka/) - Automated Kafka containers for integration tests.
- [Spring Kafka Test](https://spring.io/projects/spring-kafka) - Embedded Kafka for Spring Boot applications.
- [kafka-junit](https://github.com/salesforce/kafka-junit) - JUnit 4 and 5 support for embedded Kafka tests.
- [embedded-kafka](https://github.com/embeddedkafka/embedded-kafka) - Embedded Kafka for Scala testing with ScalaTest support.
- [TopologyTestDriver](https://kafka.apache.org/documentation/streams/developer-guide/testing.html) - In-memory testing for Kafka Streams topologies.
- [Toxiproxy](https://github.com/Shopify/toxiproxy) - Simulate network conditions for resilience testing.

### Data Generation
- [Kafka Connect Datagen](https://github.com/confluentinc/kafka-connect-datagen) - Generate mock data based on Avro schemas.
- ⚠️ [Voluble](https://github.com/MichaelDrogalis/voluble) - Realistic relational data generator for Kafka.
- 📦 [Datagen](https://github.com/MaterializeInc/datagen) - Multi-format data generator by Materialize.
- [Mockingbird](https://github.com/tinybirdco/mockingbird) - Mock streaming data generator.
- [DataFaker](https://github.com/datafaker-net/datafaker) - Java library for generating realistic fake data.

### Benchmarking
- [kafka-producer-perf-test](https://kafka.apache.org/documentation/#basic_ops_producer_perf) - Built-in producer performance testing tool.
- [kafka-consumer-perf-test](https://kafka.apache.org/documentation/#basic_ops_consumer_perf) - Built-in consumer performance testing tool.
- [OpenMessaging Benchmark](https://github.com/openmessaging/benchmark) - Cross-platform messaging system benchmarking.
- ⚠️ [Sangrenel](https://github.com/jamiealquiza/sangrenel) - Kafka cluster load testing tool.

### Chaos Engineering
- [LitmusChaos Kafka Experiments](https://litmuschaos.io/) - Chaos experiments for Kafka brokers, ZooKeeper/KRaft, and clients.
- [Steadybit Kafka Attacks](https://www.steadybit.com/integrations/kafka) - Fault injection scenarios targeting Kafka brokers and client latency.
- [Conduktor Chaos Testing via Gateway](https://docs.conduktor.io/guide/use-cases/chaos-testing) - Inject latency and failures through Conduktor Kafka proxy to validate resilience.

### IDE Plugins
- [IntelliJ Kafka Plugin](https://plugins.jetbrains.com/plugin/11645-kafka) - Official JetBrains plugin for Kafka.
- [Kafkalytic](https://plugins.jetbrains.com/plugin/11946-kafkalytic) - IntelliJ plugin with message search and filtering.
- [Confluent for VS Code](https://marketplace.visualstudio.com/items?itemName=confluentinc.vscode-confluent) - Official Confluent extension for VS Code.
- [Tools for Apache Kafka](https://marketplace.visualstudio.com/items?itemName=jeppeandersen.vscode-kafka) - VS Code extension for Kafka development.

## Observability & Tracing

### OpenTelemetry
- [Instrumenting Kafka Clients with OpenTelemetry](https://opentelemetry.io/blog/2022/instrument-kafka-clients/) - Official OpenTelemetry guide for Kafka instrumentation.
- [Kafka with OpenTelemetry Guide](https://last9.io/blog/kafka-with-opentelemetry/) - Comprehensive distributed tracing setup guide.
- [Tracing Kafka with OpenTelemetry](https://www.instaclustr.com/blog/tracing-apache-kafka-with-opentelemetry/) - Practical instrumentation tutorial.
- [Distributed Tracing for Kafka](https://newrelic.com/blog/how-to-relic/distributed-tracing-with-kafka) - New Relic's OpenTelemetry integration guide.
- [Strimzi OpenTelemetry Support](https://strimzi.io/blog/2023/03/01/opentelemetry/) - From OpenTracing to OpenTelemetry in Strimzi.

### Collectors & Pipelines
- [OpenTelemetry Collector Kafka Receiver/Exporter](https://github.com/open-telemetry/opentelemetry-collector-contrib/tree/main/receiver/kafkareceiver) - Ingest and ship traces, metrics, and logs through Kafka pipelines.
- [Vector](https://vector.dev/) - High-performance observability pipeline with Kafka sources and sinks for logs, metrics, and traces.

### Tracing Backends
- [Jaeger](https://www.jaegertracing.io/) - Open-source distributed tracing platform.
- [Zipkin](https://zipkin.io/) - Distributed tracing system for gathering timing data.
- [Grafana Tempo](https://grafana.com/oss/tempo/) - High-scale distributed tracing backend.

## Kafka on Kubernetes

### Operators
- [Strimzi](https://strimzi.io/) - CNCF Incubating Kubernetes operator for Apache Kafka.
- [Confluent for Kubernetes](https://docs.confluent.io/operator/current/overview.html) - Official Confluent operator for deploying Confluent Platform.
- 📦 [Koperator](https://github.com/banzaicloud/koperator) - Banzai Cloud's Kubernetes operator for Kafka (formerly Kafka Operator).

### Helm Charts
- 📦 [Confluent Platform Helm Charts](https://github.com/confluentinc/cp-helm-charts) - Helm charts for Confluent Platform components.
- [Bitnami Kafka Chart](https://github.com/bitnami/charts/tree/main/bitnami/kafka) - Production-ready Kafka Helm chart.
- [Strimzi Helm Charts](https://strimzi.io/docs/operators/latest/deploying.html#deploying-cluster-operator-helm-chart-str) - Helm-based Strimzi installation.

### Resources
- [Running Kafka on Kubernetes at Shopify](https://shopify.engineering/running-apache-kafka-on-kubernetes-at-shopify) - Shopify's Kubernetes migration journey.
- [Kafka on Kubernetes Best Practices](https://www.confluent.io/blog/apache-kafka-kubernetes-best-practices/) - Confluent's production recommendations.

## Use Cases & Case Studies

### Enterprise Scale
- [PayPal: Scaling Kafka to 1.3 Trillion Messages/Day](https://medium.com/paypal-tech/scaling-kafka-to-support-paypals-data-growth-a0b4da420fab) - How PayPal runs 85+ clusters with 1,500 brokers processing trillions of messages.
- [LinkedIn: 7 Trillion Messages Per Day](https://engineering.linkedin.com/blog/2019/apache-kafka-trillion-messages) - LinkedIn's Kafka customizations with 100+ clusters and 4,000+ brokers.
- [Cloudflare: 1 Trillion Inter-Service Messages](https://blog.cloudflare.com/using-apache-kafka-to-process-1-trillion-messages/) - How Cloudflare uses Kafka for analytics, DDoS mitigation, and logging.
- [Netflix: Keystone Pipeline](https://www.confluent.io/blog/how-kafka-is-used-by-netflix/) - Netflix's real-time personalization processing 2 trillion messages/day.
- [Uber: Trillion Events Per Day](https://www.slideshare.net/Hadoop_Summit/how-uber-scaled-its-real-time-infrastructure-to-trillion-events-per-day) - Uber's real-time infrastructure for driver-rider matching and fraud detection.
- [Pinterest: 1.2 Petabytes Per Day](https://medium.com/pinterest-engineering/how-pinterest-runs-kafka-at-scale-ff9c6f735be) - Running 2,000+ brokers for real-time streaming applications.
- [Airbnb: Riverbed Framework](https://www.infoq.com/news/2023/10/airbnb-riverbed-introduction/) - Processing 2.4 billion events daily with Kafka and Spark.
- [Twitter: Kafka Adoption Story](https://blog.x.com/engineering/en_us/topics/insights/2018/twitters-kafka-adoption-story) - Twitter's migration from EventBus to Kafka with 68-75% resource savings.
- [Stripe: 6 Nines Availability](https://www.confluent.io/events/kafka-summit-london-2022/6-nines-how-stripe-keeps-kafka-highly-available-across-the-globe/) - How Stripe achieves 99.9999% uptime with 700TB daily throughput.
- [Slack: Self-Driving Kafka Clusters](https://slack.engineering/building-self-driving-kafka-clusters-using-open-source-components/) - Slack's Kafka powering job queues, logging, and analytics at 6.5Gbps.
- [Shopify: Billions of Events](https://shopify.engineering/capturing-every-change-shopify-sharded-monolith) - CDC with Debezium handling 66M messages/second at peak.
- [DoorDash: 100 Billion Events](https://www.infoq.com/presentations/doordash-event-system/) - Iguazu pipeline processing billions of events with Kafka and Flink.
- [Datadog: Trillions of Datapoints](https://www.datadoghq.com/blog/kafka-at-datadog/) - Running 40+ clusters with petabytes of NVMe storage.
- [Instacart: COVID-19 Scale](https://www.confluent.io/customers/instacart/) - 10 years of growth in 6 weeks during pandemic surge.
- [Lyft: Real-Time Pricing](https://www.confluent.io/resources/kafka-summit-2020/can-kafka-handle-a-lyft-ride/) - Kafka for map-matching, ETA, and dynamic pricing.

### Architecture Patterns
- [Wix: 6 Event-Driven Architecture Patterns (Part 1)](https://medium.com/wix-engineering/6-event-driven-architecture-patterns-part-1-93758b253f47) - Patterns from running 1,500 microservices on Kafka.
- [Wix: 6 Event-Driven Architecture Patterns (Part 2)](https://medium.com/wix-engineering/6-event-driven-architecture-patterns-part-2-455cc73b22e1) - Advanced patterns including retry strategies and dead-letter queues.
- [Kai Waehner: Use Cases Across Industries](https://www.kai-waehner.de/blog/2020/10/20/apache-kafka-event-streaming-use-cases-architectures-examples-real-world-across-industries/) - Comprehensive overview of Kafka use cases by industry.
- [Kafka in Production](https://github.com/dttung2905/kafka-in-production) - Curated collection of tech blogs and talks from companies running Kafka.

## Best Practices & Patterns

### Event Sourcing & CQRS
- [Event Sourcing, CQRS, and Kafka](https://www.confluent.io/blog/event-sourcing-cqrs-stream-processing-apache-kafka-whats-connection/) - How Kafka enables event sourcing and CQRS patterns.
- [CQRS in Event Sourcing Patterns](https://developer.confluent.io/courses/event-sourcing/cqrs/) - Confluent Developer course on implementing CQRS with Kafka.
- [Microservices: Event Sourcing & CQRS](https://microservices.io/patterns/data/event-sourcing.html) - Pattern catalog entry for event sourcing.

### Exactly-Once Semantics
- [Exactly-Once Semantics in Kafka](https://www.confluent.io/blog/exactly-once-semantics-are-possible-heres-how-apache-kafka-does-it/) - Deep dive into how Kafka achieves exactly-once.
- [Exactly-Once Processing with Kafka](https://www.baeldung.com/kafka-exactly-once) - Baeldung guide with Java code examples.
- [Idempotent Consumer Pattern](https://medium.com/@zdb.dashti/exactly-once-semantics-using-the-idempotent-consumer-pattern-927b2595f231) - Implementing idempotency for exactly-once semantics.
- [What Exactly-Once Really Means](https://softwaremill.com/what-kafka-exactly-once-really-means/) - Clarifying the semantics and limitations.

### Partitioning Strategies
- [Kafka Topic Partitioning Strategies](https://newrelic.com/blog/best-practices/effective-strategies-kafka-topic-partitioning) - Best practices from New Relic.
- [Partition Strategy Guide](https://www.confluent.io/learn/kafka-partition-strategy/) - Confluent's comprehensive partitioning guide.
- [Ultimate Comparison of Partition Strategies](https://risingwave.com/blog/the-ultimate-comparison-of-kafka-partition-strategies-everything-you-need-to-know/) - Detailed comparison of all partitioning approaches.

### Transactional Outbox Pattern
- [Reliable Microservices Data Exchange with the Outbox Pattern](https://debezium.io/blog/2019/02/19/reliable-microservices-data-exchange-with-the-outbox-pattern/) - Debezium's foundational outbox pattern guide.
- [Debezium Outbox Event Router](https://debezium.io/documentation/reference/stable/transformations/outbox-event-router.html) - Official Debezium outbox SMT documentation.
- [Implementing Outbox Pattern with CDC](https://thorben-janssen.com/outbox-pattern-with-cdc-and-debezium/) - Practical implementation guide.
- [Transactional Outbox at SeatGeek](https://chairnerd.seatgeek.com/transactional-outbox-pattern/) - Real-world production implementation.
- [Outbox with Debezium: Hidden Challenges](https://medium.com/yotpoengineering/outbox-with-debezium-and-kafka-the-hidden-challenges-998c00487ae4) - Lessons learned at Yotpo.

### Schema Evolution
- [Schema Evolution and Compatibility](https://docs.confluent.io/platform/current/schema-registry/fundamentals/schema-evolution.html) - Official Confluent schema evolution guide.
- [Schema Registry Best Practices](https://www.confluent.io/blog/best-practices-for-confluent-schema-registry/) - Confluent's recommendations for schema management.
- [Schema Evolution in Kafka](https://www.everythingdevops.dev/blog/schema-evolution-in-kafka) - Comprehensive guide to backward and forward compatibility.
- [Schema Compatibility Testing](https://developer.confluent.io/courses/schema-registry/schema-compatibility/) - Confluent course on testing schema compatibility.
- [Handling Schema Evolution in Kafka Connect](https://medium.com/cloudnativepub/handling-schema-evolution-in-kafka-connect-patterns-pitfalls-and-practices-391795d7d8b0) - Patterns and pitfalls guide.

## Troubleshooting & Performance

### Consumer Lag
- [Kafka Consumer Lag Explained](https://dattell.com/data-architecture-blog/kafka-consumer-lag-explained/) - Understanding and monitoring consumer lag.
- [Fixing Consumer Lag Guide](https://last9.io/blog/fixing-kafka-consumer-lag/) - Practical guide to diagnosing and fixing lag.
- [Kafka Lag Causes and Solutions](https://www.redpanda.com/guides/kafka-performance-kafka-lag) - Comprehensive lag troubleshooting.
- [Consumer Lag Monitoring](https://sematext.com/blog/kafka-consumer-lag-offsets-monitoring/) - Setting up lag monitoring with offsets.

### Performance Tuning
- [7 Critical Kafka Performance Best Practices](https://www.instaclustr.com/education/apache-kafka/kafka-performance-7-critical-best-practices/) - Essential tuning recommendations.
- [Top 10 Tips for Tuning Performance](https://www.meshiq.com/top-10-tips-for-tuning-kafka-performance/) - meshIQ's performance optimization guide.
- [Kafka Performance Tuning](https://www.redpanda.com/guides/kafka-performance-kafka-performance-tuning) - Redpanda's tuning strategies.
- [Kafka Optimization Theorem](https://developers.redhat.com/articles/2022/05/03/fine-tune-kafka-performance-kafka-optimization-theorem) - Red Hat's mathematical approach to tuning.
- [Producer and Consumer Tuning](https://www.meshiq.com/blog/tuning-kafka-producers-and-consumers-for-maximum-efficiency/) - Fine-tuning client configurations.

### Debugging & Troubleshooting
- [Troubleshooting and Debugging in Kafka](https://www.danielsobrado.com/blog/troubleshooting-and-debugging-in-kafka/) - Comprehensive debugging guide.
- [Common Kafka Performance Issues](https://www.meshiq.com/blog/common-kafka-performance-issues-and-how-to-fix-them/) - Diagnosing and fixing common issues.

## Internals & Architecture

### KRaft (ZooKeeper Replacement)
- [Deep Dive into KRaft Protocol](https://developers.redhat.com/articles/2025/09/17/deep-dive-apache-kafkas-kraft-protocol) - Red Hat's technical deep dive based on Kafka 4.1.0.
- [KRaft Overview](https://developer.confluent.io/learn/kraft/) - Confluent's guide to Kafka Raft mode.
- [Evolution from ZooKeeper to KRaft](https://romanglushach.medium.com/the-evolution-of-kafka-architecture-from-zookeeper-to-kraft-f42d511ba242) - Architectural evolution explained.

### Replication & Consistency
- [Kafka Replication Deep Dive](https://faderskd.github.io/2024-05-15-kafka-replication.html) - Technical deep dive into replication internals.
- [ISR, High Watermark & Leader Epoch](https://shayne007.github.io/2025/06/09/Kafka-ISR-High-Watermark-Leader-Epoch-Deep-Dive-Guide/) - Understanding ISR and consistency guarantees.
- [Replication Documentation](https://docs.confluent.io/kafka/design/replication.html) - Official Confluent replication docs.

### Log Compaction
- [Log Compaction Design](https://docs.confluent.io/kafka/design/log_compaction.html) - Official log compaction documentation.
- [Introduction to Log Compaction](https://medium.com/swlh/introduction-to-topic-log-compaction-in-apache-kafka-3e4d4afd2262) - Beginner-friendly explanation.
- [Log Compaction Troubleshooting](https://www.redpanda.com/guides/kafka-performance-kafka-log-compaction) - Configuration and troubleshooting guide.
- [Compaction in Kafka Topics](https://www.baeldung.com/ops/kafka-topics-compaction) - Baeldung's practical guide.

### How Kafka Works
- [How Kafka Works](https://newsletter.systemdesign.one/p/how-kafka-works) - System design newsletter deep dive.
- [Kafka Architecture Deep Dive](https://developer.confluent.io/courses/architecture/get-started/) - Confluent's architecture course.

## Disaster Recovery

### Multi-Datacenter Patterns
- [Disaster Recovery for Multi-Datacenter Deployments](https://www.confluent.io/blog/disaster-recovery-multi-datacenter-apache-kafka-deployments/) - Confluent's comprehensive DR guide.
- [Active-Passive vs Active-Active Topologies](https://www.automq.com/blog/kafka-replication-topologies-active-passive-vs-active-active) - Comparison of replication patterns.
- [Cross-Data-Center Replication Playbook](https://www.confluent.io/blog/kafka-cross-data-center-replication-decision-playbook/) - Decision framework for geo-replication.
- [Multi-Region Kafka with RPO=0](https://www.kai-waehner.de/blog/2025/08/04/multi-region-kafka-using-synchronous-replication-for-disaster-recovery-with-zero-data-loss-rpo0/) - Achieving zero data loss with synchronous replication.
- [Hitchhiker's Guide to DR and Multi-Region Kafka](https://www.warpstream.com/blog/the-hitchhikers-guide-to-disaster-recovery-and-multi-region-kafka) - WarpStream's comprehensive guide.
- [Building Bulletproof DR for Kafka](https://oso.sh/blog/building-bulletproof-disaster-recovery-for-apache-kafka-a-field-tested-architecture/) - Field-tested architecture patterns.

### Replication Tools
- [MirrorMaker 2](https://kafka.apache.org/documentation/#georeplication) - Built-in cross-cluster replication.
- [Confluent Replicator](https://docs.confluent.io/platform/current/multi-dc-deployments/replicator/index.html) - Enterprise replication with conflict detection.
- [Cluster Linking](https://docs.confluent.io/cloud/current/multi-cloud/cluster-linking/index.html) - Byte-for-byte topic mirroring in Confluent Cloud.

## Migration Guides

### ZooKeeper to KRaft
- [KIP-866: ZooKeeper to KRaft Migration](https://cwiki.apache.org/confluence/display/KAFKA/KIP-866+ZooKeeper+to+KRaft+Migration) - Official migration KIP.
- [Strimzi KRaft Migration](https://strimzi.io/blog/2024/03/21/kraft-migration/) - How the migration works technically.
- [Confluent ZK to KRaft Migration](https://docs.confluent.io/platform/current/installation/migrate-zk-kraft.html) - Confluent Platform migration guide.
- [OSO ZooKeeper to KRaft Guide](https://oso.sh/blog/guide-to-zookeeper-to-kraft-migration/) - Step-by-step migration guide.
- [Strimzi Cluster Migration](https://strimzi.io/blog/2024/03/22/strimzi-kraft-migration/) - Kubernetes-specific migration with Strimzi.

### Cross-Cluster Replication
- [MirrorMaker 2 Guide](https://www.confluent.io/learn/kafka-mirrormaker/) - How to replicate data across clusters.
- [MirrorMaker 2 Best Practices](https://www.automq.com/blog/kafka-mirrormaker-2-usages-best-practices) - Usages and best practices.
- [Migration with MM2 and Strimzi](https://strimzi.io/blog/2021/11/22/migrating-kafka-with-mirror-maker2/) - Kubernetes migration patterns.
- [AWS MSK Migration Guide](https://docs.aws.amazon.com/msk/latest/developerguide/migration.html) - Migrating to Amazon MSK.

## AI/ML Integration

### Feature Stores
- [Online Feature Store with Kafka and Flink](https://www.kai-waehner.de/blog/2025/09/15/online-feature-store-for-ai-and-machine-learning-with-apache-kafka-and-flink/) - Building real-time feature stores.
- [Kafka as a Feature Store](https://www.linkedin.com/pulse/kafka-feature-store-machine-learning-brindha-jeyaraman-yizkc) - Using Kafka for ML feature delivery.

### ML Pipelines
- [Kafka-ML Framework](https://github.com/ertis-research/kafka-ml) - Open-source framework connecting Kafka with TensorFlow and PyTorch.
- [Machine Learning in Kafka Applications](https://www.confluent.io/blog/machine-learning-real-time-analytics-models-in-kafka-applications/) - Deploying ML models with Kafka.
- ⚠️ [Kafka Streams ML Examples](https://github.com/kaiwaehner/kafka-streams-machine-learning-examples) - Examples with H2O, TensorFlow, Keras, and DeepLearning4J.
- [Machine Learning with Kafka](https://oso.sh/blog/machine-learning-with-apache-kafka/) - Patterns for ML integration.

### Online Learning
- [Online Model Training and Model Drift](https://www.kai-waehner.de/blog/2025/02/23/online-model-training-and-model-drift-in-machine-learning-with-apache-kafka-and-flink/) - Continuous model training with Kafka and Flink.

## Data Lakehouse Integration

### Tableflow & Iceberg
- [Confluent Tableflow](https://www.confluent.io/product/tableflow/) - Convert Kafka topics to Iceberg and Delta tables.
- [Tableflow GA Announcement](https://www.confluent.io/blog/tableflow-ga-kafka-snowflake-iceberg/) - Real-time Kafka to Iceberg integration.
- [Apache Iceberg for Lakehouse and Streaming](https://www.kai-waehner.de/blog/2024/07/13/apache-iceberg-the-open-table-format-for-lakehouse-and-data-streaming/) - Iceberg as the bridge between streaming and lakehouse.
- [Tableflow with Trino and Jupyter](https://www.confluent.io/blog/integrating-confluent-tableflow-trino-apache-iceberg-jupyter/) - Querying Kafka data with Trino.

### Data Warehouse Integration
- [Snowflake Kafka Integration Options](https://www.kai-waehner.de/blog/2024/04/22/snowflake-data-integration-options-for-apache-kafka-including-iceberg/) - Snowflake integration patterns including Iceberg.

## Notable KIPs

### KIP-500: ZooKeeper Removal
- [KIP-500: Replace ZooKeeper with Self-Managed Metadata Quorum](https://cwiki.apache.org/confluence/display/KAFKA/KIP-500:+Replace+ZooKeeper+with+a+Self-Managed+Metadata+Quorum) - The foundational KIP for KRaft.
- [42 Ways ZooKeeper Removal Improves Kafka](https://www.confluent.io/blog/42-ways-zookeeper-removal-improves-kafka/) - Benefits of the ZooKeeper-less architecture.
- [Prepare for KIP-500](https://www.confluent.io/blog/how-to-prepare-for-kip-500-kafka-zookeeper-removal-guide/) - Migration preparation guide.

### KIP-1150: Diskless Topics
- [KIP-1150: Diskless Topics](https://cwiki.apache.org/confluence/display/KAFKA/KIP-1150:+Diskless+Topics) - Store data directly in object storage.
- [Kafka Without Disks](https://medium.com/@dobeerman/kafka-without-disks-lets-talk-about-kip-1150-diskless-topics-036d29d9cf7e) - Explanation of diskless topics.
- [Hitchhiker's Guide to Diskless Kafka](https://aiven.io/blog/guide-diskless-apache-kafka-kip-1150) - Aiven's comprehensive guide.
- [Benchmarking Diskless Topics](https://aiven.io/blog/benchmarking-diskless-inkless-topics-part-1) - Performance benchmarks.

### Other Notable KIPs
- [KIP-848: Next-Gen Consumer Group Protocol](https://cwiki.apache.org/confluence/display/KAFKA/KIP-848%3A+The+Next+Generation+of+the+Consumer+Rebalance+Protocol) - Improved consumer rebalancing.
- [KIP-405: Tiered Storage](https://cwiki.apache.org/confluence/display/KAFKA/KIP-405%3A+Kafka+Tiered+Storage) - Move older data to cheaper object storage.
- [Kafka Improvement Proposals Index](https://cwiki.apache.org/confluence/display/KAFKA/Kafka+Improvement+Proposals) - All KIPs.

## Kafka-Compatible Alternatives

- [Redpanda](https://redpanda.com/) - C++ implementation with Kafka API compatibility and 10x lower latency.
- [WarpStream](https://www.warpstream.com/) - Diskless Kafka on object storage, acquired by Confluent (commercial).
- [AutoMQ](https://github.com/AutoMQ/automq) - Cloud-native Kafka with shared storage for 50-90% cost reduction.
- [Bufstream](https://buf.build/product/bufstream) - Kafka-compatible broker with Apache Iceberg integration (commercial).

### Related Message Brokers
- [Apache Pulsar](https://pulsar.apache.org/) - Distributed pub-sub with separated compute and storage.
- [RabbitMQ Streams](https://www.rabbitmq.com/streams.html) - Stream processing extension for RabbitMQ.
- [NATS JetStream](https://nats.io/) - Lightweight cloud-native messaging with persistence.
- [Amazon Kinesis](https://aws.amazon.com/kinesis/) - Fully managed real-time data streaming on AWS.

## Managed Services

- [Confluent Cloud](https://www.confluent.io/confluent-cloud/) - Fully managed Kafka with Kora engine and stream processing.
- [AWS MSK](https://aws.amazon.com/msk/) - Amazon Managed Streaming for Apache Kafka with serverless option.
- [Azure Event Hubs](https://azure.microsoft.com/services/event-hubs/) - Kafka protocol compatible event streaming on Azure.
- [Aiven for Apache Kafka](https://aiven.io/kafka) - Multi-cloud managed Kafka with open-source focus.
- [Instaclustr](https://www.instaclustr.com/products/managed-apache-kafka/) - Managed open-source Kafka with strong compliance.
- [Redpanda Cloud](https://redpanda.com/redpanda-cloud) - Managed Redpanda with BYOC and serverless options.

## Learning Resources

### Courses
- [Kafkademy](https://kafkademy.com/) - Free Kafka learning platform by Conduktor and Stéphane Maarek.
- [Confluent Developer](https://developer.confluent.io/courses/) - Free courses on Kafka, Flink, Kafka Streams, and ksqlDB.
- [Stephane Maarek's Kafka Courses](https://www.udemy.com/user/stephane-maarek/) - Popular Udemy courses covering Kafka fundamentals to advanced topics.
- [Confluent Certified Developer](https://www.confluent.io/certification/) - Official Kafka certification exam.

### Documentation & Tutorials
- [Confluent Documentation](https://docs.confluent.io/) - Comprehensive guides for Confluent Platform and Cloud.
- [Cloudurable Kafka Tutorial](https://cloudurable.com/blog/kafka-tutorial-2025/) - In-depth tutorial covering Kafka 4.0 and KRaft.
- [IBM Kafka Streams Labs](https://ibm-cloud-architecture.github.io/refarch-eda/use-cases/kafka-streams/) - Hands-on Kafka Streams labs.

### Videos & Podcasts
- [Confluent YouTube](https://www.youtube.com/c/Confluent) - Official Confluent channel with tutorials and talks.
- [Kafka Summit / Current](https://www.kafka-summit.org/) - Annual data streaming conference talks.
- [Confluent Developer Podcast](https://confluent.buzzsprout.com/) - Weekly podcast with Kafka experts.

### Community
- [Confluent Community Slack](https://launchpass.com/confluentcommunity) - Active community for Q&A and discussion.
- [Apache Kafka Mailing Lists](https://kafka.apache.org/contact) - Official user and developer mailing lists.
- [Stack Overflow](https://stackoverflow.com/questions/tagged/apache-kafka) - Q&A for Kafka development.
- [Reddit r/apachekafka](https://www.reddit.com/r/apachekafka/) - Community discussions and news.

### Reference
- [Conduktor Data Streaming Glossary](https://conduktor.io/glossary) - Comprehensive glossary of data streaming terminology and concepts.

## Conferences & Events

### Kafka Summit / Current
- [Kafka Summit](https://www.kafka-summit.org/) - The largest annual Apache Kafka conference by Confluent.
- [Current](https://current.confluent.io/) - Confluent's expanded conference covering the broader streaming ecosystem.
- [Kafka Summit London 2024](https://www.confluent.io/events/kafka-summit-london-2024/) - Past sessions and slides.
- [Confluent Events Calendar](https://events.confluent.io/) - Upcoming events and conferences.

### Flink Forward
- [Flink Forward](https://www.flink-forward.org/) - Conference dedicated to Apache Flink and stream processing.
- [Ververica Academy](https://www.ververica.academy/) - Training sessions from Flink Forward conferences.

### Meetups
- [Apache Kafka Meetups](https://www.meetup.com/topics/apache-kafka/) - Local Kafka meetup groups worldwide.
- [Kafka Community Events](https://kafka.apache.org/community/events/) - Official Apache Kafka events page.
- [Meetup in a Box](https://developer.confluent.io/community/meetup-in-a-box/) - Resources for hosting Kafka meetups.

## Newsletters & Community

### Newsletters
- [Confluent Developer Newsletter](https://developer.confluent.io/newsletter/) - Bimonthly newsletter on Kafka, Flink, and streaming.
- [Kai Waehner's Blog](https://www.kai-waehner.de/blog/) - Data streaming insights and architecture patterns.
- [ByteByteGo Newsletter](https://blog.bytebytego.com/) - System design newsletter with frequent Kafka content.
- [System Design Newsletter](https://newsletter.systemdesign.one/) - Deep dives on distributed systems including Kafka.

### Podcasts
- [Confluent Developer Podcast](https://confluent.buzzsprout.com/) - Weekly podcast with Kafka experts and practitioners.
- [Software Engineering Daily: Kafka](https://softwareengineeringdaily.com/?s=kafka) - Technical interviews about Kafka.

### Community Resources
- [Apache Kafka Community](https://kafka.apache.org/community/) - Official community resources and contribution guidelines.
- [Confluent Developer](https://developer.confluent.io/) - Developer portal with courses, tutorials, and community links.

## Books

- [Kafka: The Definitive Guide, 2nd Edition](https://www.oreilly.com/library/view/kafka-the-definitive/9781492043072/) - Comprehensive guide by Confluent and LinkedIn engineers.
- [Kafka in Action](https://www.manning.com/books/kafka-in-action) - Practical introduction with real-world examples.
- [Kafka Streams in Action](https://www.manning.com/books/kafka-streams-in-action) - Stream processing guide from basics to production.
- [Designing Event-Driven Systems](https://www.confluent.io/designing-event-driven-systems/) - Free eBook on event-driven architecture with Kafka.
- [I Heart Logs](https://www.confluent.io/ebook/i-heart-logs/) - Free eBook by Jay Kreps on logs and stream processing.

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

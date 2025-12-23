# Awesome Kafka [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of awesome Apache Kafka resources, tools, libraries, and applications.

Inspired by [awesome-data-engineering](https://github.com/igorbarinov/awesome-data-engineering) and [awesome-bigdata](https://github.com/oxnr/awesome-bigdata).

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
  - [Kafka-Compatible Alternatives](#kafka-compatible-alternatives)
  - [Managed Services](#managed-services)
  - [Learning Resources](#learning-resources)
  - [Books](#books)

## Kafka

- [Apache Kafka](https://kafka.apache.org/) - Distributed event streaming platform capable of handling trillions of events a day.
- [Kafka Documentation](https://kafka.apache.org/documentation/) - Official documentation covering architecture, APIs, and operations.
- [Kafka Quickstart](https://kafka.apache.org/quickstart/) - Get up and running with Kafka in minutes.
- [KIPs](https://cwiki.apache.org/confluence/display/KAFKA/Kafka+Improvement+Proposals) - Kafka Improvement Proposals tracking upcoming features and changes.

## Clients

### Java
- [Apache Kafka Client](https://github.com/apache/kafka) - Official Java client with Producer, Consumer, Streams, and Admin APIs.

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
- [kafka.clj](https://github.com/helins/kafka.clj) - Clojure wrapper with Kafka Streams support.

### Haskell
- [hw-kafka-client](https://github.com/haskell-works/hw-kafka-client) - Haskell client based on librdkafka.

### HTTP / REST
- [Kafka REST Proxy](https://github.com/confluentinc/kafka-rest) - RESTful interface to produce and consume messages via HTTP.
- [Strimzi Kafka Bridge](https://github.com/strimzi/strimzi-kafka-bridge) - HTTP and AMQP bridge for Kubernetes.

## Stream Processing

### Kafka-Native
- [Kafka Streams](https://kafka.apache.org/documentation/streams/) - Client library for building stream processing applications.
- [ksqlDB](https://ksqldb.io/) - Event streaming database with SQL interface built on Kafka Streams.

### Frameworks
- [Apache Flink](https://flink.apache.org/) - Distributed stream processing framework with exactly-once semantics.
- [Apache Spark Streaming](https://spark.apache.org/streaming/) - Micro-batch stream processing on Spark.
- [Apache Samza](https://samza.apache.org/) - Stream processing framework with deep Kafka integration.
- [Apache Storm](https://storm.apache.org/) - Distributed real-time computation system.
- [Apache Beam](https://beam.apache.org/) - Unified batch and streaming API portable across runners.

### Streaming Databases
- [RisingWave](https://github.com/risingwavelabs/risingwave) - PostgreSQL-compatible streaming database with materialized views.
- [Materialize](https://github.com/MaterializeInc/materialize) - Streaming database with incremental view maintenance.
- [Timeplus Proton](https://github.com/timeplus-io/proton) - Fast streaming SQL engine for real-time analytics.
- [DeltaStream](https://deltastream.io/) - Serverless stream processing using Flink SQL (commercial).

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
- [Elasticsearch Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-elasticsearch) - Stream data to Elasticsearch and OpenSearch.
- [Cassandra Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-cassandra) - Write data to Apache Cassandra.
- [Neo4j Connector](https://neo4j.com/docs/kafka/current/) - Source and sink for Neo4j graph database.
- [Redis Sink](https://github.com/jcustenborder/kafka-connect-redis) - Write data to Redis.
- [ClickHouse Sink](https://github.com/ClickHouse/clickhouse-kafka-connect) - Official ClickHouse connector.

### Cloud Storage
- [S3 Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-s3) - Export data to Amazon S3 in Avro, JSON, or Parquet.
- [GCS Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-gcs) - Export data to Google Cloud Storage.
- [Azure Blob Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-azure-blob-storage) - Export data to Azure Blob Storage.
- [HDFS Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-hdfs3) - Write data to Hadoop HDFS.

### Data Warehouses
- [BigQuery Sink](https://www.confluent.io/hub/wepay/kafka-connect-bigquery) - Stream data to Google BigQuery with upsert support.
- [Snowflake Sink](https://docs.snowflake.com/en/user-guide/kafka-connector) - Official Snowflake connector with Iceberg support.
- [Redshift Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-aws-redshift) - Load data into Amazon Redshift.

### Message Queues
- [RabbitMQ Connector](https://www.confluent.io/hub/confluentinc/kafka-connect-rabbitmq) - Integrate with RabbitMQ queues.
- [ActiveMQ Source](https://www.confluent.io/hub/confluentinc/kafka-connect-activemq) - Consume messages from ActiveMQ.
- [AWS SQS Connector](https://www.confluent.io/hub/confluentinc/kafka-connect-sqs) - Source and sink for Amazon SQS.
- [Azure Event Hubs Source](https://www.confluent.io/hub/confluentinc/kafka-connect-azure-event-hubs) - Consume from Azure Event Hubs.
- [Google Pub/Sub Connector](https://www.confluent.io/hub/confluentinc/kafka-connect-gcp-pubsub) - Integration with Google Cloud Pub/Sub.

### HTTP & APIs
- [HTTP Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-http) - Send data to HTTP endpoints.
- [HTTP Source](https://github.com/castorm/kafka-connect-http) - Poll HTTP APIs as a Kafka source.
- [Salesforce Connector](https://www.confluent.io/hub/confluentinc/kafka-connect-salesforce) - Capture changes from Salesforce.

### Observability
- [Datadog Metrics Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-datadog-metrics) - Stream metrics to Datadog.
- [Splunk Sink](https://www.confluent.io/hub/splunk/kafka-connect-splunk) - Send events to Splunk.
- [InfluxDB Sink](https://www.confluent.io/hub/confluentinc/kafka-connect-influxdb) - Write to InfluxDB time-series database.

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
- [CMAK](https://github.com/yahoo/CMAK) - Cluster Manager for Apache Kafka by Yahoo.
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
- [Kafka Lag Exporter](https://github.com/seglo/kafka-lag-exporter) - Consumer group latency exporter for Kubernetes.

### Cluster Management
- [Strimzi](https://strimzi.io/) - Kubernetes operator for running Apache Kafka (CNCF Incubating).
- [Cruise Control](https://github.com/linkedin/cruise-control) - LinkedIn's automated workload rebalancer and self-healing.
- [Cruise Control UI](https://github.com/linkedin/cruise-control-ui) - Web interface for Cruise Control operations.
- [MirrorMaker 2](https://kafka.apache.org/documentation/#georeplication) - Built-in cross-cluster replication using Kafka Connect.
- [Jikkou](https://github.com/streamthoughts/jikkou) - GitOps tool for managing Kafka resources as code.

### Interactive Tools
- [Kafka Options Explorer](https://kafka-options-explorer.conduktor.io/) - Browse and compare Kafka configuration options across versions.

## CLI Tools

- [kcat](https://github.com/edenhill/kcat) - Swiss army knife for Kafka, formerly kafkacat.
- [kafkactl](https://github.com/deviceinsight/kafkactl) - Command-line tool inspired by kubectl with auto-completion.
- [kaf](https://github.com/birdayz/kaf) - Modern CLI for Kafka inspired by kubectl and docker.
- [Zoe](https://github.com/adevinta/zoe) - CLI for humans with time-based consumption and filtering.
- [kcli](https://github.com/cswank/kcli) - Simple Kafka command line browser.
- [trubka](https://github.com/xitonix/trubka) - CLI tool for Kafka with Protobuf support.
- [topicctl](https://github.com/segmentio/topicctl) - Tool for managing Kafka topics with YAML configs.
- [kafka-shell](https://github.com/devshawn/kafka-shell) - Interactive shell for Apache Kafka.

## Security

### Authentication & Authorization
- [Strimzi OAuth](https://github.com/strimzi/strimzi-kafka-oauth) - OAuth2/OIDC authentication for Kafka.
- [Apache Ranger](https://ranger.apache.org/) - Fine-grained authorization and centralized policy management.
- [Kafka Security Manager](https://github.com/conduktor/kafka-security-manager) - Git-based ACL management with auto-revert by Conduktor.
- [Julie](https://github.com/kafka-ops/julie) - GitOps for Kafka RBAC and topologies.
- [kafka-gitops](https://github.com/devshawn/kafka-gitops) - Manage Kafka resources as code with Git.

### Encryption
- [kafka-end-2-end-encryption](https://github.com/salyh/kafka-end-2-end-encryption) - Transparent AES encryption for Kafka messages.
- [kafkacrypto](https://github.com/tmcqueen-materials/kafkacrypto) - End-to-end encryption library for Python and Java.
- [Kryptonite](https://github.com/mercari/Kryptonite) - Field-level encryption SMT for Kafka Connect.

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
- [Voluble](https://github.com/MichaelDrogalis/voluble) - Realistic relational data generator for Kafka.
- [Datagen](https://github.com/MaterializeInc/datagen) - Multi-format data generator by Materialize.
- [Mockingbird](https://github.com/tinybirdco/mockingbird) - Mock streaming data generator.
- [DataFaker](https://github.com/datafaker-net/datafaker) - Java library for generating realistic fake data.

### Benchmarking
- [kafka-producer-perf-test](https://kafka.apache.org/documentation/#basic_ops_producer_perf) - Built-in producer performance testing tool.
- [kafka-consumer-perf-test](https://kafka.apache.org/documentation/#basic_ops_consumer_perf) - Built-in consumer performance testing tool.
- [OpenMessaging Benchmark](https://github.com/openmessaging/benchmark) - Cross-platform messaging system benchmarking.
- [Sangrenel](https://github.com/jamiealquiza/sangrenel) - Kafka cluster load testing tool.

### IDE Plugins
- [IntelliJ Kafka Plugin](https://plugins.jetbrains.com/plugin/11645-kafka) - Official JetBrains plugin for Kafka.
- [Kafkalytic](https://plugins.jetbrains.com/plugin/11946-kafkalytic) - IntelliJ plugin with message search and filtering.
- [Confluent for VS Code](https://marketplace.visualstudio.com/items?itemName=confluentinc.vscode-confluent) - Official Confluent extension for VS Code.
- [Tools for Apache Kafka](https://marketplace.visualstudio.com/items?itemName=jeppeandersen.vscode-kafka) - VS Code extension for Kafka development.

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
- [Upstash Kafka](https://upstash.com/kafka) - Serverless Kafka with pay-per-message pricing.
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

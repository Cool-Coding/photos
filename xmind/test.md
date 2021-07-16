Please answer these questions before submitting your issue.

- Why do you submit this issue?
- [ ] Question or discussion
- [x] Bug
- [ ] Requirement
- [ ] Feature or performance improvement

___
### Bug
- Which version of SkyWalking, OS, and JRE?
 skywalking8.6.0,mac,jdk1.8.0_191

- What happened?
oap creates wrong topic when I write namespace in kafka-fetcher item;
(1) fill namespace with a string value
```yaml
kafka-fetcher:
  selector: ${SW_KAFKA_FETCHER:default}
  default:
    bootstrapServers: ${SW_KAFKA_FETCHER_SERVERS:localhost:9092}
    namespace: ${SW_NAMESPACE:"yanggy"}
    partitions: ${SW_KAFKA_FETCHER_PARTITIONS:2}
    replicationFactor: ${SW_KAFKA_FETCHER_PARTITIONS_FACTOR:2}
    enableMeterSystem: ${SW_KAFKA_FETCHER_ENABLE_METER_SYSTEM:false}
    enableNativeProtoLog: ${SW_KAFKA_FETCHER_ENABLE_NATIVE_PROTO_LOG:false}
    enableNativeJsonLog: ${SW_KAFKA_FETCHER_ENABLE_NATIVE_JSON_LOG:false}
    isSharding: ${SW_KAFKA_FETCHER_IS_SHARDING:false}
    consumePartitions: ${SW_KAFKA_FETCHER_CONSUME_PARTITIONS:""}
    kafkaHandlerThreadPoolSize: ${SW_KAFKA_HANDLER_THREAD_POOL_SIZE:-1}
    kafkaHandlerThreadPoolQueueSize: ${SW_KAFKA_HANDLER_THREAD_POOL_QUEUE_SIZE:-1}
```
(2) start oap server
(3) show topics using kafka-manager

  ![](https://github.com/Cool-Coding/photos/blob/master/skywalking/skywalking-1.png?raw=true)
___
### Requirement or improvement
- Please describe your requirements or improvement suggestions.

# 도움말
```bash
kafka-topics.sh --help
```
# 토픽 생성
```bash
kafka-topics.sh \
--zookeeper 10.20.80.101:2181,10.20.80.102:2181,10.20.80.103:2181 \
--replication-factor 3 --partitions 3 --topic runpil-topic --create
```
# 토픽 삭제
```bash
kafka-topics.sh \
--zookeeper localhost:2181 --delete --topic runpil-topic
```
# 토픽 리스트 확인
```bash
kafka-topics.sh \
--zookeeper 10.20.80.101:2181,10.20.80.102:2181,10.20.80.103:2181 \
--list
```
# 토픽 상세보기
```bash
kafka-topics.sh \
--zookeeper 10.20.80.101:2181,10.20.80.102:2181,10.20.80.103:2181 \
--topic runpil-topic --describe
```
# Producer (메시지 생산하기)
```bash
kafka-console-producer.sh \
--broker-list 10.20.80.101:9092,10.20.80.102:9092,10.20.80.103:9092 \
--topic runpil-topic
```
# Consumer (메시지 소비하기)
```bash
kafka-console-consumer.sh \
--zookeeper 10.20.80.101:2181,10.20.80.102:2181,10.20.80.103:2181 \
--topic runpil-topic --from-beginning
```
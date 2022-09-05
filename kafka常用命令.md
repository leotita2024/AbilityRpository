# 命令大全
https://segmentfault.com/a/1190000040316572



* 主题列表查看
    ./kafka-topics.sh --list --bootstrap-server localhost:19092
* 消息查看
    ./kafka-console-consumer.sh --bootstrap-server localhost:19092 --topic TAP_GPS_TOPIC 
* 发送消息
    ./kafka-console-producer.sh --broker-list localhost:19092 --topic TAP_GPS_TOPIC
* 显示某个消费组的消费详情（仅支持offset存储在zookeeper上的）
bin/kafka-run-class.sh kafka.tools.ConsumerOffsetChecker --zookeeper localhost:2181 --group test

* #消息是否堆积
./kafka-consumer-groups.sh --describe --bootstrap-server 10.206.80.121:9092 --group S17-base-tap-service-group

* #指定offset partition 获取kafka消息
 ./kafka-console-consumer.sh --bootstrap-server  10.206.80.121:9092 --topic S17_signal_up_10001 --offset 98696281 --partition 3 --max-messages 1

* #将消费组的offset 设置为最新的，跳过历史数据
./kafka-consumer-groups.sh --bootstrap-server 10.206.48.170:9092 --group S17-base-tap-service-group --reset-offsets --to-latest --topic tap-alarm-topic --execute

* 查看消费组
./kafka-consumer-groups.sh --bootstrap-server xxxx:9090 --list

删除指定消费组--group
./kafka-consumer-groups.sh --delete --group test2_consumer_group --bootstrap-server xxxx:9090

# Kafka_Python_Client
```console
brew install librdkafka
```
- Add some symlinks
 ```console
 ls -lah ~/homebrew/include/librdkafka
 lrwxr-xr-x  1 sonnguyen  staff    45B May 15 17:06 /Users/sonnguyen/homebrew/include/librdkafka -> ../Cellar/librdkafka/1.8.2/include/librdkafka
 ```
 - Set env var
 ```console
 export C_INCLUDE_PATH=~/homebrew/Cellar/librdkafka/1.8.2/include
 export LIBRARY_PATH=~/homebrew/Cellar/librdkafka/1.8.2/lib
 ```
 
 
 - Install confluent-kafka
 ```console
 pipenv install confluent-kafka
 ```

## Create Topic
Create a new topic, `purchases`, which we will use to produce and consume events.
```console
docker compose exec broker \
  kafka-topics --create \
    --topic purchases \
    --bootstrap-server localhost:9092 \
    --replication-factor 1 \
    --partitions 1
 ```
 

## Run Consumer
```console
python consumer.py getting_started.ini
```
## Run Producer
```console
python producer.py getting_started.ini
```

# Kafka_Python_Client
```console
brew install librdkafka
```
- add some symlinks
 ```console
 ls -lah ~/homebrew/include/librdkafka
 lrwxr-xr-x  1 sonnguyen  staff    45B May 15 17:06 /Users/sonnguyen/homebrew/include/librdkafka -> ../Cellar/librdkafka/1.8.2/include/librdkafka
 ```
 - set env var
 ```console
 export C_INCLUDE_PATH=~/homebrew/Cellar/librdkafka/1.8.2/include
 export LIBRARY_PATH=~/homebrew/Cellar/librdkafka/1.8.2/lib
 ```
 
 ```console
 pipenv install confluent-kafka
 ```

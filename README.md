# How to run
## To run the project

1. Download, setup and run Apache Kafka. I use following commands on OSX from bin dir of kafka
```
sh zookeeper-server-start.sh ../config/zookeeper.properties
```
```
sh kafka-server-start.sh ../config/server.properties
```
2. Install complete NLTK
3. Create a twitter app and set your keys in live_twitter_sentiment_analysis/webapp/tweet_ingestion/config.py
4. Install python packages
```
pip install -r /live_data_sentiment_analysis/webapp/requirements.txt
```
5. Run webserver 
```
python live_twitter_sentiment_analysis/webapp/main.py
```
6. Run the maven-java project (rolling_average) after installing maven dependencies specified in live_twitter_sentiment_analysis/rolling_average/pom.xml. Don't forget to set checkpoint dir in Main.java

7. open the url localhost:8001/index.html

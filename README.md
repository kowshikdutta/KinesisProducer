# KinesisProducer
Compile with Maven:
mvn assembly:assembly -DdescriptorId=jar-with-dependencies


Create the Stream:
aws kinesis create-stream --stream-name StockTradeStream --shard-count 1

Run the Stream:
java -cp KinesisProducer-0.0.1-SNAPSHOT-jar-with-dependencies.jar producer.writer.StockTradesWriter StockTradeStream ap-south-1
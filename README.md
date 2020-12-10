# CurrencyPublisher
Standalone Springboot Java application to retrieve and publish various currency rates to Kafka Topics.

The main goal of this application module is to retrieve various currency values starting from given date to latest date
and keep publishing to configured Kafka Brokers for every 1 Second on various Kafka topics configured based on currency name.

The various currnecy values are retrieved from public api available at [Foreign exchange rates API](http://exchangeratesapi.io/)

# Prerquisites
- Java 8
- Apache Maven
- Apache Kafka

# Flow
CurrencyPublisher application is designed to have a threads pool containing separate thread for retrieveing curreny rates for
each of the currency for every 1 second from [Foreign exchange rates API](http://exchangeratesapi.io/) and publish to respective
Kafka topic for further processing from Kafka Event Streaming Module. Below diagram represents pictorial representation of the flow:

![Currency-Publisher-Flow](Currency-publisher-flow.pdf)

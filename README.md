#Heroku Kafka Message Generator

<br>
This demo application is written in ASP.NET Core and is intended to generate a randomized, simulated "web traffic data stream" and post it to a Heroku Kafka-as-a-Service Topic. It has 2 brother apps, one which pulls the Kafka Messages off the topic and persists them to Heroku Postgres, and another which finds specific messages and flips them in Postgres for Heroku Connect to Sync to Salesforce. <br><br>
Obviously you need Heroku Kafka in order to use this app, as well as the following Heroku App Config VARs:<br>
<br><p>
- HTTP_ENDPOINT_URL (should be set to the Kafka Rest API URL...similar to http://kafka-rest-app.herokuapp.com/api/messages)
- KAFKA_TOPIC (should be set to the exact name of the Kafka Topic to write messages to)
<br><p>
The other Config VARs are set when you provision Heroku Kafka and include:
<br>
- KAFKA_CLIENT_CERT
- KAFKA_CLIENT_CERT_KEY
- KAFKA_JMX_URL
- KAFKA_PLAINTEXT_URL (if in a Private Space)
- KAFKA_TRUSTED_CERT
- KAFKA_URL
- KAFKA_ZOOKEEPER_JMX_URL
- KAFKA_ZOOKEEPER_URL
- SECURITY_PROTOCOL_CONFIG
<br><p>

## Deploy this App to Heroku by clicking the button below:

<a href="https://heroku.com/deploy?template=https://github.com/herokumx/kafka-generator"> <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy">
</a>

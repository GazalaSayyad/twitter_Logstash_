# twitter_Logstash

ElasticSearch -
Elasticsearch has the ability to store large quantities of semi-structured (JSON) data and provides the ability to quickly and easily query this data. This makes it a good option for storing Twitter data which is delivered as JSON.

Logstash -
Logstash uses configurable input plugin to retreive data, filters to process it and ouptuts to define where to write all the aggregated data.
Tweets can be collected via the twitter API. Plugins are defined in logstash configuration files. So, retreiving twitter messages based on keyword can be achieved by adding a configuration file.
Added languages property to the twitter configuration to get only twitter message in english.

Visualisation with Kibana -
Need to have at least one data index, and one index pattern. Indices, the largest unit of data in Elasticsearch, are logical partitions grouping similar data together (corresponds to a database in relational databases). If you look back at line 18 of logstash.conf, I stored Twitter documents in the tweets index.

Twitter Stream API
1.Go to https://dev.twitter.com/apps/new and log in, if necessary
2.Supply the necessary required fields, accept the Terms Of Service, and solve the CAPTCHA.
3.Submit the form
4.Go to the API Keys tab, there you will find your Consumer key and Consumer secret keys.
5.Copy the consumer key (API key) and consumer secret from the screen into our application.


Run with Docker Compose:
1.Create a docker-compose.yml file for the Elastic Stack.
2.Run docker-compose up
3.Check Elasticsearch running at :http://localhost:9200.
4.Open Kibana to load sample data and interact with the cluster: http://localhost:5601.
5.At the end tear down the containers and volumes by running docker-compose down -v.
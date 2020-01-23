= installation =

= arch linux =
package: elasticserach
start/enable elasticsearch.service
test: curl http://127.0.0.1:9200
configuration file: /etc/elasticsearch/elasticsearch.yml
restrict access to host: network.host: 127.0.0.1 (config file)

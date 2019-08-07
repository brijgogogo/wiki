= elk =
take data from any source and any format and then search, analyze, and visualize it in real time.

made up of: Elasticsearch, Logstash, Kibana

Elasticsearch: distributed, search and analytics engine
Logstash: data collection, enrichment and transportation pipeline
Kibana: data visualization platform


* [[elasticsearch]]
* [[logstash]]
* [[kibana]]

       applications
    (logstash shipper)
           |
           |
           V
    logstash indexer
           |
           |
           V
      Elasticsearch
           ^
           |
           |
        Kibana



Shopbay Elasticsearch - Open Source Ecommerce Platform  
=======================================

This provides a wrapper of elasticsearch runtime and stores configuration / data / log files.
Other `shopbay-app` such as `shopbay-shop` or `shopbay-merchant` can use its api endpoint to perform search function

Please make sure elasticsearch is installed first.


REQUIREMENTS
------------
* shopbay-kernel
* Elasticsearch 1.4 or above

SETUP
------
Configure `config/elasticsearch.yml`

        ELASTICSEARCH_CLUSTER : <Please input the elasticsearch hostname, e.g. localhost>
        ELASTICSEARCH_PORT : e.g. 9200
        ELASTICSEARCH_CLUSTER : <Please input the elasticsearch cluster name, e.g. cluster_app>
        ELASTICSEARCH_NODE : <Please input the elasticsearch node name, e.g. node_app>
        ELASTICSEARCH_DATA_DIR : <Please input the elasticsearch data directory name, e.g. /INSTALL_PATH/elasticsearch/data>
        ELASTICSEARCH_LOG_DIR : <Please input the elasticsearch logs directory name, e.g. /INSTALL_PATH/elasticsearch/logs>


RUN `shopbay-elasticsearch` at command line
------------

Option 1
--------
Assume `app` is installed at APP_HOME, e.g. /home/shopbay

        cd APP_HOME/shopbay-elasticsearch
        ./start

Option 2
--------
Assume elasticsearch is installed at ES_HOME, e.g. /home/shopbay/elasticsearch-1.4.1

Assume `app` is installed at APP_HOME, e.g. /home/shopbay

Create a shell script to have following command line to run elasticsearch by pointing to `app` specific yml. 

        ES_HOME/bin/elasticsearch -d --config=APP_HOME/shopbay-elasticsearch/config/elasticsearch.yml

Check status
------------

        ./status
# Kibana Dockerfile

First we need to make sure Elasticsearch is running

    docker run --name elasticsearch -d -t denibertovic/elasticsearch

Run kibana

    docker run -d -p 5601:5601 -v /path/to/logs:/logs -v `pwd`/config-example:/kibana/config denibertovic/kibana

Ports

    5601  (kibana interface)

Volumes

    /kibana/config (contains kibana.yml config file)
    /logs (contains kibana.logs)


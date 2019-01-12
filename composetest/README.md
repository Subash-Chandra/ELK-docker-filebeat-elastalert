# Docker Elasticsearch with Kibana and Filebeat

Run the latest version of the ELK (Elasticsearch, Filebeat, Kibana) stack with Docker and Docker Compose.

It will give you the ability to analyze any data set by using the searching/aggregation capabilities of Elasticsearch
and the visualization power of Kibana.

Based on the official Docker images:

* [elasticsearch](https://github.com/elastic/elasticsearch-docker)
* [filebeat](https://github.com/elastic/filebeat-docker)
* [kibana](https://github.com/elastic/kibana-docker)
## Requirements

### Host setup
Install Docker. 
Download this repository.

## Usage

### Bringing up the stack

**Note**: In case you switched branch or updated a base image - you may need to run `docker-compose build` first

Start the ELK stack using `docker-compose`:

```console
$ docker-compose -f docker-compose-elk.yml up
```

You can also choose to run it in background (detached mode):

```console
$ docker-compose -f docker-compose-elk.yml up -d
```

Give Kibana a few seconds to initialize, then access the Kibana web UI by hitting
[http://localhost:5601](http://localhost:5601) with a web browser.

By default, the stack exposes the following ports:
* 9200: Elasticsearch HTTP
* 9300: Elasticsearch TCP transport
* 5601: Kibana


### How can I tune the filebeat configuration?

The Filebeat configuration is stored in `filebeat/filebeat.yml`.

### How can I tune the Elasticsearch configuration?

The Elasticsearch configuration is stored in `elasticsearch/config/elasticsearch.yml`.

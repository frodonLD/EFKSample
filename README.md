# EFK

In this document we'll mainly have a look on how we can use the EK suite with fluentd as the producer of the logs message.
We won't really discuss about [Elasticsearch](https://www.elastic.co/products/elasticsearch), [Fluentd](https://www.fluentd.org/) and [Kibana](https://www.elastic.co/products/kibana). The document will be focused on
how we can use these tools together to handle and parse our logs from docker containers.

## Fluentd

* [https://docs.docker.com/config/containers/logging/fluentd/](https://docs.docker.com/config/containers/logging/fluentd/)
* [https://docs.fluentd.org/v0.12/articles/kubernetes-fluentd](https://docs.fluentd.org/v0.12/articles/kubernetes-fluentd)
* [https://www.fluentd.org/guides/recipes/docker-logging](https://www.fluentd.org/guides/recipes/docker-logging)
* [https://docs.fluentd.org/v0.12/articles/docker-logging-efk-compose](https://docs.fluentd.org/v0.12/articles/docker-logging-efk-compose)
* [https://docs.fluentd.org/v1.0/articles/config-file](https://docs.fluentd.org/v1.0/articles/config-file)

## The suite together

Build our fluentd docker image

```bash
docker build -t sample/fluentd fluentd
```

Launch the docker-compose

```bash
docker-compose up -d
```
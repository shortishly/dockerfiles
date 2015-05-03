# Dockerfiles

All of the below images use the official
[centos repository](https://registry.hub.docker.com/_/centos/) as
their base.

## Kibana

Download the latest version of Kibana with an entry point that can be
linked to Elastic Search.

Trivial to integrate via
[docker compose](https://docs.docker.com/compose/) with official
Elastic Search image.

```yaml
elasticsearch:
  image: elasticsearch
  ports:
    - "9200:9200"

kibana:
  image: shortishly/kibana
  links:
    - elasticsearch
  ports:
    - "5601:5601"
```

## EPEL

## Erlang

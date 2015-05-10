# Kibana

Download the latest version of Kibana with an entry point that can be
linked to Elastic Search.

Trivial to integrate via
[docker compose](https://docs.docker.com/compose/) with official
Elastic Search image.

```
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

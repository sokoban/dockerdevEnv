# docker-compose-elasticsearch-kibana

## Overview
Docker Compose for 3 Node Elasticsearch (7.5.1) Cluster and Kibana (Open Source 7.5.1) Instance for development purposes.

Kibana is being served behind Nginx Proxy so you can secure access of kibana for your purpose.

## Requirements
1. Docker 18.05
2. Docker-compose 1.21

### Start Stack in Daemon Mode
```
docker-compose up -d
```

### Check status of docker-compose cluster
```
docker-compose ps -a
```

### Cluster Node Info
```
curl http://localhost:9200/_nodes?pretty=true
```

### Access Kibana
```
http://localhost:5601
```

### Accessing Kibana through Nginx
```
http://localhost:8080
```

### Access Elasticsearch
```
http://localhost:9200
```

### Before you Up

1. Change max_map_count
```
$ echo 262144 > /proc/sys/vm/max_map_count
```
2. Create the folder
```
/usr/share/elasticsearch/data
```

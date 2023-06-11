# Criar docker-compose

Talvez seja necessario fazer os seguintes passos

```bash
docker network create observability
```

```bash
mkdir elasticsearch_data
```

```bash
sudo chown 1000:1000 elasticsearch_data
```

```bash
sysctl -w vm.max_map_count=262144
```

### Elasticsearch

-   Porta padrão do elasticsearch 9200
-   Volume criado para não perder os dados do container.

### Kibana

-   Porta padrão do kibana 5601

### Executando

```bash
docker compose up -d
```

```bash
docker logs elasticsearch
```

http://localhost:5601

```bash
sudo chown root metricbeat.yml
```

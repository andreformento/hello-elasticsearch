# hello-elasticsearch

- start: `docker compose up --wait`
- user `elastic`
- password: `cat .env | grep ES_LOCAL_PASSWORD`
- Elasticsearch will be running at http://localhost:9200
- Kibana will be running at http://localhost:5601
- Jupyter Notebook will be running at http://localhost:8888
- ES Host: `http://elasticsearch:9200`

### References

- https://github.com/elastic/start-local
- https://github.com/elastic/elasticsearch-labs
- https://github.com/elastic/elasticsearch-labs?tab=readme-ov-file

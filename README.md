# hello-elasticsearch

- Run elasticsearch

```shell
$ docker run --rm -d \
         --name elasticsearch \
         -p 9201:9200 -p 9300:9300 \
         elasticsearch
```

- Create sample Data

```shell
$ curl -XPOST 'http://localhost:9201/twitter/tweed/1' -d '
{
"user": "oveits",
"message": "this is my first elasticsearch message",
"postDate": "2016-11-18T15:55:00"
}'
```

- And stop container with `docker stop elasticsearch`

### References

- https://oliverveits.wordpress.com/2016/11/18/elasticsearch-hello-world-example/

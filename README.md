# hello-elasticsearch

## How to do

- Run elasticsearch

```shell
$ docker run --rm -d \
         --name elasticsearch \
         -p 9200:9200 -p 9300:9300 \
         elasticsearch
```

- Create sample Data

```shell
$ curl -XPOST 'http://localhost:9200/twitter/tweed/1' -d '
{
"user": "oveits",
"message": "this is my first elasticsearch message",
"postDate": "2016-11-18T15:55:00"
}'
```

- Read Data `curl -XGET 'localhost:9200/twitter/tweed/1'`
- Search Data based on Content `curl -XGET 'localhost:9200/twitter/_search?q=message:first'`
- Search String in any Field `curl -XGET 'localhost:9200/twitter/_search?q=2016'`

- Search for Entries within a Time Range
```shell
curl -XGET localhost:9200/twitter/_search? -d '
{ "query":{
      "range":{
         "postDate":{ "from":"2016-11-18T15:00:00",
                      "to"  :"2016-11-18T17:00:00" }
      }
}}
'
```

- After all, stop container with `docker stop elasticsearch`

### Requirements

- `Docker` _(just it, seriously!)_
- `curl` or any another client

### References

- https://oliverveits.wordpress.com/2016/11/18/elasticsearch-hello-world-example/

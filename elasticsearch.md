# Shards

- maximum shard size ~50GB
- maximum shard count per node: depends on heap. estimate: 30GB heap = max 600 - 750 shards

- larger segments have less overhead than smaller segments
```
http://master:9200/index/_forcemerge?max_num_segments=1
```


Additional info:
https://www.elastic.co/blog/how-many-shards-should-i-have-in-my-elasticsearch-cluster

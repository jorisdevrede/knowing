## Shards

- maximum shard size ~50GB
- maximum shard count per node: depends on heap. estimate: 30GB heap = max 600 - 750 shards
- an index with less shards is faster to query
- larger segments have less overhead than smaller segments
```
http://master:9200/index/_forcemerge?max_num_segments=1
```


Additional info:
https://www.elastic.co/blog/how-many-shards-should-i-have-in-my-elasticsearch-cluster

## Index Recovery
Use only when there is no search activity.

```
PUT /_cluster/settings

{
  "transient": {
    "cluster.routing.allocation.node_concurrent_recoveries": 6,
    "indices.recovery.concurrent_streams": "6",
    "indices.recovery.max_bytes_per_sec": "1000mb",
    "indices.store.throttle.type" : "none"
  }
}

```

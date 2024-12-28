# Issues and Fixes

A list of possible known issues and fixes

## ElasticSearch Issue

Rarely the elastic search install will run into errors figuring out who is the main node. Easiest way to fix this is delete the entire `Elasticsearch` kubernetes object and let the Argo Recreate, then rerun the ingestion pipeline.

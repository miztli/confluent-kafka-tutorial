# Confluent commands cheat sheet

### Login

`confluent login -save` 

### List environments

`confluent environment list`

Use the id of the given environment to connect to a cluster inside that environment

### Use environment

`confluent environment use <environment-id>`

### List kafka clusters

`confluent kafka cluster list`

Use the id of the retrieved list of the clusters to connect to a specific cluster

### Select a kafka cluster

`confluent kafka cluster use <cluster-id>`

### Create API key/secret to connect to the cluster

`confluent api-key create --resource <cluster-id> --description 'created from terminal'`

### Set api-key to start interacting with the cluster

`confluent api-key use <api-key-id> --resource <cluster-id>`

### List kafka topics

`confluent kafka topic list`

### Consume messages from topic

`confluent kafka topic consume <topic-name> --from-beginning`

Check available options for partitions, group id, etc.

### Produce messages to a topic

`confluent kafka topic produce orders --parse-key`
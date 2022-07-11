---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "upstash_kafka_credential Resource - terraform-provider-upstash"
subcategory: ""
description: |-
  
---

# upstash_kafka_credential (Resource)



## Example Usage

```terraform
resource "upstash_kafka_cluster" "exampleKafkaCluster" {
    cluster_name = var.cluster_name
    region = var.region
    multizone = var.multizone
}


resource "upstash_kafka_topic" "exampleKafkaTopic" {
    topic_name = var.topic_name
    partitions = var.partitions
    retention_time = var.retention_time
    retention_size = var.retention_size
    max_message_size = var.max_message_size
    cleanup_policy = var.cleanup_policy
    cluster_id = resource.upstash_kafka_cluster.exampleKafkaCluster.cluster_id
}

resource "upstash_kafka_credential" "exampleKafkaCredential" {
    cluster_id = upstash_kafka_cluster.exampleKafkaCluster.cluster_id
    credential_name="credentialFromTerraform"
    topic = upstash_kafka_topic.exampleKafkaTopic.topic_name
    permissions = "ALL"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `cluster_id` (String) ID of the kafka cluster
- `credential_name` (String) Name of the kafka credential
- `permissions` (String) Permission scope given to the kafka credential
- `topic` (String) Name of the kafka topic

### Read-Only

- `creation_time` (Number) Creation time of the credential
- `credential_id` (String) Unique ID of the kafka credential
- `id` (String) The ID of this resource.
- `password` (String, Sensitive) Password to be used in authenticating to the cluster
- `state` (String) State of the credential(active or deleted)
- `username` (String) Username to be used for the kafka credential


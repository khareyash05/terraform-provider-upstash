---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "upstash_redis_database_data Data Source - terraform-provider-upstash"
subcategory: ""
description: |-
  
---

# upstash_redis_database_data (Data Source)



## Example Usage

```terraform
data "upstash_redis_database_data" "exampleDBData" {
    database_id = resource.upstash_redis_database.exampleDB.database_id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `database_id` (String) Unique Database ID for requested database

### Read-Only

- `auto_scale` (Boolean) Upgrade to higher plans automatically when it hits quotas
- `consistent` (Boolean, Deprecated) When enabled database runs in Consistency Mode
- `creation_time` (Number) Creation time of the database
- `database_name` (String) Name of the database
- `database_type` (String) Type of the database
- `db_daily_bandwidth_limit` (Number) Daily bandwidth limit for the database
- `db_disk_threshold` (Number) Disk threshold for the database
- `db_max_clients` (Number) Max clients for the database
- `db_max_commands_per_second` (Number) Max commands per second for the database
- `db_max_entry_size` (Number) Max entry size for the database
- `db_max_request_size` (Number) Max request size for the database
- `db_memory_threshold` (Number) Memory threshold for the database
- `endpoint` (String) Database URL for connection
- `eviction` (Boolean) Enable eviction, to evict keys when your database reaches the max size
- `id` (String) The ID of this resource.
- `multizone` (Boolean, Deprecated) When enabled database is highly available and deployed multi-zone
- `password` (String, Sensitive) Password of the database
- `port` (Number) Port of the endpoint
- `primary_region` (String) Primary region for the database
- `read_only_rest_token` (String) Rest Token for the database.
- `read_regions` (Set of String) Read regions for the database
- `region` (String) region of the database. Possible values are: "global", "eu-west-1", "us-east-1", "us-west-1", "ap-northeast-1" , "eu-central1"
- `rest_token` (String, Sensitive) Rest Token for the database.
- `state` (String) State of the database
- `tls` (Boolean) When enabled data is encrypted in transit
- `user_email` (String) User email for the database



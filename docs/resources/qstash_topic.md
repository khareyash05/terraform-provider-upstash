---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "upstash_qstash_topic Resource - terraform-provider-upstash"
subcategory: ""
description: |-
  
---

# upstash_qstash_topic (Resource)



## Example Usage

```terraform
resource "upstash_qstash_topic" "exampleQstashTopic" {
  name = "exampleQstashTopicName"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) Name of the Qstash Topic

### Read-Only

- `endpoints` (List of Map of String) Endpoints for the Qstash Topic
- `id` (String) The ID of this resource.
- `topic_id` (String) Unique Qstash Topic ID for requested topic



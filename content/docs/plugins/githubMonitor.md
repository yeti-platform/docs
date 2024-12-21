---
title: Github Monitor
date: 2024-12-17T12:00:00
draft: false
weight: 1
---

1. Create a Github token at https://github.com/settings/tokens
2. Pop that in `yeti.conf`
3. Create a an indicator with the following essential details :
   * query text : (see [query template](#query-template) below)
   * query type : `github`
   * diamond model : depends on context

![Example of the Github Monitor settings](github-monitor-example.png)

Here are some gotchas:

* The query type won't show up in the list - you need to type it in
* The query text isn't really documented outside of the code for this plugin.
  The example in the code is missing an inverted comma.
* You need to fill in the diamond model field.

#### Query Template

```json
[
    {
        "type": "code",
        "query": "CVE-2024-49138 poc"
    }
]
```

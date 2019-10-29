---
title: DNS Event Sentinel One
description: This event is triggered by Sentinel One when a Windows process issues a DNS request
log.type: sentinelone
sentinelone.version: 1
sentinelone.rule: DNSEvent
author: Zack Payton (@zackpayton)
date: 10/29/2019
---

## Event JSON

```

```

## Event Types:
|	Standard Name	|	Field Name	|	Description	|
|	-------------	|	----------	|	----	|



## Data Dictionary
|	Standard Name	|	Field Name	|	Type	|	Description	|	Sample Value	|
|	-------------	|	----------	|	----	|	-----------	|	------------	|
| process_id | dns.source.process.fullPid.pid | integer | Process ID used by the os to identify the created process (child) | 5956 |
| dst_host_name | dns.query | string | DNS query name | chrome.google.com |
| dns_query_status | dns.status | string | DNS query status | 1 |
| dns_query_results | dns.results | string | DNS query results | type: 5 www3.l.google.com;172.217.7.206; |
| event_date_creation | timestamp.millisecondsSinceEpoch | date | Time in UTC when event was created | 	4/11/18 5:25 |

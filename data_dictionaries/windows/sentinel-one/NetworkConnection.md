---
title: Process Created Sentinel One
description: This event is triggered by Sentinel One when a Windows process establishes a network connection
log.type: sentinelone
sentinelone.version: 1
sentinelone.rule: NetworkConnection
author: Zack Payton (@zackpayton)
date: 10/28/2019
---

## Description
Sentinel One will generate an event when a process opens a TCP/UDP network connection.

## Event JSON

```
{
      "http": null,
      "regKeyImport": null,
      "persistency": null,
      "tcpv4Listen": null,
      "regValueCreate": null,
      "schedTaskDelete": null,
      "fileCreation": null,
      "fileRename": null,
      "logout": null,
      "fileModification": null,
      "schedTaskTrigger": null,
      "processExit": null,
      "schedTaskRegister": null,
      "regKeySecurityChanged": null,
      "processCreation": null,
      "regKeyExport": null,
      "schedTaskUpdate": null,
      "tcpv4": {
        "direction": "OUTGOING",
        "trueContext": {
          "key": {
            "value": "4F9C2917DB832811"
          }
        },
        "status": "SUCCESS",
        "destinationAddress": {
          "port": 443,
          "address": "40.97.28.98"
        },
        "sourceAddress": {
          "port": 52413,
          "address": "10.115.32.249"
        },
        "source": {
          "parent": null,
          "activeContent": null,
          "node": {
            "key": {
              "value": "3BA1AE60AE67F8C9"
            }
          },
          "fullPid": {
            "pid": 3068,
            "startTime": {
              "millisecondsSinceEpoch": 1571670467763
            }
          },
          "user": null,
          "integrityLevel": "INTEGRITY_LEVEL_UNKNOWN",
          "isWow64": "E_UNSUPPORTED",
          "sessionId": 0,
          "trueContext": null,
          "executable": null,
          "excluded": "E_UNSUPPORTED",
          "commandLine": "",
          "interactive": "E_UNSUPPORTED",
          "subsystem": "SUBSYSTEM_UNKNOWN",
          "isRedirectedCommandProcessor": "E_UNSUPPORTED",
          "root": "E_UNSUPPORTED",
          "name": "Google Chrome"
        }
      },
      "regKeyRename": null,
      "regValueDelete": null,
      "timestamp": {
        "millisecondsSinceEpoch": 1571933515865
      },
      "regKeyDelete": null,
      "regValueModified": null,
      "login": null,
      "fileDeletion": null,
      "processTermination": null,
      "dns": null,
      "schedTaskStart": null,
      "regKeyCreate": null
    }```

## Event Types:
|	Standard Name	|	Field Name	|	Description	|
|	-------------	|	----------	|	----	|
| processs_start    |   processCreation | Process was started   |


## Data Dictionary
|	Standard Name	|	Field Name	|	Type	|	Description	|	Sample Value	|
|	-------------	|	----------	|	----	|	-----------	|	------------	|
| src_ip | tcpv4.sourceAddress.address | ip | source ip address that made the network connection | 1.2.3.4 |
| src_port | tcpv4.sourceAddress.port | integer | source port number | 39324 |
| dst_ip | tcpv4.destinationAddress.address | ip | ip address destination | 4.3.2.1 |
| dst_port | tcpv4.destinationAddress.port | integer | destination port number | 139 |
| process_id | tcpv4.source.fullPid.pid | 	Process ID used by the os to identify the process that made the network connection | 139 |
| event_date_creation | timestamp.millisecondsSinceEpoch | date | Time in UTC when event was created | 	4/11/18 5:25 |

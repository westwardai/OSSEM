---
title: Flie Created Sentinel One
description: This event is triggered by Sentinel One when a Windows process creates a file
log.type: sentinelone
sentinelone.version: 1
sentinelone.rule: FlieCreate
author: Zack Payton (@zackpayton)
date: 10/24/2019
---

## Event JSON

```
{
      "http": null,
      "regKeyImport": null,
      "persistency": null,
      "tcpv4Listen": null,
      "regValueCreate": null,
      "schedTaskDelete": null,
      "fileCreation": {
        "trueContext": {
          "key": {
            "value": "4F9C2917DB832811"
          }
        },
        "targetFile": {
          "creationTime": null,
          "sizeBytes": 0,
          "node": {
            "key": {
              "value": "A80BB3E47E3C15BD"
            }
          },
          "hashes": null,
          "isKernelModule": "E_UNSUPPORTED",
          "isDir": "E_UNSUPPORTED",
          "path": "C:\Users\username\AppData\Local\Google\Chrome\User Data\Default\787f76b8-5dfc-4317-a5d0-fb1b57dc6321.tmp",
          "p_windows": "",
          "owner": null,
          "p_unix": 0,
          "signature": null
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
      "tcpv4": null,
      "regKeyRename": null,
      "regValueDelete": null,
      "timestamp": {
        "millisecondsSinceEpoch": 1571933526958
      },
      "regKeyDelete": null,
      "regValueModified": null,
      "login": null,
      "fileDeletion": null,
      "processTermination": null,
      "dns": null,
      "schedTaskStart": null,
      "regKeyCreate": null
}
```

## Event Types:
|	Standard Name	|	Field Name	|	Description	|
|	-------------	|	----------	|	----	|



## Data Dictionary
|	Standard Name	|	Field Name	|	Type	|	Description	|	Sample Value	|
|	-------------	|	----------	|	----	|	-----------	|	------------	|
| process_id | fileCreation.source.fullPid.pid | integer | Process ID used by the os to identify the process changing the file creation time | 3068 |
| file_name | fileCreation.targetFile.path | string | full path name of the file | C:\Users\username\AppData\Local\Google\Chrome\User Data\Default\787f76b8-5dfc-4317-a5d0-fb1b57dc6321.tmp |
| event_date_creation | timestamp.millisecondsSinceEpoch | date | Time in UTC when event was created | 	4/11/18 5:25 |

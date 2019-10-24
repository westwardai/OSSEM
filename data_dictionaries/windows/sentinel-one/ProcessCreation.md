---
title: Process Created Sentinel One
description: This event is triggered by Sentinel One when a new Windows process is created
log.type: sentinelone
sentinelone.version: 1
sentinelone.rule: ProcessCreate
author: Zack Payton (@zackpayton)
date: 10/24/2019
---

## Event Log Illustration & Event JSON

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
      "processCreation": {
        "trueContext": {
          "key": {
            "value": "BE160A34845BCEE6"
          }
        },
        "parent": {
          "parent": null,
          "activeContent": null,
          "node": {
            "key": {
              "value": "8B02A291C0D2A77B"
            }
          },
          "fullPid": {
            "pid": 604,
            "startTime": {
              "millisecondsSinceEpoch": 1571537545377
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
          "name": "Host Process for Windows Services"
        },
        "hashes": {
          "md5": "de1934bdb5b8e10b2f3574c3ccd35bb4",
          "sha1": "36eb5db4c3ca78596f3e08158d54392cf3d43739",
          "sha256": "b13697c44f1939cb00ea58a65e2460d4be5637704a6dd14c6746709e448a8cc5"
        },
        "signature": null,
        "status": "UNKNOWN",
        "process": {
          "parent": {
            "parent": null,
            "activeContent": null,
            "node": {
              "key": {
                "value": ""
              }
            },
            "fullPid": {
              "pid": 0,
              "startTime": {
                "millisecondsSinceEpoch": 0
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
            "name": ""
          },
          "activeContent": null,
          "node": {
            "key": {
              "value": "99C0960D288C8C9F"
            }
          },
          "fullPid": {
            "pid": 5956,
            "startTime": {
              "millisecondsSinceEpoch": 1571923530370
            }
          },
          "user": {
            "name": "NT AUTHORITY\\NETWORK SERVICE",
            "sid": "S-1-5-20"
          },
          "integrityLevel": "SYSTEM",
          "isWow64": "E_TRUE",
          "sessionId": 0,
          "trueContext": {
            "key": {
              "value": ""
            }
          },
          "executable": {
            "creationTime": null,
            "sizeBytes": 0,
            "node": {
              "key": {
                "value": "69F3E3678D507023"
              }
            },
            "hashes": null,
            "isKernelModule": "E_UNSUPPORTED",
            "isDir": "E_UNSUPPORTED",
            "path": "C:\\Windows\\SysWOW64\\wbem\\WmiPrvSE.exe",
            "p_windows": "",
            "owner": null,
            "p_unix": 0,
            "signature": null
          },
          "excluded": "E_FALSE",
          "commandLine": "C:\\Windows\\sysWOW64\\wbem\\wmiprvse.exe -secured -Embedding",
          "interactive": "E_FALSE",
          "subsystem": "SYS_WIN32",
          "isRedirectedCommandProcessor": "E_FALSE",
          "root": "E_TRUE",
          "name": "WMI Provider Host"
        }
      },
      "regKeyExport": null,
      "schedTaskUpdate": null,
      "tcpv4": null,
      "regKeyRename": null,
      "regValueDelete": null,
      "timestamp": {
        "millisecondsSinceEpoch": 1571933530992
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
| processs_start    |   processCreation | Process was started   |


## Data Dictionary
|	Standard Name	|	Field Name	|	Type	|	Description	|	Sample Value	|
|	-------------	|	----------	|	----	|	-----------	|	------------	|
| process_parent_id | processCreation.parent.fullPid.pid | integer | Process ID of the process that spawned/created the main process (child) | 0 |

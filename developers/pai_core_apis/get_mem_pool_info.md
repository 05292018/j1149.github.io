---
layout: default
title: GetMemPoolInfo
parent: PAI Core Apis
grand_parent: Developer Reference
---

GetMemPoolInfo
========================

The `getmempoolinfo` RPC returns information about the node’s current transaction memory pool.

*Parameters: none*

*Result---information about the transaction memory pool*

| Name | Type      | Presence            | Description
|------|-----------|---------------------|-------------
|`result`  |object | Required<br>(exactly 1) | A object containing information about the memory pool
| →<br>`size` | number (int) | Required<br>(exactly 1) | The number of transactions currently in the memory pool
| →<br>`bytes` | number (int) | Required<br>(exactly 1) | The total number of bytes in the transactions in the memory pool
| →<br>`usage` | number (int) | Required<br>(exactly 1) | *Added in Pai Core 0.11.0*<br><br>Total memory usage for the mempool in bytes
| →<br>`maxmempool` | number (int) | Required<br>(exactly 1) | *Added in Pai Core 0.12.0*<br><br>Maximum memory usage for the mempool in bytes
| →<br>`mempoolminfee` | number (int) | Required<br>(exactly 1) | Added in Pai Core 0.12.0*<br><br>The lowest fee per kilobyte paid by any transaction in the memory pool


*Example from PAI Core 0.14.1*

```
pai-cli -testnet getmempoolinfo
```

Result:

```
{
  "size": 1237,
  "bytes": 591126,
  "usage": 1900416,
  "maxmempool": 300000000,
  "mempoolminfee": 0.00000000
}
```

*See also*

* `GetBlockChainInfo`:
* `GetRawMemPool`:
* `GetTxOutSetInfo`:

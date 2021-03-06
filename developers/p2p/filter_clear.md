---
layout: default
title: FilterClear
parent: P2P
grand_parent: Developer Reference
---

FilterClear
=============

*Added in protocol version 70001 as described by BIP37.*

The `filterclear` message tells the receiving peer to remove a
previously-set bloom filter.  This also undoes the effect of setting the
relay field in the `version` message to 0, allowing unfiltered access to
`inv` messages announcing new transactions.

Pai Core does not require a `filterclear` message before a
replacement filter is loaded with `filterload`.  It also doesn't require
a `filterload` message before a `filterclear` message.

There is no payload in a `filterclear` message.  See the [message header
section][section message header] for an example of a message without a payload.

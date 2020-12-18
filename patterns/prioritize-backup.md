---
title: Prioritize Backup
tags:
  - pattern
  - app
  - sync
  - archiving
  - status
layout: pattern
---

## The Design Problem

In a centralized application, it is assumed that the owner will prioritize backing up all your data. If there was some natural disaster at one of Google's data centers, for example, they have a variety of backups of your data in various locations around the world.

In a decentralized application, we have no guarantee that data will be replicated to other locations. In fact, for some use cases, this user agency and control over who has access to their data is a feature, not a bug. But if users expect archiving and long-term storage across the world's data centers, your app needs to provide timely information about syncronization status and availability.

## The Design Solution

Prioritize backing up all data in multiple locations, ideally across the world. Tell the user when data has been syncronized to long-term storage locations. Pair this with [Network Health Indicator](network-health-indicator.md) for more fine-grained information about where data is syncronized.

### Examples

- Dropbox app (checkmarks)
- IPFS
- Matrix

## Why Choose Prioritize Backup?

When users depend upon long-term storage and archiving of their data.

## Best Practice: How to Implement Prioritize Backup

- Prioritize backup can be more useful for static data.
- Trust needs to be established among organizations beforehand to create systems that are resilient with good feedback loops.
- Make sure to communicate about the community-owned infrastructure upfront.
- If possible, encrypt data before backup so that it is not readable by the storage providers.

## Potential Problems with Prioritize Backup

- Without encryption of contents that are being syncronized across the network, users could be subject to attacks. Be sure to communicate when unencrypted data will be stored and readable by back up services.
- Prioritize backup can be too technical. Hide advanced metrics and show users simple indicators on their syncronization status, similar to Dropbox.
- It could be difficult to delete data if there are many storage providers or peers on the network. See [Tombstones](tombstones.md) for more information on how to request data removal.

## The Take-Away

Prioritizing backup is crucial for competing with centralized services that provide long-term archiving and storage.

## References & Where to Learn More

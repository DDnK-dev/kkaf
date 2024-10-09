# kkaf - kubernetes-usable Kaf Specification

## Overview

`kkaf` is toy project to make `kaf` usable in kubernetes. Some commands are modified, influenced by `kubectl`.

This document describes the specification of `kkaf`.
In this document, features and main concepts of `kkaf` are described.

## Main Concepts

1. `kkaf` should be able to communicate with kubernetes services, which are not exposed to the internet (NodePort or something)
2. `kkaf` is CLI based on cobra and viper.
3. `kkaf` should provide `status` command to check the status and health of kafka cluster.
4. `kaf`'s main feature has to be provided in `kkaf`

## Features

### command overview

| Command     | Description                                | Status     |
|-------------|--------------------------------------------|------------|
| `config`    | Handle kkaf configuration                  | InProgress |
| `get`       | `List` or `Get` resources                  | TODO       |
| `resources` | `List` all resources available in kkaf     | TODO       |
| `describe`  | `Describe` a resource in kafka cluster     | TODO       |
| `create`    | `Create` a resource on kafka cluster       | TODO       |
| `consume`   | Consume messages from a topic              | TODO       |
| `produce`   | Produce record. Reads data from stdin.     | TODO       |
| `group`     | Display information about consumer groups. | TODO       |
| `query`     | Query topic by key                         | TODO       |

### `config`

| Subcommand     | Description              | Status |
|----------------|--------------------------|--------|
| `get-clusters` | List registered clusters | TODO   |
| `use-cluster`  | Use a cluster            | TODO   |
| `add-cluster`  | Add a cluster            | TODO   |

## Referemces

- [kaf](https://github.com/birdayz/kaf)
- []

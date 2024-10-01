# kkaf - kubernetes-usable Kaf Specification

## Overview

kkaf is toy project to make kaf usable in kubernetes. This document describes the specification of kkaf.
In this document, features and main concepts of kkaf are described.

## Main Concepts

1. kkaf should be able to communicate with kubernetes services, which are not exposed to the internet (NodePort or something)
2. kkaf is CLI based on cobra and viper.
3. kkaf should provide `status` command to check the status and health of kafka cluster.
4. kaf's main feature has to be provided in kkaf

## Features

### kaf command specification

| Command | Description | 
|--------|-------------|
| config |             |

config      Handle kaf configuration
consume     Consume messages
group       Display information about consumer groups.
groups      List groups
help        Help about any command
node        Describe and List nodes
nodes       List nodes in a cluster
produce     Produce record. Reads data from stdin.
query       Query topic by key
topic       Create and describe topics.
topics      List topics


## Referemces

- [kaf](https://github.com/birdayz/kaf)
- []

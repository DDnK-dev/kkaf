# Kaf Commands

## Document Purpose

This document describes the commands of `kaf` CLI.
This is written to check the depth of the commands of `kaf` or how to use them to check what functions are available and how to use them in `kaf`.

## Commands Overview

### **root**

> kaf -h

```text
Kafka Command Line utility for cluster management

Usage:
kaf [command]

Available Commands:
completion  Generate completion script for bash, zsh, fish or powershell
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

Flags:
-b, --brokers strings          Comma separated list of broker ip:port pairs
-c, --cluster string           set a temporary current cluster
--config string            config file (default is $HOME/.kaf/config)
-h, --help                     help for kaf
--schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
-v, --verbose                  Whether to turn on sarama logging
--version                  version for kaf
```

----

### **config**

> kaf config -h

```text
Handle kaf configuration

Usage:
kaf config [command]

Available Commands:
add-cluster     Add cluster
add-eventhub    Add Azure EventHub
current-context Displays the current context
get-clusters    Display clusters in the configuration file
import          Import configurations into the $HOME/.kaf/config file
remove-cluster  remove cluster
select-cluster  Interactively select a cluster
use-cluster     Sets the current cluster in the configuration

Flags:
-h, --help   help for config

Global Flags:
-b, --brokers strings          Comma separated list of broker ip:port pairs
-c, --cluster string           set a temporary current cluster
--config string            config file (default is $HOME/.kaf/config)
--schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
-v, --verbose                  Whether to turn on sarama logging

Use "kaf config [command] --help" for more information about a command.
```

---

> kaf config add-cluster -h

```text
Add cluster

Usage:
  kaf config add-cluster [NAME] [flags]

Flags:
      --broker-version string   Broker Version. Available Versions: [0.8.2.0 0.8.2.1 0.8.2.2 0.9.0.0 0.9.0.1 0.10.0.0 0.10.0.1 0.10.1.0 0.10.1.1 0.10.2.0 0.10.2.1 0.10.2.2 0.11.0.0 0.11.0.1 0.11.0.2 1.0.0 1.0.1 1.0.2 1.1.0 1.1.1 2.0.0 2.0.1 2.1.0 2.1.1 2.2.0 2.2.1 2.2.2 2.3.0 2.3.1 2.4.0 2.4.1 2.5.0 2.5.1 2.6.0 2.6.1 2.6.2 2.7.0 2.7.1 2.8.0 2.8.1 2.8.2 3.0.0 3.0.1 3.0.2 3.1.0 3.1.1 3.1.2 3.2.0 3.2.1 3.2.2 3.2.3 3.3.0 3.3.1 3.3.2 3.4.0 3.4.1 3.5.0 3.5.1 3.6.0]
  -h, --help                    help for add-cluster

Global Flags:
  -b, --brokers strings          Comma separated list of broker ip:port pairs
  -c, --cluster string           set a temporary current cluster
      --config string            config file (default is $HOME/.kaf/config)
      --schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
  -v, --verbose                  Whether to turn on sarama logging
```

---

> kaf config add-eventhub -h

```text
Add cluster

Usage:
  kaf config add-cluster [NAME] [flags]

Flags:
      --broker-version string   Broker Version. Available Versions: [0.8.2.0 0.8.2.1 0.8.2.2 0.9.0.0 0.9.0.1 0.10.0.0 0.10.0.1 0.10.1.0 0.10.1.1 0.10.2.0 0.10.2.1 0.10.2.2 0.11.0.0 0.11.0.1 0.11.0.2 1.0.0 1.0.1 1.0.2 1.1.0 1.1.1 2.0.0 2.0.1 2.1.0 2.1.1 2.2.0 2.2.1 2.2.2 2.3.0 2.3.1 2.4.0 2.4.1 2.5.0 2.5.1 2.6.0 2.6.1 2.6.2 2.7.0 2.7.1 2.8.0 2.8.1 2.8.2 3.0.0 3.0.1 3.0.2 3.1.0 3.1.1 3.1.2 3.2.0 3.2.1 3.2.2 3.2.3 3.3.0 3.3.1 3.3.2 3.4.0 3.4.1 3.5.0 3.5.1 3.6.0]
  -h, --help                    help for add-cluster

Global Flags:
  -b, --brokers strings          Comma separated list of broker ip:port pairs
  -c, --cluster string           set a temporary current cluster
      --config string            config file (default is $HOME/.kaf/config)
      --schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
  -v, --verbose                  Whether to turn on sarama logging
```

---

> kaf config current-context -h

```text
Add cluster

Usage:
  kaf config add-cluster [NAME] [flags]

Flags:
      --broker-version string   Broker Version. Available Versions: [0.8.2.0 0.8.2.1 0.8.2.2 0.9.0.0 0.9.0.1 0.10.0.0 0.10.0.1 0.10.1.0 0.10.1.1 0.10.2.0 0.10.2.1 0.10.2.2 0.11.0.0 0.11.0.1 0.11.0.2 1.0.0 1.0.1 1.0.2 1.1.0 1.1.1 2.0.0 2.0.1 2.1.0 2.1.1 2.2.0 2.2.1 2.2.2 2.3.0 2.3.1 2.4.0 2.4.1 2.5.0 2.5.1 2.6.0 2.6.1 2.6.2 2.7.0 2.7.1 2.8.0 2.8.1 2.8.2 3.0.0 3.0.1 3.0.2 3.1.0 3.1.1 3.1.2 3.2.0 3.2.1 3.2.2 3.2.3 3.3.0 3.3.1 3.3.2 3.4.0 3.4.1 3.5.0 3.5.1 3.6.0]
  -h, --help                    help for add-cluster

Global Flags:
  -b, --brokers strings          Comma separated list of broker ip:port pairs
  -c, --cluster string           set a temporary current cluster
      --config string            config file (default is $HOME/.kaf/config)
      --schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
  -v, --verbose                  Whether to turn on sarama logging
```

---

> kaf config get-clusters -h

```text
Add cluster

Usage:
  kaf config add-cluster [NAME] [flags]

Flags:
      --broker-version string   Broker Version. Available Versions: [0.8.2.0 0.8.2.1 0.8.2.2 0.9.0.0 0.9.0.1 0.10.0.0 0.10.0.1 0.10.1.0 0.10.1.1 0.10.2.0 0.10.2.1 0.10.2.2 0.11.0.0 0.11.0.1 0.11.0.2 1.0.0 1.0.1 1.0.2 1.1.0 1.1.1 2.0.0 2.0.1 2.1.0 2.1.1 2.2.0 2.2.1 2.2.2 2.3.0 2.3.1 2.4.0 2.4.1 2.5.0 2.5.1 2.6.0 2.6.1 2.6.2 2.7.0 2.7.1 2.8.0 2.8.1 2.8.2 3.0.0 3.0.1 3.0.2 3.1.0 3.1.1 3.1.2 3.2.0 3.2.1 3.2.2 3.2.3 3.3.0 3.3.1 3.3.2 3.4.0 3.4.1 3.5.0 3.5.1 3.6.0]
  -h, --help                    help for add-cluster

Global Flags:
  -b, --brokers strings          Comma separated list of broker ip:port pairs
  -c, --cluster string           set a temporary current cluster
      --config string            config file (default is $HOME/.kaf/config)
      --schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
  -v, --verbose                  Whether to turn on sarama logging
```

---

> kaf config import -h

```text
Import configurations into the $HOME/.kaf/config file

Usage:
  kaf config import [ccloud] [flags]

Flags:
  -h, --help   help for import

Global Flags:
  -b, --brokers strings          Comma separated list of broker ip:port pairs
  -c, --cluster string           set a temporary current cluster
      --config string            config file (default is $HOME/.kaf/config)
      --schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
  -v, --verbose                  Whether to turn on sarama logging
```

---

> kaf config remove-cluster -h

```text
Import configurations into the $HOME/.kaf/config file

Usage:
  kaf config import [ccloud] [flags]

Flags:
  -h, --help   help for import

Global Flags:
  -b, --brokers strings          Comma separated list of broker ip:port pairs
  -c, --cluster string           set a temporary current cluster
      --config string            config file (default is $HOME/.kaf/config)
      --schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
  -v, --verbose                  Whether to turn on sarama logging
```

---

> kaf config select-cluster -h

```text
Import configurations into the $HOME/.kaf/config file

Usage:
  kaf config import [ccloud] [flags]

Flags:
  -h, --help   help for import

Global Flags:
  -b, --brokers strings          Comma separated list of broker ip:port pairs
  -c, --cluster string           set a temporary current cluster
      --config string            config file (default is $HOME/.kaf/config)
      --schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
  -v, --verbose                  Whether to turn on sarama logging
```

---

> kaf config use-cluster -h

```text
Import configurations into the $HOME/.kaf/config file

Usage:
  kaf config import [ccloud] [flags]

Flags:
  -h, --help   help for import

Global Flags:
  -b, --brokers strings          Comma separated list of broker ip:port pairs
  -c, --cluster string           set a temporary current cluster
      --config string            config file (default is $HOME/.kaf/config)
      --schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
  -v, --verbose                  Whether to turn on sarama logging
```

---

### **consume**

> kaf consume -h

```text
Consume messages

Usage:
  kaf consume TOPIC [flags]

Flags:
      --commit                  Commit Group offset after receiving messages. Works only if consuming as Consumer Group
      --decode-msgpack          Enable deserializing msgpack
  -f, --follow                  Continue to consume messages until program execution is interrupted/terminated
  -g, --group string            Consumer Group to use for consume
  -h, --help                    help for consume
      --key-proto-type string   Fully qualified name of the proto key type. Example: com.test.SampleMessage
  -l, --limit-messages int      Limit messages per partition
      --offset string           Offset to start consuming. Possible values: oldest, newest, or integer. (default "oldest")
      --output OutputFormat     Set output format messages: default, raw (without key or prettified JSON), json (default default)
  -p, --partitions int32Slice   Partitions to consume from (default [])
      --proto-exclude strings   Proto exclusions (path prefixes)
      --proto-include strings   Path to proto files
      --proto-type string       Fully qualified name of the proto message type. Example: com.test.SampleMessage
  -n, --tail int32              Print last n messages per partition

Global Flags:
  -b, --brokers strings          Comma separated list of broker ip:port pairs
  -c, --cluster string           set a temporary current cluster
      --config string            config file (default is $HOME/.kaf/config)
      --schema-registry string   URL to a Confluent schema registry. Used for attempting to decode Avro-encoded messages
  -v, --verbose                  Whether to turn on sarama logging
```

### 
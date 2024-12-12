---
uid: Connector_help_Techex_Darwin
---

# Techex Darwin

The Techex Darwin connector can display configuration via the REST API and metrics by consuming Kafka messages.

The microservice-based tx darwin platform is used for live media processing, transport, and monitoring, and is designed for both hybrid and pure cloud software workflows.

## About

### Version Info

| Range              | Features                   | Based on | System Impact |
|--------------------|----------------------------|----------|---------------|
| 1.0.0.x            | Initial version.           | -        | -             |
| 1.0.1.x [SLC Main] | Update for firmware 1.4.2. | 1.0.0.2  | -             |

### Product Info

| Range   | Supported Firmware |
|---------|--------------------|
| 1.0.0.x | 1.4.0              |
| 1.0.1.x | 1.4.2              |

### System Info

| Range   | DCF Integration | Cassandra Compliant | Linked Components | Exported Components |
|---------|-----------------|---------------------|-------------------|---------------------|
| 1.0.0.x | No              | Yes                 | -                 | -                   |
| 1.0.1.x | No              | Yes                 | -                 | -                   |

## Configuration

### Connections

#### HTTP Connection

This connector uses an HTTP connection and requires the following input during element creation:

HTTP CONNECTION:

- **IP address/host**: The polling IP or URL of the destination.
- **IP port**: The IP port of the destination.
- **Device address**: The bus address of the device. If the proxy server has to be bypassed, specify *BypassProxy*.

### Initialization

For the REST API to work, the **Username** and **Password** need to be configured on the **General** page.

In addition, for the connector to start receiving Kafka messages, the following parameters need to be configured:

- **Bootstrap Server**
- **Port**
- **Client ID** (optional)
- **Group ID** (optional)

Finally, an entry in the **Kafka Topic Subscriptions** needs to be created specifying the topic name.

## How to Use

To poll REST API data, the username and password need to be filled in. You can then control the commands that are sent and their frequency using the **Poll Manager Table**.

To subscribe to start receiving Kafka messages after configuring the parameters above, click **Consume** to start the connection. The **Connection** parameter on the same page will show if this operation worked.

For Kafka messages to work, the **Modules** command in the **Poll Manager Table** needs to be enabled. Once this command has been sent at least once, data will be filled in in the **Schema Modules Table** on the **General** page, and you will be able to control the processing and frequency for each module from there.

### Layout

The connector is split in two main parts: Config and Metrics. Any table that ends with "config" contains information from the REST API, while metrics include information from Kafka.

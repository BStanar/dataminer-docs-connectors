---
uid: Connector_help_Axon_ACP_-_GEP100
---

# Axon ACP - GEP100

The GEP100 is a 3 Gb/s, HD, SD embedded domain Dolby-E to PCM decoder with audio shuffler.

The **Axon ACP - GEP100** connector can be used to display and configure information related to this device.

## About

This connector is automatically generated by the connector **Axon ACP**.

There are different possibilities available for **alarm monitoring** and **trending**.

### Version Info

| Range     | Description                        | DCF Integration     | Cassandra Compliant     |
|------------------|------------------------------------|---------------------|-------------------------|
| 1.0.2.x          | Change in export rules.            | Yes                 | Yes                     |
| 1.0.3.x          | Change in discrete display values. | Yes                 | Yes                     |

### Product Info

| Range | Supported Firmware Version |
|------------------|-----------------------------|
| 1.0.2.x          | 3128                        |
| 1.0.3.x          | 3128                        |

## Installation and configuration

### Creation

This element is automatically created by the parent element using the **Axon ACP** connector.

## Usage

This element has the following data pages:

- **General**: This page displays general information about the card: **Card Name**, **Card Description**, **SW Revision**, **HW Revision**, etc.
- **SDI**
- **Output**
- **Add-On**
- **Video**
- **Preset**
- **Meta Data**
- **Miscellaneous**
- **Audio**
- **Embedder**
- **Embedder A**
- **Embedder B**
- **Embedder C**
- **Embedder D**
- **Dolby**
- **Dolby Digital**
- **Dolby Decoder**
- **Alarm Priority**: This page displays the event messages of the card, i.e. special messages generated asynchronously on the card.

## DataMiner Connectivity Framework

The Axon ACP connector supports the usage of DCF.

DCF can also be implemented through the DataMiner DCF user interface and through DataMiner third-party connectors (for instance a manager).

Connectivity for this protocol is managed by the parent protocol Axon ACP.

### Interfaces

#### Physical Interfaces

- **SDI Input 1**: A single fixed interface of type **input**.
- **SDI Input 2**: A single fixed interface of type **input**.
- **QUAD-SPEED SYNAPSE Bus Input**: A single fixed interface of type **input**.
- **SDI Output 1**: A single fixed interface of type **output**.
- **SDI Output 2**: A single fixed interface of type **output**.
- **QUAD-SPEED SYNAPSE Bus Output**: A single fixed interface of type **output**.

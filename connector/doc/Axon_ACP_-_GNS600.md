---
uid: Connector_help_Axon_ACP_-_GNS600
---

# Axon ACP - GNS600

The GNS600 is a 3G, HD and SD SDI SCTE104 inserter with SDI inputs and outputs. SCTE104 information present in the SDI signal can be transcoded and inserted into the main 3G, HD or SD SDI signal. The GNS600 can insert data from both the Ethernet and SDI domain into lines in the SDI domain or insert a user-defined cue on a preset base.

The **Axon ACP - GNS600** connector can be used to display and configure information related to this device.

## About

This connector is automatically generated by the connector **Axon ACP**.

There are different possibilities available for **alarm monitoring** and **trending**.

### Version Info

| Range | Description | DCF Integration | Cassandra Compliant |
|------------------|-----------------|---------------------|-------------------------|
| 1.0.3.x          | Initial version | Yes                 | Yes                     |

### Product Info

| Range | Supported Firmware Version |
|------------------|-----------------------------|
| 1.0.3.x          | 1407                        |

## Installation and configuration

### Creation

This element is automatically created by the parent element using the **Axon ACP** connector.

## Usage

This element has the following pages:

- **General**: This page displays general information about the card: **Card Name**, **Card Description**, **SW Revision**, **HW Revision**, etc.
- Status
- Video Status
- S2010 Status
- SCTE104 Status
- S2016 Status
- S2031-OP47-WST Status
- GPI Mode Status
- Video
- Delay
- S2010
- SCTE104
- S2016
- S2031-OP47-WST
- GPI Mode
- Teletext
- X31
- Network
- Network Status
- **Alarm Priority**: This page displays the event messages of the card, i.e. special messages generated asynchronously on the card.

## DataMiner Connectivity Framework

The Axon ACP connector supports the usage of DCF.

DCF can also be implemented through the DataMiner DCF user interface and through DataMiner third-party connectors (for instance a manager).

Connectivity for this protocol is managed by the parent protocol Axon ACP.

### Interfaces

#### Physical Interfaces

- **SDI Input 1**: A single fixed interface of type **input**.
- **SDI Input 2**: A single fixed interface of type **input**.
- **SDI Input 3**: A single fixed interface of type **input**.
- **SDI Input 4**: A single fixed interface of type **input**.
- **SDI Output 1**: A single fixed interface of type **output**.
- **SDI Output 2**: A single fixed interface of type **output**.
- **SDI Output 3**: A single fixed interface of type **output**.
- **SDI Output 4**: A single fixed interface of type **output**.

#### Virtual Interfaces

- **Internal Switch**: A single fixed interface of type **inout.**

Connections

#### Internal Connections

When a DVE child element is created, the following connections are established:

- Between **Internal Switch** and **SDI Output 1**.
- Between **Internal Switch** and **SDI Output 2**
- Between **Internal Switch** and **SDI Output 3**.
- Between **Internal Switch** and **SDI Output 4**.

Depending on the state of the **Input Select**, the following connections are established:

- **SDI-1**: Between **SDI Input 1** and **Internal Switch**.
- **SDI-2**: Between **SDI Input 2** and **Internal Switch**.
- **SDI-3**: Between **SDI Input 3** and **Internal Switch**.
- **SDI-4**: Between **SDI Input 4** and **Internal Switch**.

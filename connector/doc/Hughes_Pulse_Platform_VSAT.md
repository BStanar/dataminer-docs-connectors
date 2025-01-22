---
uid: Connector_help_Hughes_Pulse_Platform_VSAT
---

# Hughes Pulse Platform VSAT

The Hughes Pulse Platform VSAT connector facilitates the integration of Hughes Pulse API data into a DataMiner System. This connector allows users to configure and poll various endpoints from the Hughes Pulse Platform to retrieve and display information about remote devices and their status.

## About

### Version Info

| Range              | Features                                         | Based on | System Impact |
|--------------------|--------------------------------------------------|----------|---------------|
| 1.0.0.x [SLC Main] | Initial release. Supports basic API integration. | -        | -             |

### Product Info

| Range      | Supported Firmware          |
|------------|-----------------------------|
| 1.0.0.x    | Hughes Pulse API V1         |

### System Info

| Range   | DCF Integration | Cassandra Compliant | Linked Components | Exported Components |
|---------|-----------------|---------------------|-------------------|---------------------|
| 1.0.0.x | No              | Yes                 | -                 | -                   |

## Configuration

### Connections

#### HTTP Connection

This connector uses an HTTP connection and requires the following input during element creation:

HTTP CONNECTION:

- **IP address/host**: `https://api.hugheson.net`
- **IP port**: `443` (default)

### Initialization

When you have created an element with this connector, you will then need to configure the REST API credentials, including the username, password, and maximum login retries.

The system will automatically generate a token upon successful login, with the status displayed as *Token Created* and the **Token Expiration** parameter set to one hour from the current time.

## How to use

The Hughes Pulse Platform VSAT connector primarily communicates with the Hughes Pulse API using HTTP REST calls. The connector provides a configurable interface for managing API endpoints, including polling intervals and response display.

### Configuration Page

On the **Configuration** page, users can set the REST API username and password, and configure the maximum login retries. You can use the **Login** button to manually trigger the login process, generating a new token when required.

### REST API Endpoints Page

The **REST API Endpoints Configuration** table, accessible from the REST API Endpoints page, allows you to add, edit, or delete API endpoint configurations. Upon element startup, the connector automatically adds two essential endpoints:

1. **Endpoint:** `assets/device?san=*`
   - **Category:** Remotes
   - **Timer:** 30 minutes
   - **Purpose:** Populates the columns in the Remotes Table.

1. **Endpoint:** `assets/device?san=*&fields=["name","state"]`
   - **Category:** Remotes
   - **Timer:** 5 minutes
   - **Purpose:** Provides the data for the **Current Device Status** in the Remotes Table.

You can also add other endpoints, which should be categorized as *N/A*. The table also includes options to enable or disable polling and to display the API response for debugging purposes. Each row in the table has a **Poll** button to manually trigger the GET request outside of the defined timer.

### Collector Setup Page

The **Collector Setup** page contains settings for managing entities, including options for enabling automatic entity removal and configuring the removal period. This feature clears entries in the tables that have not been updated within the specified period.

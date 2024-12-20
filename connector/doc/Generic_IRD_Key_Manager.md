---
uid: Connector_help_Generic_IRD_Key_Manager
---

# Generic IRD Key Manager

This connector is used to upload key files to elements running an Ericsson RX8200 connector.

## About

### Version Info

| Range     | Key Features                                                 | Based on     | System Impact     |
|-----------|--------------------------------------------------------------|--------------|-------------------|
| 1.0.0.x   | Uploading key files to IRDs.                                 | -            | -                 |
| 1.0.1.x   | More Convenient way to deal with uploading files (see notes).| 1.0.0.4      | -                 |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | -                     | -                       |
| 1.0.1.x   | No                  | Yes                     | -                     | -                       |

## Configuration

### Connections

#### Virtual connection

This connector uses a virtual connection and does not require any input during element creation.

## How to use

### General

This page displays the **IRD Key Encryption Upload Table**, which consists of a list of all available elements running either the Ericsson RX8200 or MediaKind RX1 connector. This list is continuously updated and can also be manually refreshed with the Refresh List button.

Uploading key files can be done for each element separately or for all of them at once. Elements can be excluded from this process with the **Include/Exclude Element** toggle button.

On the **Config** subpage, you can set the directory and file to select the key file on the devices. You can also select to automatically apply the most recent file that is available in the directory.

### Notes

**File Upload Process in Range 1.0.0.X**:

1) The connector reads the referenced folder (typically a DataMiner Documents folder) and lists the files in a dropdown menu.
2) The user can select one file at a time by choosing an item from the dropdown menu.
3) After selecting a file, the user must perform an additional click to move the file to the table where the files to be uploaded are listed.

**File Upload Process from Range 1.0.1.X Onward**:

1) The connector reads the files from the referenced folder and places them directly into the table. Any changes (addition or removal of files) in the folder are automatically reflected in the table.
2) The user retains the option to include or exclude a file from being uploaded using the same table column as in range 1.0.0.X.
3) When using the table’s Delete button, the file entry is removed from both the table and the actual folder. This change is also synchronized across the cluster, if applicable.


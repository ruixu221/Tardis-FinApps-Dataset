# Tardis-FinApps-Dataset

The Financial Applications (FinApps) dataset is collected from the production environments of the backbone network of a financial institution. We independently collect two subsets of data in March and May 2024, each through a 2-minute packet capture with our network management system. When capturing packets, we truncate them before the payload content to ensure that user information is not collected.

As mentioned in the paper, we use the Configuration Management Database (CMDB) to label the applications, resulting in 60 unique applications for each subset. Besides applications that are directly identifiable with the Database, we group the remaining traffic data into 4 additional categories:

- Unknown: Neither the source nor the destination IP address matches any known application in the CMDB.

- Conflict: The source and destination IP addresses match different applications in the CMDB.

- One-to-Many: The IP addresses match multiple applications in the CMDB.

- One-to-Many & Conflict: The IP addresses match multiple applications in the CMDB, and the source and destination IP addresses match different applications.

In order to facilitate the reproducibility of our work and promote further research in the field, we plan to release the FinApps dataset after proper anonymization. The released dataset will comply with the following format: Each dataset will consist of several CSV files, each corresponding to a specific application. Within the CSV file, each row will represent a packet, with the columns listed in the Table below.

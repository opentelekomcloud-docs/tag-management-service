:original_name: en-us_topic_0056858747.html

.. _en-us_topic_0056858747:

TMS and Other Services
======================

-  Services that support TMS

   TMS allows you to manage resource tags centrally. For details about services supported by TMS, see :ref:`Table 1 <en-us_topic_0056858747__table256483375112>`.

   A cloud service may contain multiple resource types. You can specify a resource type and then centrally manage tags on TMS console as need.

   .. _en-us_topic_0056858747__table256483375112:

   .. table:: **Table 1** Services that support TMS

      +------------------------------------+----------------------------------------+
      | Service                            | Resource Type                          |
      +====================================+========================================+
      | Auto Scaling                       | AS-AS group                            |
      +------------------------------------+----------------------------------------+
      | Bare Metal Server (BMS)            | BMS-BMS                                |
      +------------------------------------+----------------------------------------+
      | Cloud Container Engine (CCE)       | CCE-Cluster                            |
      +------------------------------------+----------------------------------------+
      | Cloud Server Backup Service (CSBS) | -  CSBS-Backup                         |
      |                                    | -  CSBS-Backup policy                  |
      +------------------------------------+----------------------------------------+
      | Cloud Search Service (CSS)         | CSS-Cluster                            |
      +------------------------------------+----------------------------------------+
      | Cloud Backup and Recovery (CBR)    | CBR-Vault                              |
      +------------------------------------+----------------------------------------+
      | Distributed Cache Service (DCS)    | DCS-DCS                                |
      +------------------------------------+----------------------------------------+
      | Document Database Service (DDS)    | DDS-DB instance                        |
      +------------------------------------+----------------------------------------+
      | Dedicated Host                     | Dedicated host                         |
      +------------------------------------+----------------------------------------+
      | Data Lake Insight (DLI)            | -  DLI-BasicDatasource                 |
      |                                    | -  DLI-Queue                           |
      +------------------------------------+----------------------------------------+
      | Distributed Message Service (DMS)  | Kafka                                  |
      +------------------------------------+----------------------------------------+
      | Domain Name Service (DNS)          | -  DNS-Private zone                    |
      |                                    | -  DNS-PTR record                      |
      |                                    | -  DNS-Private record set              |
      +------------------------------------+----------------------------------------+
      | Data Replication Service (DRS)     | -  DRS-Data Synchronization Task       |
      |                                    | -  DRS-Data Subscription Task          |
      |                                    | -  DRS-Disaster Recovery Task          |
      |                                    | -  DRS-Backup Migration Task           |
      |                                    | -  DRS-Online Migration Task           |
      +------------------------------------+----------------------------------------+
      | Database Security Service (DBSS)   | DBSS                                   |
      +------------------------------------+----------------------------------------+
      | Elastic Cloud Server (ECS)         | ECS-ECS                                |
      +------------------------------------+----------------------------------------+
      | Elastic IP (EIP)                   | EIP-EIP                                |
      +------------------------------------+----------------------------------------+
      | Elastic Load Balance (ELB)         | -  ELB-Enhanced load balancer          |
      |                                    | -  ELB-Enhanced load balancer listener |
      +------------------------------------+----------------------------------------+
      | Elastic Volume Service (EVS)       | EVS-Disk                               |
      +------------------------------------+----------------------------------------+
      | GaussDB                            | GaussDB instance                       |
      +------------------------------------+----------------------------------------+
      | GaussDB NoSQL                      | GeminiDB-Instance                      |
      +------------------------------------+----------------------------------------+
      | Image Management Service (IMS)     | IMS-Private image                      |
      +------------------------------------+----------------------------------------+
      | Key Management Service (KMS)       | KMS-Key                                |
      +------------------------------------+----------------------------------------+
      | MapReduce Service (MRS)            | MRS-Cluster                            |
      +------------------------------------+----------------------------------------+
      | NAT Gateway                        | NAT-Public NAT gateway                 |
      +------------------------------------+----------------------------------------+
      | Object Storage Service (OBS)       | OBS-Bucket                             |
      +------------------------------------+----------------------------------------+
      | Relational Database Service (RDS)  | RDS-DB instance                        |
      +------------------------------------+----------------------------------------+
      | Scalable File Service (SFS)        | SFS-File system                        |
      +------------------------------------+----------------------------------------+
      | Simple Message Notification (SMN)  | Topic                                  |
      +------------------------------------+----------------------------------------+
      | Volume Backup Service (VBS)        | -  VBS-Backup                          |
      |                                    | -  VBS-Backup policy                   |
      +------------------------------------+----------------------------------------+
      | VPC Endpoint (VPCEP)               | -  VPC-Endpoint                        |
      |                                    |                                        |
      |                                    | -  VPC-Endpoint service                |
      +------------------------------------+----------------------------------------+
      | Virtual Private Cloud (VPC)        | -  VPC-VPC                             |
      |                                    | -  VPC-Subnet                          |
      +------------------------------------+----------------------------------------+
      | Virtual Private Network (VPN)      | VPN-VPN                                |
      +------------------------------------+----------------------------------------+
      | Web Application Firewall (WAF)     | WAF-Domain                             |
      +------------------------------------+----------------------------------------+

-  Related services

   .. table:: **Table 2** Relationships with other services

      +-----------------------------------------------------------------------------------------------------------+---------------------------+-----------------------------------------------+
      | Function                                                                                                  | Service                   | Reference                                     |
      +===========================================================================================================+===========================+===============================================+
      | With CTS, you can record operations associated with TMS for later query, audit, and backtrack operations. | Cloud Trace Service (CTS) | :ref:`Interconnecting with CTS <tms_06_0001>` |
      +-----------------------------------------------------------------------------------------------------------+---------------------------+-----------------------------------------------+

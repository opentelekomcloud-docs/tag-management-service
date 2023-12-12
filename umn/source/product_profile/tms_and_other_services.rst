:original_name: en-us_topic_0056858747.html

.. _en-us_topic_0056858747:

TMS and Other Services
======================

-  Services that support TMS

   TMS provides central management for all tags of the cloud resources listed in :ref:`Table 1 <en-us_topic_0056858747__table256483375112>`.

   A cloud service can have multiple resource types. You can select a resource type as required on the TMS console and manage the tags of this type of resources in a centralized manner.

   .. _en-us_topic_0056858747__table256483375112:

   .. table:: **Table 1** Services that support TMS

      +------------------------------------+----------------------------------------+
      | Service                            | Resource Type                          |
      +====================================+========================================+
      | VPC Endpoint (VPCEP)               | -  VPC-Endpoint                        |
      |                                    |                                        |
      |                                    | -  VPC-Endpoint service                |
      +------------------------------------+----------------------------------------+
      | Data Replication Service (DRS)     | -  DRS-Data Synchronization Task       |
      |                                    | -  DRS-Disaster Recovery Task          |
      |                                    | -  DRS-Backup Migration Task           |
      |                                    | -  DRS-Online Migration Task           |
      +------------------------------------+----------------------------------------+
      | Bare Metal Server (BMS)            | BMS-BMS                                |
      +------------------------------------+----------------------------------------+
      | Elastic Cloud Server (ECS)         | ECS-ECS                                |
      +------------------------------------+----------------------------------------+
      | Virtual Private Cloud (VPC)        | -  VPC-VPC                             |
      |                                    | -  VPC-Subnet                          |
      +------------------------------------+----------------------------------------+
      | Elastic IP (EIP)                   | VPC-EIP                                |
      +------------------------------------+----------------------------------------+
      | Elastic Volume Service (EVS)       | EVS-Disk                               |
      +------------------------------------+----------------------------------------+
      | Volume Backup Service (VBS)        | -  VBS-Backup                          |
      |                                    | -  VBS-Backup policy                   |
      +------------------------------------+----------------------------------------+
      | Auto Scaling                       | AS-AS group                            |
      +------------------------------------+----------------------------------------+
      | Image Management Service (IMS)     | IMS-Private image                      |
      +------------------------------------+----------------------------------------+
      | Key Management Service (KMS)       | KMS-Key                                |
      +------------------------------------+----------------------------------------+
      | Domain Name Service (DNS)          | -  DNS-Private zone                    |
      |                                    | -  DNS-PTR record                      |
      |                                    | -  DNS-Private record set              |
      +------------------------------------+----------------------------------------+
      | Virtual Private Network (VPN)      | VPN-VPN                                |
      +------------------------------------+----------------------------------------+
      | Scalable File Service (SFS)        | SFS-File system                        |
      +------------------------------------+----------------------------------------+
      | Cloud Server Backup Service (CSBS) | -  CSBS-Backup                         |
      |                                    | -  CSBS-Backup policy                  |
      +------------------------------------+----------------------------------------+
      | Elastic Load Balance (ELB)         | -  ELB-Enhanced load balancer          |
      |                                    | -  ELB-Enhanced load balancer listener |
      +------------------------------------+----------------------------------------+
      | SMN                                | SMN-Topic                              |
      +------------------------------------+----------------------------------------+
      | Distributed Message Service (DMS)  | Kafka                                  |
      +------------------------------------+----------------------------------------+
      | Relational Database Service (RDS)  | RDS-DB instance                        |
      +------------------------------------+----------------------------------------+
      | MapReduce Service (MRS)            | MRS-Cluster                            |
      +------------------------------------+----------------------------------------+
      | Document Database Service (DDS)    | DDS-DB instance                        |
      +------------------------------------+----------------------------------------+
      | Web Application Firewall (WAF)     | WAF-domain                             |
      +------------------------------------+----------------------------------------+
      | Dedicated host                     | DeH-DeH                                |
      +------------------------------------+----------------------------------------+
      | Cloud Backup and Recovery (CBR)    | CBR-Vault                              |
      +------------------------------------+----------------------------------------+
      | GaussDB                            | GaussDB instance                       |
      +------------------------------------+----------------------------------------+
      | GaussDB NoSQL                      | GeminiDB-Instance                      |
      +------------------------------------+----------------------------------------+

-  Related services

   .. table:: **Table 2** Relationships with other services

      +-----------------------------------------------------------------------------------------------------------+---------------------------+-----------------------------------------------+
      | Function                                                                                                  | Service                   | Reference                                     |
      +===========================================================================================================+===========================+===============================================+
      | With CTS, you can record operations associated with TMS for later query, audit, and backtrack operations. | Cloud Trace Service (CTS) | :ref:`Interconnecting with CTS <tms_06_0001>` |
      +-----------------------------------------------------------------------------------------------------------+---------------------------+-----------------------------------------------+

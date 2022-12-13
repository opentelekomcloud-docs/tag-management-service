:original_name: en-us_topic_0056858747.html

.. _en-us_topic_0056858747:

TMS and Other Services
======================

-  Services that support central management of tags

   TMS provides central management for all tags of all cloud resources. Services listed in :ref:`Table 1 <en-us_topic_0056858747__table564615341427>` are supported.

   A cloud service can contain multiple resource types. You can select a resource type as required on the TMS console and manage the tags of this type of resources in a centralized manner.

   .. _en-us_topic_0056858747__table564615341427:

   .. table:: **Table 1** Services that support TMS

      +------------------------------------+------------------------------------+
      | Service                            | Resource Type                      |
      +====================================+====================================+
      | Bare Metal Server (BMS)            | BMS                                |
      +------------------------------------+------------------------------------+
      | Elastic Cloud Server (ECS)         | ECS                                |
      +------------------------------------+------------------------------------+
      | Object Storage Service (OBS)       | Bucket                             |
      +------------------------------------+------------------------------------+
      | Virtual Private Cloud (VPC)        | -  VPC                             |
      |                                    | -  Subnet                          |
      |                                    | -  EIP                             |
      +------------------------------------+------------------------------------+
      | Elastic Volume Service (EVS)       | Disk                               |
      +------------------------------------+------------------------------------+
      | Volume Backup Service (VBS)        | -  Backup                          |
      |                                    | -  Backup policy                   |
      +------------------------------------+------------------------------------+
      | Auto Scaling (AS)                  | AS group                           |
      +------------------------------------+------------------------------------+
      | Image Management Service (IMS)     | Private image                      |
      +------------------------------------+------------------------------------+
      | Key Management Service (KMS)       | Key                                |
      +------------------------------------+------------------------------------+
      | Domain Name Service (DNS)          | -  Private zone                    |
      |                                    | -  Public zone                     |
      |                                    | -  PTR record                      |
      |                                    | -  Private record set              |
      |                                    | -  Public record set               |
      +------------------------------------+------------------------------------+
      | Virtual Private Network (VPN)      | VPN                                |
      +------------------------------------+------------------------------------+
      | Scalable File Service (SFS)        | File system                        |
      +------------------------------------+------------------------------------+
      | Cloud Server Backup Service (CSBS) | -  Backup                          |
      |                                    | -  Backup policy                   |
      +------------------------------------+------------------------------------+
      | Elastic Load Balancing (ELB)       | -  Enhanced load balancer          |
      |                                    | -  Enhanced load balancer listener |
      +------------------------------------+------------------------------------+
      | NAT Gateway                        | NAT gateway                        |
      +------------------------------------+------------------------------------+
      | Simple Message Notification (SMN)  | Topic                              |
      +------------------------------------+------------------------------------+
      | Distributed Message Service (DMS)  | Queue                              |
      +------------------------------------+------------------------------------+
      | Relational Database Service (RDS)  | DB instance                        |
      +------------------------------------+------------------------------------+
      | MapReduce Service (MRS)            | Cluster                            |
      +------------------------------------+------------------------------------+
      | Data Warehouse Service (DWS)       | Cluster                            |
      +------------------------------------+------------------------------------+
      | Document Database Service (DDS)    | DB instance                        |
      +------------------------------------+------------------------------------+
      | Data Ingestion Service (DIS)       | Stream                             |
      +------------------------------------+------------------------------------+
      | Dedicated Host (DeH)               | DeH                                |
      +------------------------------------+------------------------------------+

-  CTS

   With CTS, you can record operations associated with TMS for later query, audit, and backtrack operations. Once CTS is enabled, it starts to record operations on cloud service resources. For details about how to view audit logs, see :ref:`Viewing CTS Traces <en-us_topic_0110866980>`.

:original_name: ListProviders.html

.. _ListProviders:

Querying Services Supported by TMS
==================================

Function
--------

You can use this API to query services supported by TMS.

URI
---

GET /v1.0/tms/providers

.. table:: **Table 1** Query parameters

   +-----------+-----------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter | Mandatory | Type    | Description                                                                                                                                                                  |
   +===========+===========+=========+==============================================================================================================================================================================+
   | locale    | No        | String  | Specifies the display language.                                                                                                                                              |
   +-----------+-----------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | limit     | No        | Integer | The maximum queries supported. The value 10 is used by default if this parameter is not set. The value range is 1 to 200.                                                    |
   +-----------+-----------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | offset    | No        | Integer | Specifies the index position, which starts from the next data record specified by **offset**. The value must be a number and cannot be negative. The default value is **0**. |
   +-----------+-----------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | provider  | No        | String  | Specifies the cloud service name.                                                                                                                                            |
   +-----------+-----------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request
-------

.. table:: **Table 2** Header parameters

   +--------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter    | Mandatory | Type   | Description                                                                                                                                                                                                              |
   +==============+===========+========+==========================================================================================================================================================================================================================+
   | X-Auth-Token | Yes       | String | Specifies the user token. TMS is a global service. So you need to set **scope** to **domain** when calling an IAM API to obtain a user token. The value of **X-Subject-Token** in the response header is the user token. |
   +--------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Response
--------

**Status code: 200**

.. table:: **Table 3** Body parameters

   +-------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
   | Parameter   | Type                                                                                                                                                  | Description                                   |
   +=============+=======================================================================================================================================================+===============================================+
   | providers   | Array of :ref:`ProviderResponseBody <listproviders__en-us_topic_0000001470343266_en-us_topic_0000001471116345_response_providerresponsebody>` objects | Specifies the cloud services                  |
   +-------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
   | total_count | Integer                                                                                                                                               | Specifies the total cloud services supported. |
   +-------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+

.. _listproviders__en-us_topic_0000001470343266_en-us_topic_0000001471116345_response_providerresponsebody:

.. table:: **Table 4** ProviderResponseBody

   +----------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------+
   | Parameter                  | Type                                                                                                                                          | Description                                                                                                 |
   +============================+===============================================================================================================================================+=============================================================================================================+
   | provider                   | String                                                                                                                                        | Specifies the cloud service name.                                                                           |
   +----------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------+
   | provider_i18n_display_name | String                                                                                                                                        | Specifies the display name of the resource. You can set the language by setting the \**locale*\* parameter. |
   +----------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------+
   | resource_types             | Array of :ref:`ResourceTypeBody <listproviders__en-us_topic_0000001470343266_en-us_topic_0000001471116345_response_resourcetypebody>` objects | Specifies the resource type.                                                                                |
   +----------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------+

.. _listproviders__en-us_topic_0000001470343266_en-us_topic_0000001471116345_response_resourcetypebody:

.. table:: **Table 5** ResourceTypeBody

   +---------------------------------+------------------+------------------------------------------------------------------------------------------------------------------+
   | Parameter                       | Type             | Description                                                                                                      |
   +=================================+==================+==================================================================================================================+
   | resource_type                   | String           | Specifies the resource type.                                                                                     |
   +---------------------------------+------------------+------------------------------------------------------------------------------------------------------------------+
   | resource_type_i18n_display_name | String           | Specifies the display name of the resource type. You can set the language by setting the \**locale*\* parameter. |
   +---------------------------------+------------------+------------------------------------------------------------------------------------------------------------------+
   | regions                         | Array of strings | Specifies the supported regions.                                                                                 |
   +---------------------------------+------------------+------------------------------------------------------------------------------------------------------------------+
   | global                          | Boolean          | Specifies whether the resource is a global resource.                                                             |
   +---------------------------------+------------------+------------------------------------------------------------------------------------------------------------------+

Example Request
---------------

Querying supported services by TMS

.. code-block:: text

   GET https://{Endpoint}/v1.0/tms/providers?locale=en-us&limit=200

Example Response
----------------

**Status code: 200**

Successful operation

.. code-block::

   {
       "providers": [
           {
               "provider": "drs",
               "provider_i18n_display_name": "drs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "sync",
                       "resource_type_i18n_display_name": "sync",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "cloudDataGuard",
                       "resource_type_i18n_display_name": "cloudDataGuard",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "subscription",
                       "resource_type_i18n_display_name": "subscription",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "backupMigration",
                       "resource_type_i18n_display_name": "backupMigration",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "migration",
                       "resource_type_i18n_display_name": "migration",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "dli",
               "provider_i18n_display_name": "dli",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "dli_basic_datasource",
                       "resource_type_i18n_display_name": "dli_basic_datasource",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "dli_queue",
                       "resource_type_i18n_display_name": "dli_queue",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "gaussdb",
               "provider_i18n_display_name": "gaussdb",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "gaussdb",
                       "resource_type_i18n_display_name": "gaussdb",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "er",
               "provider_i18n_display_name": "er",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "instance",
                       "resource_type_i18n_display_name": "instance",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "nosql",
               "provider_i18n_display_name": "GaussDBNoSQL",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "nosql",
                       "resource_type_i18n_display_name": "nosql",
                       "regions": [
                           "cn-north-7",
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "as",
               "provider_i18n_display_name": "AS",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "scaling_group",
                       "resource_type_i18n_display_name": "AS",
                       "regions": [
                           "ru-northwest-2"
                       ]
                   }
               ]
           },
           {
               "provider": "ecs",
               "provider_i18n_display_name": "ecs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "ecs",
                       "resource_type_i18n_display_name": "ECS",
                       "regions": [
                           "ru-northwest-2",
                           "eu-de",
                           "eu-nl"
                       ]
                   }
               ]
           },
           {
               "provider": "vpc",
               "provider_i18n_display_name": "vpc",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "subnet",
                       "resource_type_i18n_display_name": "subnet",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "eip",
                       "resource_type_i18n_display_name": "eip",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "vpc",
                       "resource_type_i18n_display_name": "vpc",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "loadbalancers",
                       "resource_type_i18n_display_name": "loadbalancers",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "listeners",
                       "resource_type_i18n_display_name": "listeners",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "ipsec-site-connections",
                       "resource_type_i18n_display_name": "ipsec-site-connections",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "nat_gateways",
                       "resource_type_i18n_display_name": "nat_gateways",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "DBSS",
               "provider_i18n_display_name": "Database Security Service",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "auditInstance",
                       "resource_type_i18n_display_name": "Database Security Service",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "FunctionGraph",
               "provider_i18n_display_name": "FunctionGraph",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "functions",
                       "resource_type_i18n_display_name": "functions",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "dms",
               "provider_i18n_display_name": "dms",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "kafka",
                       "resource_type_i18n_display_name": "kafka",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "dcs",
               "provider_i18n_display_name": "dcs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "dcs",
                       "resource_type_i18n_display_name": "dcs",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "css",
               "provider_i18n_display_name": "css",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "css-cluster",
                       "resource_type_i18n_display_name": "css-cluster",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "cce",
               "provider_i18n_display_name": "cce",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "cce-cluster",
                       "resource_type_i18n_display_name": "cce-cluster",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "ims",
               "provider_i18n_display_name": "ims",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "private_image",
                       "resource_type_i18n_display_name": "private_image",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "vbs",
               "provider_i18n_display_name": "vbs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "backup",
                       "resource_type_i18n_display_name": "backup",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "autoback",
               "provider_i18n_display_name": "autoback",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "backup_policy",
                       "resource_type_i18n_display_name": "backup_policy",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "rds",
               "provider_i18n_display_name": "rds",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "rds",
                       "resource_type_i18n_display_name": "rds",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "csbs",
               "provider_i18n_display_name": "csbs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "vault",
                       "resource_type_i18n_display_name": "vault",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "csbs_backup",
                       "resource_type_i18n_display_name": "csbs_backup",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": false,
                       "resource_type": "csbs_backup_policy",
                       "resource_type_i18n_display_name": "csbs_backup_policy",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "dns",
               "provider_i18n_display_name": "dns",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "DNS_ptr_record",
                       "resource_type_i18n_display_name": "DNS_ptr_record",
                       "regions": [
                           "eu-de"
                       ]
                   },
                   {
                       "global": true,
                       "resource_type": "DNS_private_zone",
                       "resource_type_i18n_display_name": "DNS_private_zone",
                       "regions": [
                           "eu-de",
                           "eu-nl"
                       ]
                   },
                   {
                       "global": true,
                       "resource_type": "DNS_private_recordset",
                       "resource_type_i18n_display_name": "DNS_private_recordset",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "evs",
               "provider_i18n_display_name": "evs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "disk",
                       "resource_type_i18n_display_name": "disk",
                       "regions": [
                           "",
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "kms",
               "provider_i18n_display_name": "kms",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "kms",
                       "resource_type_i18n_display_name": "kms",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "smn",
               "provider_i18n_display_name": "smn",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "smn_topic",
                       "resource_type_i18n_display_name": "smn_topic",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "dws",
               "provider_i18n_display_name": "dws",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "dws_clusters",
                       "resource_type_i18n_display_name": "dws_clusters",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "bms",
               "provider_i18n_display_name": "bms",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "bms_server",
                       "resource_type_i18n_display_name": "bms_server",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "deh",
               "provider_i18n_display_name": "deh",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "dedicated-host-tags",
                       "resource_type_i18n_display_name": "dedicated-host-tags",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "waf",
               "provider_i18n_display_name": "waf",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "waf",
                       "resource_type_i18n_display_name": "waf",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "sfs",
               "provider_i18n_display_name": "sfs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "sfs",
                       "resource_type_i18n_display_name": "sfs",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "obs",
               "provider_i18n_display_name": "obs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "bucket",
                       "resource_type_i18n_display_name": "bucket",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "sdrs",
               "provider_i18n_display_name": "sdrs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "sdrs",
                       "resource_type_i18n_display_name": "sdrs",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "dds",
               "provider_i18n_display_name": "dds",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "dds",
                       "resource_type_i18n_display_name": "dds",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           },
           {
               "provider": "mrs",
               "provider_i18n_display_name": "mrs",
               "resource_types": [
                   {
                       "global": false,
                       "resource_type": "clusters",
                       "resource_type_i18n_display_name": "clusters",
                       "regions": [
                           "eu-de"
                       ]
                   }
               ]
           }
       ],
       "total_count": 32
   }

Status Codes
------------

See :ref:`Status Codes <en-us_topic_0130578970>`.

Error Codes
-----------

See :ref:`Error Codes <en-us_topic_0057939857>`.

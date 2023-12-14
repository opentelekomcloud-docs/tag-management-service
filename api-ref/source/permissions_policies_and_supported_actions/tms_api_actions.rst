:original_name: en-us_topic_0180205869.html

.. _en-us_topic_0180205869:

TMS API Actions
===============

.. table:: **Table 1** API actions

   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Permission                  | API                                    | Action                                    | IAM Project   | Enterprise Project |
   +=============================+========================================+===========================================+===============+====================+
   | Querying predefined tags    | GET /v1.0/predefine_tags               | tms:predefineTags:list                    | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Creating predefined tags    | POST /v1.0/predefine_tags/action       | tms:predefineTags:create                  | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Deleting predefined tags    | POST /v1.0/predefine_tags/action       | tms:predefineTags:delete                  | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Modifying a predefined tag  | PUT /v1.0/predefine_tags               | tms:predefineTags:update                  | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Batch creating tags         | POST /v1.0/resource-tags/batch-create  | tms:resourceTags:create                   | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Batch deleting tags         | POST /v1.0/resource-tags/batch-delete  | tms:resourceTags:delete                   | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Querying tag Keys           | GET /v1.0/tag-keys                     | tms:tagKeys:list                          | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Querying tag values         | GET /v1.0/tag-values                   | tms:tagValues:list                        | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Querying resource tags      | GET /v2.0/resources/{resource_id}/tags | tms:resourceTags:list                     | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Querying resources by tag   | POST /v1.0/resource-instances/filter   | tms:resources:list                        | Supported     | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Querying tag quotas         | GET /v1.0/tms/quotas                   | Included in the Tenant Guest permissions. | Not supported | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+
   | Querying supported services | GET /v1.0/tms/providers                | Included in the Tenant Guest permissions. | Not supported | Not supported      |
   +-----------------------------+----------------------------------------+-------------------------------------------+---------------+--------------------+

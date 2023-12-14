:original_name: en-us_topic_0180205869.html

.. _en-us_topic_0180205869:

TMS API Actions
===============

.. table:: **Table 1** API actions

   +----------------------------+----------------------------------+--------------------------+-------------+--------------------+
   | Permission                 | API                              | Action                   | IAM Project | Enterprise Project |
   +============================+==================================+==========================+=============+====================+
   | Querying predefined tags   | GET /v1.0/predefine_tags         | tms:predefineTags:list   | Supported   | Not supported      |
   +----------------------------+----------------------------------+--------------------------+-------------+--------------------+
   | Creating predefined tags   | POST /v1.0/predefine_tags/action | tms:predefineTags:create | Supported   | Not supported      |
   +----------------------------+----------------------------------+--------------------------+-------------+--------------------+
   | Deleting predefined tags   | POST /v1.0/predefine_tags/action | tms:predefineTags:delete | Supported   | Not supported      |
   +----------------------------+----------------------------------+--------------------------+-------------+--------------------+
   | Modifying a predefined tag | PUT /v1.0/predefine_tags/action  | tms:predefineTags:update | Supported   | Not supported      |
   +----------------------------+----------------------------------+--------------------------+-------------+--------------------+

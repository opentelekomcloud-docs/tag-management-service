:original_name: GetResourceTag.html

.. _GetResourceTag:

Querying Resource Tags
======================

Function
--------

You can use this API to query tags of a specific resource.

URI
---

GET /v2.0/resources/{resource_id}/tags

.. table:: **Table 1** Parameter description

   =========== ========= ====== ==========================
   Parameter   Mandatory Type   Description
   =========== ========= ====== ==========================
   resource_id Yes       String Specifies the resource ID.
   =========== ========= ====== ==========================

.. table:: **Table 2** Query parameters

   +---------------+-----------+--------+-----------------------------------------------------------------------------------+
   | Parameter     | Mandatory | Type   | Description                                                                       |
   +===============+===========+========+===================================================================================+
   | project_id    | No        | String | Specifies the project ID. This parameter is mandatory for region-level resources. |
   +---------------+-----------+--------+-----------------------------------------------------------------------------------+
   | resource_type | Yes       | String | Specifies the resource type.                                                      |
   +---------------+-----------+--------+-----------------------------------------------------------------------------------+

Request
-------

.. table:: **Table 3** Header parameters

   +--------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter    | Mandatory | Type   | Description                                                                                                                                                                                                              |
   +==============+===========+========+==========================================================================================================================================================================================================================+
   | X-Auth-Token | Yes       | String | Specifies the user token. TMS is a global service. So you need to set **scope** to **domain** when calling an IAM API to obtain a user token. The value of **X-Subject-Token** in the response header is the user token. |
   +--------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Response
--------

**Status code: 200**

.. table:: **Table 4** Body parameters

   +-----------+--------------------------------------------------------------------------------------------------------------------------+--------------------------+
   | Parameter | Type                                                                                                                     | Description              |
   +===========+==========================================================================================================================+==========================+
   | tags      | Array of :ref:`TagVo <getresourcetag__en-us_topic_0000001470502906_en-us_topic_0000001420559672_response_tagvo>` objects | Specifies resource tags. |
   +-----------+--------------------------------------------------------------------------------------------------------------------------+--------------------------+

.. _getresourcetag__en-us_topic_0000001470502906_en-us_topic_0000001420559672_response_tagvo:

.. table:: **Table 5** TagVo

   +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                                                                                                                          |
   +=======================+=======================+======================================================================================================================================================================+
   | key                   | String                | Specifies the key.                                                                                                                                                   |
   |                       |                       |                                                                                                                                                                      |
   |                       |                       | It cannot be left blank and can contain a maximum of 36 Unicode characters. Only digits, letters, hyphens (-), at signs (@), and underscores (_) are allowed.        |
   +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | value                 | String                | Specifies the value.                                                                                                                                                 |
   |                       |                       |                                                                                                                                                                      |
   |                       |                       | Each value contains a maximum of 43 Unicode characters and can be an empty string. Only digits, letters, hyphens (-), at signs (@), and underscores (_) are allowed. |
   +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Example Request
---------------

Querying tags of a resource

.. code-block:: text

   GET https://{Endpoint}/v2.0/resources/xxxx/tags?project_id=xxxx&resource_type=disk

Example Response
----------------

**Status code: 200**

Successful operation

.. code-block::

   {
     "tags" : [ {
       "key" : "key1",
       "value" : "value1"
     }, {
       "key" : "key2",
       "value" : "value2"
     } ]
   }

Status Codes
------------

See :ref:`Status Codes <en-us_topic_0130578970>`.

Error Codes
-----------

See :ref:`Error Codes <en-us_topic_0057939857>`.

:original_name: CreateResourceTag.html

.. _CreateResourceTag:

Batch Adding Tags
=================

Function
--------

You can use this API to add tags to multiple resources. Up to 10 tags can be added to a resource and a maximum of 50 resources can be tagged at a time.

URI
---

POST /v1.0/resource-tags/batch-create

Request
-------

.. table:: **Table 1** Header parameters

   +--------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter    | Mandatory | Type   | Description                                                                                                                                                                                                              |
   +==============+===========+========+==========================================================================================================================================================================================================================+
   | X-Auth-Token | Yes       | String | Specifies the user token. TMS is a global service. So you need to set **scope** to **domain** when calling an IAM API to obtain a user token. The value of **X-Subject-Token** in the response header is the user token. |
   +--------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. table:: **Table 2** Body parameters

   +------------+-----------+--------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------+
   | Parameter  | Mandatory | Type                                                                                                                                             | Description                                                                                        |
   +============+===========+==================================================================================================================================================+====================================================================================================+
   | project_id | No        | String                                                                                                                                           | Specifies the project ID. This parameter is mandatory when **resource_type** is at a region level. |
   +------------+-----------+--------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------+
   | resources  | Yes       | Array of :ref:`ResourceTagBody <createresourcetag__en-us_topic_0000001470662542_en-us_topic_0000001470836057_request_resourcetagbody>` objects   | Specifies resources.                                                                               |
   +------------+-----------+--------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------+
   | tags       | Yes       | Array of :ref:`CreateTagRequest <createresourcetag__en-us_topic_0000001470662542_en-us_topic_0000001470836057_request_createtagrequest>` objects | Specifies tags.                                                                                    |
   +------------+-----------+--------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------+

.. _createresourcetag__en-us_topic_0000001470662542_en-us_topic_0000001470836057_request_resourcetagbody:

.. table:: **Table 3** ResourceTagBody

   ============= ========= ====== ============================
   Parameter     Mandatory Type   Description
   ============= ========= ====== ============================
   resource_id   Yes       String Specifies the resource ID.
   resource_type Yes       String Specifies the resource type.
   ============= ========= ====== ============================

.. _createresourcetag__en-us_topic_0000001470662542_en-us_topic_0000001470836057_request_createtagrequest:

.. table:: **Table 4** CreateTagRequest

   +-----------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                                                                                                                                          |
   +=================+=================+=================+======================================================================================================================================================================+
   | key             | Yes             | String          | Specifies the key.                                                                                                                                                   |
   |                 |                 |                 |                                                                                                                                                                      |
   |                 |                 |                 | It can contain up to 36 characters. The key cannot be empty. Only digits, letters, hyphens (-), at signs (@), and underscores (_) are allowed.                       |
   +-----------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | value           | Yes             | String          | Specifies the value.                                                                                                                                                 |
   |                 |                 |                 |                                                                                                                                                                      |
   |                 |                 |                 | Each value contains a maximum of 43 Unicode characters and can be an empty string. Only digits, letters, hyphens (-), at signs (@), and underscores (_) are allowed. |
   +-----------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Response
--------

**Status code: 200**

.. table:: **Table 5** Body parameters

   +------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------+
   | Parameter        | Type                                                                                                                                                        | Description                                          |
   +==================+=============================================================================================================================================================+======================================================+
   | failed_resources | Array of :ref:`TagCreateResponseItem <createresourcetag__en-us_topic_0000001470662542_en-us_topic_0000001470836057_response_tagcreateresponseitem>` objects | Specifies resources for which tags fail to be added. |
   +------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------+

.. _createresourcetag__en-us_topic_0000001470662542_en-us_topic_0000001470836057_response_tagcreateresponseitem:

.. table:: **Table 6** TagCreateResponseItem

   ============= ====== ============================
   Parameter     Type   Description
   ============= ====== ============================
   resource_id   String Specifies the resource ID.
   resource_type String Specifies the resource type.
   error_code    String Error Codes
   error_msg     String Specifies the error.
   ============= ====== ============================

Example Request
---------------

You can use this API to batch tag resources.

.. code-block:: text

   POST https://{Endpoint}/v1.0/resource-tags/batch-create

   {
     "project_id" : "xxxdcffffffff",
     "resources" : [ {
       "resource_id" : "a28531fa-a8d5-468e-8417-86a80962ee5e",
       "resource_type" : "disk"
     }, {
       "resource_id" : "a28531fa-a8d5-468e-8417-86a8096ddddd",
       "resource_type" : "vpc"
     } ],
     "tags" : [ {
       "key" : "ENV",
       "value" : "dev"
     }, {
       "key" : "DEPT",
       "value" : "pdd"
     } ]
   }

Example Response
----------------

**Status code: 200**

Successful operation

.. code-block::

   {
     "failed_resources": []
   }

Status Codes
------------

See :ref:`Status Codes <en-us_topic_0130578970>`.

Error Codes
-----------

See :ref:`Error Codes <en-us_topic_0057939857>`.

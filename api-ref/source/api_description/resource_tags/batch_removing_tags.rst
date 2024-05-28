:original_name: DeleteResourceTag.html

.. _DeleteResourceTag:

Batch Removing Tags
===================

Function
--------

You can use this API to remove tags from multiple resources. Up to 10 tags can be removed from a resource and a maximum of 50 resources can be operated at a time.

URI
---

POST /v1.0/resource-tags/batch-delete

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
   | resources  | Yes       | Array of :ref:`ResourceTagBody <deleteresourcetag__en-us_topic_0000001470822378_en-us_topic_0000001421036544_request_resourcetagbody>` objects   | Specifies resource list                                                                            |
   +------------+-----------+--------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------+
   | tags       | Yes       | Array of :ref:`DeleteTagRequest <deleteresourcetag__en-us_topic_0000001470822378_en-us_topic_0000001421036544_request_deletetagrequest>` objects | Specifies tags.                                                                                    |
   +------------+-----------+--------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------+

.. _deleteresourcetag__en-us_topic_0000001470822378_en-us_topic_0000001421036544_request_resourcetagbody:

.. table:: **Table 3** ResourceTagBody

   ============= ========= ====== ============================
   Parameter     Mandatory Type   Description
   ============= ========= ====== ============================
   resource_id   Yes       String Specifies the resource ID.
   resource_type Yes       String Specifies the resource type.
   ============= ========= ====== ============================

.. _deleteresourcetag__en-us_topic_0000001470822378_en-us_topic_0000001421036544_request_deletetagrequest:

.. table:: **Table 4** DeleteTagRequest

   +-----------------+-----------------+-----------------+------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                                                                                                                    |
   +=================+=================+=================+================================================================================================================================================+
   | key             | Yes             | String          | Specifies the key.                                                                                                                             |
   |                 |                 |                 |                                                                                                                                                |
   |                 |                 |                 | It can contain up to 36 characters. The key cannot be empty. Only digits, letters, hyphens (-), at signs (@), and underscores (_) are allowed. |
   +-----------------+-----------------+-----------------+------------------------------------------------------------------------------------------------------------------------------------------------+

Response
--------

**Status code: 200**

.. table:: **Table 5** Body parameters

   +------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------+
   | Parameter        | Type                                                                                                                                                        | Description                                                  |
   +==================+=============================================================================================================================================================+==============================================================+
   | failed_resources | Array of :ref:`TagDeleteResponseItem <deleteresourcetag__en-us_topic_0000001470822378_en-us_topic_0000001421036544_response_tagdeleteresponseitem>` objects | Specifies resources for which tags are failed to be deleted. |
   +------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------+

.. _deleteresourcetag__en-us_topic_0000001470822378_en-us_topic_0000001421036544_response_tagdeleteresponseitem:

.. table:: **Table 6** TagDeleteResponseItem

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

Batch delete tags

.. code-block:: text

   POST https://{Endpoint}/v1.0/resource-tags/batch-delete

   {
     "project_id" : "xxxdcffffffff",
     "resources" : [ {
       "resource_id" : "a28531fa-a8d5-468e-8417-86a80962ee5e",
       "resource_type" : "disk"
     }, {
       "resource_id" : "vpc-dc7d19b7",
       "resource_type" : "vpc"
     } ],
     "tags" : [ {
       "key" : "ENV"
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

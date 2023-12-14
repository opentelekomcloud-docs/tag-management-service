:original_name: ShowTagQuota.html

.. _ShowTagQuota:

Querying Tag Quotas
===================

Function
--------

This API is used to query tag quotas.

URI
---

GET /v1.0/tms/quotas

Request
-------

.. table:: **Table 1** Header

   +--------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter    | Mandatory | Type   | Description                                                                                                                                                                                                              |
   +==============+===========+========+==========================================================================================================================================================================================================================+
   | X-Auth-Token | Yes       | String | Specifies the user token. TMS is a global service. So you need to set **scope** to **domain** when calling an IAM API to obtain a user token. The value of **X-Subject-Token** in the response header is the user token. |
   +--------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Response
--------

**Status code: 200**

.. table:: **Table 2** Body

   +-----------+------------------------------------------------------------------------------------------------------------------------------+-------------+
   | Parameter | Type                                                                                                                         | Description |
   +===========+==============================================================================================================================+=============+
   | quotas    | Array of :ref:`TagQuota <showtagquota__en-us_topic_0000001521222041_en-us_topic_0000001338904437_response_tagquota>` objects | Quota lists |
   +-----------+------------------------------------------------------------------------------------------------------------------------------+-------------+

.. _showtagquota__en-us_topic_0000001521222041_en-us_topic_0000001338904437_response_tagquota:

.. table:: **Table 3** TagQuota

   =========== ======= ==========================
   Parameter   Type    Description
   =========== ======= ==========================
   quota_key   String  Specifies the quota key.
   quota_limit Integer Specifies the quota value.
   used        Integer Specifies the used quota.
   unit        String  Specifies the unit.
   =========== ======= ==========================

Example Request
---------------

Querying tag quotas

.. code-block:: text

   GET https://{Endpoint}/v1.0/tms/quotas

Example Response
----------------

**Status code: 200**

Successful operation

.. code-block::

   {
     "quotas" : [ {
       "used" : 4,
       "unit" : "count",
       "quota_key" : "predefine_tag",
       "quota_limit" : 500
     } ]
   }

Status Codes
------------

See :ref:`Status Codes <en-us_topic_0130578970>`.

Error Codes
-----------

See :ref:`Error Codes <en-us_topic_0057939857>`.

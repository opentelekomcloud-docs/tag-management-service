:original_name: en-us_topic_0056765935.html

.. _en-us_topic_0056765935:

Creating or Deleting Predefined Tags
====================================

Function
--------

This API is used to create or delete predefined tags. You can add tags to resources using the predefined tags.

This API supports idempotency and batch processing.

.. note::

   Idempotent operations refer to invoking the same API for multiple times by using the same parameters, which have the same impact on the system.

URI
---

POST /v1.0/predefine_tags/action

Request
-------

-  Parameter description

   .. table:: **Table 1** Request header parameters

      +--------------+-----------+--------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter    | Mandatory | Type   | Description                                                                                                                                                                                                 |
      +==============+===========+========+=============================================================================================================================================================================================================+
      | X-Auth-Token | Yes       | String | Specifies the user token. TMS is a global service. When calling the IAM API to obtain a user token, set **scope** to **domain**. The value of **X-Subject-Token** in the response header is the user token. |
      +--------------+-----------+--------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

   .. table:: **Table 2** Parameters

      +-----------------+-----------------+------------------+-------------------------------------------------------------------------------------------------+
      | Name            | Mandatory       | Type             | Description                                                                                     |
      +=================+=================+==================+=================================================================================================+
      | action          | Yes             | String           | Specifies the action identifier.                                                                |
      |                 |                 |                  |                                                                                                 |
      |                 |                 |                  | The value is case sensitive and can be **create** or **delete**.                                |
      +-----------------+-----------------+------------------+-------------------------------------------------------------------------------------------------+
      | tags            | Yes             | Array of objects | Specifies the tags. One to fifty tags are specified.                                            |
      |                 |                 |                  |                                                                                                 |
      |                 |                 |                  | For details, see :ref:`Table 3 <en-us_topic_0056765935__en-us_topic_0056765542_table46817064>`. |
      +-----------------+-----------------+------------------+-------------------------------------------------------------------------------------------------+

-  **tags** field description

   .. _en-us_topic_0056765935__en-us_topic_0056765542_table46817064:

   .. table:: **Table 3** Fields

      +-----------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Name            | Mandatory       | Type            | Description                                                                                                                                                          |
      +=================+=================+=================+======================================================================================================================================================================+
      | key             | Yes             | String          | Specifies the key.                                                                                                                                                   |
      |                 |                 |                 |                                                                                                                                                                      |
      |                 |                 |                 | It can contain up to 36 characters. The key cannot be empty. Only digits, letters, hyphens (-), at signs (@), and underscores (_) are allowed.                       |
      +-----------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | value           | Yes             | String          | Specifies the value.                                                                                                                                                 |
      |                 |                 |                 |                                                                                                                                                                      |
      |                 |                 |                 | Each value contains a maximum of 43 Unicode characters and can be an empty string. Only digits, letters, hyphens (-), at signs (@), and underscores (_) are allowed. |
      +-----------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+

-  Example request

   .. code-block:: text

      POST https://{TMS endpoint}/v1.0/predefine_tags/action

   .. code-block::

      {
          "action": "create",
          "tags": [
              {
                  "key": "ENV1",
                  "value": "DEV1"
              },
              {
                  "key": "ENV2",
                  "value": "DEV2"
              }
          ]
      }

Example Response
----------------

**Status code: 204**

Status Codes
------------

See :ref:`Status Codes <en-us_topic_0130578970>`.

Error Codes
-----------

See :ref:`Error Codes <en-us_topic_0057939857>`.

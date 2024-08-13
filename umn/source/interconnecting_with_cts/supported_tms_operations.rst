:original_name: en-us_topic_0110866979.html

.. _en-us_topic_0110866979:

Supported TMS Operations
========================

Scenario
--------

With Cloud Trace Service (CTS), you can record operations associated with TMS for later query, audit, and backtrack operations.

Prerequisites
-------------

You have enabled CTS.


Supported TMS Operations
------------------------

.. table:: **Table 1** TMS operations supported by CTS

   +--------------------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Operation                                                                                                    | Resource Type         | Trace Name              |
   +==============================================================================================================+=======================+=========================+
   | Creating Predefined Tags                                                                                     | predefineTag          | addPredefineTag         |
   +--------------------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Deleting Predefined Tags                                                                                     | predefineTag          | deletePredefineTag      |
   +--------------------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Creating Resource Tags                                                                                       | application           | createResourceTag       |
   +--------------------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Deleting Resource Tags                                                                                       | application           | deleteResourceTag       |
   +--------------------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Batch Removing Tags                                                                                          | resourceTag           | batchDeleteResourceTags |
   |                                                                                                              |                       |                         |
   | .. note::                                                                                                    |                       |                         |
   |                                                                                                              |                       |                         |
   |    You can perform this operation by calling an API. Currently, TMS console does not support this operation. |                       |                         |
   +--------------------------------------------------------------------------------------------------------------+-----------------------+-------------------------+

Querying Traces
---------------

See `Querying Real-Time Traces <https://docs.otc.t-systems.com/cloud-trace-service/umn/getting_started/querying_real-time_traces.html>`__.

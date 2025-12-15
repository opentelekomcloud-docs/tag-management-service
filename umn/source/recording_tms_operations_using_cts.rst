:original_name: tms_06_0002.html

.. _tms_06_0002:

Recording TMS Operations Using CTS
==================================

Scenario
--------

Cloud Trace Service (CTS) records operations on TMS for your later query, audit, and backtrack.

Prerequisites
-------------

You have enabled CTS.

Supported TMS Operations
------------------------

.. table:: **Table 1** TMS operations supported by CTS

   +-----------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Operation                                                                                           | Resource Type         | Trace Name              |
   +=====================================================================================================+=======================+=========================+
   | Creating predefined tags                                                                            | predefineTag          | addPredefineTag         |
   +-----------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Deleting predefined tags                                                                            | predefineTag          | deletePredefineTag      |
   +-----------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Creating resource tags                                                                              | application           | createResourceTag       |
   +-----------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Deleting resource tags                                                                              | application           | deleteResourceTag       |
   +-----------------------------------------------------------------------------------------------------+-----------------------+-------------------------+
   | Batch removing tags                                                                                 | resourceTag           | batchDeleteResourceTags |
   |                                                                                                     |                       |                         |
   | .. note::                                                                                           |                       |                         |
   |                                                                                                     |                       |                         |
   |    You can only call an API to perform this operation. TMS console does not support this operation. |                       |                         |
   +-----------------------------------------------------------------------------------------------------+-----------------------+-------------------------+

Querying Traces
---------------

See `Querying Real-Time Traces <https://docs.otc.t-systems.com/cloud-trace-service/umn/getting_started/querying_real-time_traces.html>`__.

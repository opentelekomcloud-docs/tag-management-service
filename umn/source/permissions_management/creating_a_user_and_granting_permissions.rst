:original_name: tms_04_0002.html

.. _tms_04_0002:

Creating a User and Granting Permissions
========================================

This section describes how to use `IAM <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0026.html>`__ to implement fine-grained permissions control for your DMS resources. With IAM, you can:

-  Create IAM users or user groups for personnel based on your enterprise's organizational structure. Each IAM user has their own identity credentials for accessing TMS resources.
-  Grant users only the permissions required to perform a given task based on their job responsibilities.
-  Entrust an account or a cloud service to perform efficient O&M on your TMS resources.

If your account meets your permissions requirements, you can skip this section.

:ref:`Figure 1 <tms_04_0002__fig33941114133916>` shows the process flow for granting permissions.

.. note::

   If users do not have the **TMS Administrator** permissions, the following situations occur:

   -  Users cannot access the TMS console.
   -  On consoles of other cloud services, users cannot view or use predefined tags created on the TMS console.

Prerequisites
-------------

Before granting permissions, learn about the TMS permissions and select the permissions as required. For details about the system-defined permissions in RBAC supported by TMS, see :ref:`TMS Permissions <tms_01_0009__section1814075113611>`. To grant permissions for other services, learn about all `permissions <https://docs.otc.t-systems.com/permissions/index.html>`__.

Process Flow
------------

.. _tms_04_0002__fig33941114133916:

.. figure:: /_static/images/en-us_image_0281161475.jpg
   :alt: **Figure 1** Process for granting TMS permissions

   **Figure 1** Process for granting TMS permissions

#. `create a user group and grant it permissions <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0030.html>`__ (TMS Administrator as an example).

#. `Create an IAM user and add it to the created user group <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0031.html>`__.

#. `Log in <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0032.html>`__ and verify permissions.

   Log in to the TMS console as the created user, and verify that it only has the **TMS Administrator** permissions.

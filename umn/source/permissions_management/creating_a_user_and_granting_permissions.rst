:original_name: tms_04_0002.html

.. _tms_04_0002:

Creating a User and Granting Permissions
========================================

This section describes how to use `IAM <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0026.html>`__ to implement fine-grained permissions control for your TMS resources. With IAM, you can:

-  Create IAM users for employees based on your organizational structure. Each IAM user has their own security credentials for accessing TMS resources.
-  Grant users only the permissions required to perform a given task based on their job responsibilities.
-  Entrust an account or a cloud service to perform operations for your TMS resources.

If your account does not need individual IAM users, skip this section.

:ref:`Figure 1 <tms_04_0002__fig890010150810>` shows the process flow for granting permissions.

Prerequisites
-------------

Before granting permissions, learn about the TMS permissions and select the permissions as required. For details about the system-defined permissions supported by TMS, see :ref:`TMS Permissions <tms_01_0009__section1814075113611>`. To grant permissions for other services, you can see `permissions <https://docs.otc.t-systems.com/identity-access-management/permissions/permissions.html>`__.

Flowchart
---------

.. _tms_04_0002__fig890010150810:

.. figure:: /_static/images/en-us_image_0000001700714200.png
   :alt: **Figure 1** Granting TMS permissions

   **Figure 1** Granting TMS permissions

#. On the IAM console, `create a user group and assigning permissions <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0030.html>`__. Here, TMS ReadOnlyAccess permissions are used as an example.

#. `Create an IAM user and add it to the created user group <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0031.html>`__.

#. `Log in <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0032.html>`__ and verify permissions.

   The created user logs in to the console and verifies permissions as described below:

   -  Choose **Service List** > **Tag Management Service**. In the navigation pane on the left, click **Predefined Tags**. In the upper right corner of the displayed page, click **Create Tag**. If a message appears indicating that you have insufficient permissions to perform the operation, and if you can view existing predefined tags in the **Predefined Tags** page, the **TMS ReadOnlyAccess** policy is in effect.
   -  Choose another service from **Service List**. If a message appears indicating that you have insufficient permissions to access the service, the **TMS ReadOnlyAccess** policy is in effect.

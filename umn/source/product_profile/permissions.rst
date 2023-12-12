:original_name: tms_01_0009.html

.. _tms_01_0009:

Permissions
===========

If you need to assign different permissions to personnel in your enterprise to access your cloud resources, Identity and Access Management (IAM) is a good choice for fine-grained permissions management. IAM provides identity authentication, permissions management, and access control, helping you securely access your cloud resources.

With IAM, you can use your account to create IAM users for your employees, and assign permissions to the users to control their access to specific resource types. For example, if you want some software developers in your enterprise to use TMS resources but do not want them to delete the resources or perform any other high-risk operations, you can grant permission to use the resources but not permission to delete them.

If your account does not require IAM for permissions management, you can skip this section.

IAM is a free service. You only pay for the resources in your account. For more information about IAM, see `IAM Service Overview <https://docs.otc.t-systems.com/identity-access-management/umn/service_overview/what_is_iam.html>`__.

.. _tms_01_0009__section1814075113611:

TMS Permissions
---------------

New IAM users do not have any permissions assigned by default. You need to first add them to one or more groups and attach policies or roles to these groups. The users then inherit permissions from the groups and can perform specified operations on cloud services based on the permissions they have been assigned.

TMS is a global service deployed for all regions. When you set the authorization scope to **Global services**, users have permission to access TMS resources in all regions.

:ref:`Table 1 <tms_01_0009__table18049733717>` lists all the system-defined policies for TMS. Some TMS policies dependent on the policies of other services to take effect. When you assign TMS permissions to users, you also assign dependent policies for the TMS permissions to take effect.

.. _tms_01_0009__table18049733717:

.. table:: **Table 1** System-defined policies for TMS

   +-----------------------+----------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
   | Policy Name           | Description                                                                | Dependencies                                                                                                                             |
   +=======================+============================================================================+==========================================================================================================================================+
   | TMS Administrator     | Users with this permission can create, modify, and delete predefined tags. | Dependent on the following policies:                                                                                                     |
   |                       |                                                                            |                                                                                                                                          |
   |                       |                                                                            | -  **Tenant Guest**: a global or project-level policy, which must be assigned in the Global project                                      |
   |                       |                                                                            | -  **Server Administrator**: a project-level policy, which must be assigned in the same project as the **TMS Administrator** policy      |
   |                       |                                                                            | -  **Tenant Guest**: a global policy. Select **Global service project** for **Scope**.                                                   |
   |                       |                                                                            | -  **Tenant Administrator**: a global policy. Select **Global service project** for **Scope**.                                           |
   |                       |                                                                            | -  **IMS Administrator**: a project-level policy, which must be assigned in the same project as the **TMS Administrator** policy         |
   |                       |                                                                            | -  **AutoScaling Administrator**: a project-level policy, which must be assigned in the same project as the **TMS Administrator** policy |
   |                       |                                                                            | -  **VPC Administrator**: a project-level policy, which must be assigned in the same project as the **TMS Administrator** policy         |
   |                       |                                                                            | -  **VBS Administrator**: a project-level policy, which must be assigned in the same project as the **TMS Administrator** policy         |
   +-----------------------+----------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+

:ref:`Table 2 <tms_01_0009__table748201904614>` lists the common operations supported by system-defined policies for TMS.

.. _tms_01_0009__table748201904614:

.. table:: **Table 2** Common operations supported by system-defined policies

   +----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Operation                        | TMS Administrator                                                                                                                                                                                       |
   +==================================+=========================================================================================================================================================================================================+
   | Querying the cloud resource list | Not supported (depending on **Tenant Guest**)                                                                                                                                                           |
   +----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Creating keys                    | Not supported (depending on **Tenant Guest**)                                                                                                                                                           |
   +----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Managing tags                    | Not supported (depending on **Tenant Guest** and the project policy corresponding to the cloud resource. For example, if you want to manage the VPC tags, select **Tenant Guest** in the same project.) |
   +----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Creating predefined tags         | Supported                                                                                                                                                                                               |
   +----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Modifying predefined tags        | Supported                                                                                                                                                                                               |
   +----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Deleting predefined tags         | Supported                                                                                                                                                                                               |
   +----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Related Documents
-----------------

-  `What Is IAM? <https://docs.otc.t-systems.com/identity-access-management/umn/service_overview/what_is_iam.html>`__
-  :ref:`Creating a User and Granting Permissions <tms_04_0002>`
-  Section "Permissions Policies and Supported Actions" in *Tag Management Service API Reference*

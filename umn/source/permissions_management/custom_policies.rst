:original_name: tms_04_0008.html

.. _tms_04_0008:

Custom Policies
===============

Custom policies can be created to supplement the predefined policies provided by TMS. For details about the actions available for custom policies, see :ref:`Permissions <tms_01_0009>`.

You can create a custom policy in either of the following ways:

-  Visual editor: Select cloud services, actions, resources, and request conditions. This does not require knowledge of policy syntax.
-  JSON: Create a JSON policy or edit an existing one.

For details, see `Creating a Custom Policy <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0016.html>`__. Examples of common TMS custom policies are as follows:

Example Custom Policies
-----------------------

-  Example 1: Grant permission to view predefined tags

   .. code-block::

      {
          "Version": "1.1",
          "Statement": [
              {
                  "Effect": "Allow",
                  "Action": [
                      "tms:predefineTags:list"
                  ]
              }
          ]
      }

-  Example 2: Grant permission to deny predefined tag deletion

   A policy with only "Deny" permissions must be used together with other policies. If the permissions granted to an IAM user contain both "Allow" and "Deny", the "Deny" permissions take precedence over the "Allow" permissions.

   Assume that you want to grant the permissions of the **TMS FullAccess** to a user but want to prevent them from deleting predefined tags. You can create a custom policy for denying predefined tag deletion, and attach this policy together with the **TMS FullAccess** policy to the user. As an explicit deny in any policy overrides any allows, the user can perform all operations on these tags excepting deleting them. Example policy denying predefined tag deletion:

   .. code-block::

      {
          "Version": "1.1",
          "Statement": [
              {
                  "Effect": "Deny",
                  "Action": [
                      "tms:predefineTags:delete"
                  ]
              }
          ]
      }

-  Example 3: Create a custom policy containing multiple actions.

   A custom policy can contain the actions of one or multiple services that are of the same type (global or project-level).

   Example policy containing multiple actions:

   .. code-block::

      {
          "Version": "1.1",
          "Statement": [
              {
                  "Effect": "Allow",
                  "Action": [
                      "tms:predefineTags:create",
                      "tms:predefineTags:delete"
                  ]
              },
              {
                  "Effect": "Allow",
                  "Action": [
                      "obs:bucket:ListAllMyBuckets",
                      "obs:bucket:ListBucket"
                  ]
              }
          ]
      }

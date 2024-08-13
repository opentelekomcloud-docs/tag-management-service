:original_name: tms_04_0008.html

.. _tms_04_0008:

Custom Policies
===============

The following lists examples of custom policies for TMS.

Example Custom Policies
-----------------------

-  Example 1: Granting permission to view predefined tags

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

-  Example 2: Granting permission to deny predefined tag deletion

   "Deny" permissions should be used together with "Allow" permissions. If "Deny" and "Allow" permissions are both assigned, the "Deny" permissions take precedence over the "Allow" permissions.

   Assume that you want to grant the **TMS FullAccess** permissions to a user but do not want them to delete predefined tags. You can create a custom policy for denying predefined tag deletion, and attach this policy together with the **TMS FullAccess** policy to the user. As an explicit deny in any policy overrides any allows, the user can perform all operations on these predefined tags excepting deleting them. The following shows an example policy for denying predefined tag deletion.

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

-  Example 3: Creating a custom policy containing multiple actions.

   A custom policy can contain actions of one or more services. To grant permissions of multiple services in a policy, ensure that the services are all of the same level (global or project).

   The following shows an example policy that contains multiple actions.

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

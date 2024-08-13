:original_name: tms_02_0006.html

.. _tms_02_0006:

Deleting Resource Tags
======================

Deleting a Tag for a Cloud Resource
-----------------------------------

To delete a tag for a cloud resource, perform the following steps:

#. Log in to the management console.

#. Under **Management & Deployment**, select **Tag Management Service**.

#. Set the resource search criteria.

   For details, see :ref:`Searching for Resources <en-us_topic_0056266264>`.

#. Click **Edit** in the upper right part of the **Search Result** area so that you can edit tag values in the list.

#. (Optional) Set the key display list.

   If the key of the tag to be deleted is not displayed in the list, perform the following steps:

   a. In the upper right corner of the **Search Result** list, click |image1|.

   b. Select the key of the tag to be deleted from the drop-down list.

      You are advised not to select more than 10 keys to display.

#. Locate the row containing the resource whose tag you want to delete and click |image2|.

   After a resource tag is deleted, resources cannot be managed based on the deleted tag.

   .. note::

      To delete multiple tags of a resource, repeat the preceding steps. You can also select the target resource in the list and click **Manage Tag** above the list to delete one or more tags. For details, see :ref:`Deleting Tags for Multiple Cloud Resources <tms_02_0006__section35202115111142>`.

.. _tms_02_0006__section35202115111142:

Deleting Tags for Multiple Cloud Resources
------------------------------------------

To delete tags for multiple cloud resources, perform the following steps:

.. important::

   Exercise caution when deleting tags in batches.

   After you delete a tag, it will be removed from all corresponding cloud resources and you will not be able to recover it.

#. Log in to the management console.

#. Under **Management & Deployment**, select **Tag Management Service**.

#. Set the resource search criteria.

   For details, see :ref:`Searching for Resources <en-us_topic_0056266264>`.

#. Click **Search**.

#. Select one or more target resources.

#. Click **Manage Tag** above the list.

#. In the **Edit Tag** area, locate a target tag and click **Delete** in the **Operation** column.

   All tags of the target resources are displayed in the **Edit Tag** area. You can delete one or more tags as needed.

#. Click **OK**.

   After a resource tag is deleted, resources cannot be managed based on the deleted tag.

.. |image1| image:: /_static/images/en-us_image_0145874750.png
.. |image2| image:: /_static/images/en-us_image_0141727100.png

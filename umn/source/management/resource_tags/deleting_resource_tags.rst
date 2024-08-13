:original_name: tms_02_0006.html

.. _tms_02_0006:

Deleting Resource Tags
======================

Deleting a Tag for a Resource
-----------------------------

The following procedure shows how to delete a tag for a resource.

#. Log in to the management console.

#. In the upper left corner of the page, click |image1|, and then click **Management & Deployment** > **Tag Management Service**.

#. Set the resource search criteria.

   For details, see :ref:`Searching for Resources <en-us_topic_0056266264>`.

#. Click **Edit** in the upper right part of the **Search Result** area so that you can edit tag values in the list.

#. (Optional) Set the key display list.

   If the key of the tag to be deleted is not displayed in the list, perform the following steps:

   a. In the right corner of the search result area, click |image2|.

   b. Select target keys from the drop-down list.

      You are advised not to select more than 10 keys.

#. Click |image3| in the row that contains the resource to be deleted.

   After a resource tag is deleted, resources cannot be managed based on the deleted tag.

   .. note::

      To delete multiple tags of a resource, repeat the preceding steps. You can also select the target resource in the list and click **Manage Tag** above the list to delete one or more tags. For details, see :ref:`Deleting Tags for Multiple Resources <tms_02_0006__section35202115111142>`.

.. _tms_02_0006__section35202115111142:

Deleting Tags for Multiple Resources
------------------------------------

The following procedure shows how to delete tags for multiple resources.

.. important::

   Exercise caution when deleting tags in batches.

   After you delete tags based on the following procedure, the tags will be deleted from all resources that are attached with the same tag key, and the deletion cannot be undone.

#. Log in to the management console.

#. In the upper left corner of the page, click |image4|, and then click **Management & Deployment** > **Tag Management Service**.

#. Set the resource search criteria.

   For details, see :ref:`Searching for Resources <en-us_topic_0056266264>`.

#. Click **Search**.

#. Select one or more target resources.

#. Click **Manage Tag** above the list.

#. In the **Edit Tag** area, locate a target tag and click **Delete** in the **Operation** column.

   All tags of the target resources are displayed in the **Edit Tag** area. You can delete tags as needed.

#. Click **OK**.

   You can no longer manage related resources based on deleted tags.

.. |image1| image:: /_static/images/en-us_image_0000001950886124.png
.. |image2| image:: /_static/images/en-us_image_0000001949896556.png
.. |image3| image:: /_static/images/en-us_image_0000001980537901.png
.. |image4| image:: /_static/images/en-us_image_0000001982565529.png

:original_name: en-us_topic_0056266267.html

.. _en-us_topic_0056266267:

Modifying Resource Tags
=======================

.. _en-us_topic_0056266267__section303626711947:

Modifying a Tag for a Cloud Resource
------------------------------------

In this section, modifying a tag is through modifying the value of a tag key, and the corresponding tag key remains unchanged.

#. Log in to the management console.

#. Under **Management & Deployment**, select **Tag Management Service**.

#. Set the resource search criteria.

   For details, see :ref:`Searching for Resources <en-us_topic_0056266264>`.

#. Click **Search**.

#. Click **Edit** in the upper right part of the **Search Result** area so that you can edit tag values in the list.

#. (Optional) Set the key display list.

   If the key of the tag to be modified is not displayed in the list, perform the following steps:

   a. In the upper right corner of the **Search Result** list, click |image1|.

   b. Select the key of the tag to be modified from the drop-down list.

      You are advised to display no more than 10 keys.

#. Locate the row containing the cloud resource whose tag you want to modify and click |image2|.

#. Enter a new tag value.

#. Click |image3|.

   After the resource tag is modified, the cloud resources can be managed based on the new tag.

   .. note::

      To modify multiple tags of a resource, repeat the preceding steps. You can also select the target resource in the list and click **Manage Tag** above the list to modify one or more tags. For details, see :ref:`Modifying Tags for Multiple Cloud Resources <en-us_topic_0056266267__section1906940111333>`.

.. _en-us_topic_0056266267__section1906940111333:

Modifying Tags for Multiple Cloud Resources
-------------------------------------------

You can only modify tags of resources that have already been tagged.

.. important::

   Exercise caution when modifying tags in batches. After a tag value is modified, the tag values of corresponding cloud resources will be modified and cannot be recovered.

#. Log in to the management console.

#. Under **Management & Deployment**, select **Tag Management Service**.

#. Set the resource search criteria.

   For details, see :ref:`Searching for Resources <en-us_topic_0056266264>`.

#. Click **Search**.

#. Select one or more target resources in the list and click **Manage Tag** above the list.

#. In the **Edit Tag** area, specify new values for tags.

   All tags of the target resources are displayed in the **Edit Tag** area. You can modify one or more tags as needed.

   .. note::

      To set different values of a tag for multiple cloud resources, see :ref:`Modifying a Tag for a Cloud Resource <en-us_topic_0056266267__section303626711947>`.

#. Click **OK**.

   Then you can use the modified tags to manage resources.

.. |image1| image:: /_static/images/en-us_image_0238398847.png
.. |image2| image:: /_static/images/en-us_image_0153920847.png
.. |image3| image:: /_static/images/en-us_image_0153921664.png

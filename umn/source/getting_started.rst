:original_name: en-us_topic_0056130823.html

.. _en-us_topic_0056130823:

Getting Started
===============

Adding Tags to Cloud Resources
------------------------------

You can add tags to cloud resources in either of the following ways:

-  Adding tags on the TMS console

   When you need to tag a batch of cloud resources, add tags on the TMS console.

-  Adding tags on the consoles of other cloud services

   When you use the resources of a specific service, you can add tags on the corresponding service console. For new cloud resources, you can configure tag items when configuring parameters.

   .. note::

      -  You can use predefined tags to tag resources without the need to enter tag keys and values. Predefined tags are more efficient and less error-prone.
      -  It is strongly recommended that you do not place confidential or sensitive information (such as your customer's name, email address, or mobile number) in the tag field.

Constraints
-----------

-  Each resource supports up to 20 key-value pairs.
-  For each resource, each tag key must be unique, and each tag key can have only one tag value.
-  You can enter a maximum of 36 and 43 characters for **Key** and **Value**, respectively. Both **Key** and **Value** can contain only digits, letters, hyphens (-), at signs (@), and underscores (_).

Adding Tags on the TMS Console
------------------------------

You can tag your resources using TMS to centrally classify and manage your resources.

#. Log in to the management console.

#. In the upper left corner of the page, click |image1|, and then click **Management & Deployment** > **Tag Management Service**.

#. Set the resource search criteria.

   For details, see :ref:`Searching for Resources <en-us_topic_0056266264>`.

#. Click **Search**.

#. In the **Search Result** list, select the cloud resource to which you want to add tags and click **Manage Tag** in the upper left corner.

#. In the **Add Tag** area, enter a tag key and a tag value.

   You can also directly select existing tags from the drop-down list.

#. Click **OK**.

Adding Tags on the Consoles of Other Cloud Services
---------------------------------------------------

The following procedure shows how you add tags on the service console. This procedure may differ slightly from service to service.

#. Log in to the management console.

#. Under **Service List**, select a target service. For details about supported services and resource types, see :ref:`TMS and Other Services <en-us_topic_0056858747>`.

#. On the displayed service console, click the resource to which you want to add a tag.

#. Select the **Tags** tab.

#. Click **Add Tag**.

#. In the displayed **Add Tag** dialog box, enter a tag key and a tag value.

   You can also directly select predefined tags from the drop-down list.

#. Click **OK**.

Checking Whether a Tag Takes Effect
-----------------------------------

If you have added a tag to a resource, you can check whether the tag takes effect by searching for the resource with the added tag.

#. Log in to the management console.

#. In the upper left corner of the page, click |image2|, and then click **Management & Deployment** > **Tag Management Service**.

#. Select the **Tag Management** tab.

#. Set the resource search criteria.

   Set the region and resource type as needed.

   For **Resource Tag**, enter the tag that has been added to the resource.

#. Click **Search**.

   The resource is displayed in the **Search Result** list.

.. |image1| image:: /_static/images/en-us_image_0000001982565541.png
.. |image2| image:: /_static/images/en-us_image_0000001982445689.png

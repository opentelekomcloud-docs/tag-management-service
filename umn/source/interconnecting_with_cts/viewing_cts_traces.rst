:original_name: en-us_topic_0110866980.html

.. _en-us_topic_0110866980:

Viewing CTS Traces
==================

**Scenarios**
-------------

After CTS is enabled, it starts recording operations on cloud resources. The CTS management console stores the last seven days of operation records.

This topic describes how to query or export the last seven days of operation records on the CTS console.

.. note::

   You can also configure TMS key operation notifications on the CTS console. When these key operations are performed, notifications are sent to the related subscribers in real time through SMN. For details, see section "Configuring Key Event Notification" in the *Cloud Trace Service User Guide*.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click **Service List** and choose **Management & Deployment** > **Cloud Trace Service**.

#. In the left navigation pane, choose **Trace List**.

#. Specify filters as needed. The following filters are available:


   .. figure:: /_static/images/en-us_image_0000001369232030.png
      :alt: **Figure 1** Filtering connections

      **Figure 1** Filtering connections

   -  **Trace Source**, **Resource Type**, and **Search By**

      Select the desired content from the drop-down lists one by one.

      When you select **Trace name** for **Search By**, select a trace name.

      When you select **Resource ID** for **Search By**, enter a resource ID.

      When you select **Resource name** for **Search By**, select or enter a resource name.

   -  **Operator**: Select a specific operator at the user level rather than the account level.

   -  **Trace Status**: Select **All trace statuses**, **Normal**, **Warning**, or **Incident**.

   -  Time range: You can query traces generated at any time range in the last seven days.

6. Click |image2| on the left of the required trace to expand its details.


   .. figure:: /_static/images/en-us_image_0000001420271697.png
      :alt: **Figure 2** Trace details

      **Figure 2** Trace details

7. Click **View Trace** in the **Operation** column. On the displayed **View Trace** dialog box, the trace structure details are displayed.


   .. figure:: /_static/images/en-us_image_0000001419952997.png
      :alt: **Figure 3** View Trace

      **Figure 3** View Trace

.. |image1| image:: /_static/images/en-us_image_0000001369711658.png
.. |image2| image:: /_static/images/en-us_image_0000001369711662.jpg

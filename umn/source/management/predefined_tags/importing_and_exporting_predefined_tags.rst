:original_name: en-us_topic_0056266555.html

.. _en-us_topic_0056266555:

Importing and Exporting Predefined Tags
=======================================

Constraints and Limitations
---------------------------

You can only import CSV files that use UTF-8 encoding.

Tag files or templates downloaded with Internet Explorer 9 cannot be imported to TMS via other browsers, and vice versa those downloaded with other browsers cannot be imported to TMS via Internet Explorer 9.

If duplicate tags exist between the current environment and the imported file, the tags of the current environment will be overwritten after the import.

When you edit imported tags, the following rules need to be followed:

-  You can create up to 500 predefined tags for each account.
-  You can enter a maximum of 36 and 43 characters for **Key** and **Value**, respectively. Both **Key** and **Value** can contain only digits, letters, hyphens (-), at signs (@), and underscores (_).

.. important::

   If you edit a CSV file with Excel and then import the file to TMS, the tags will be garbled. To edit a CSV file, open it with notepad.

Importing Predefined Tags
-------------------------

You can batch import tags to TMS, and then attach them to your resources.

To import predefined tags, perform the following steps:

#. Log in to the management console.

#. In the upper left corner of the page, click |image1|. Select **Management & Deployment** > **Tag Management Service**.

#. Click **Predefined Tags**.

#. Click **Download template (CSV file)** in the message that is displayed above the list.

#. Fill in the template by referring to the format of existing tags.

#. Click **Import** and select the target file.

#. Click **OK**.

   The predefined tags are imported successfully and displayed in the predefined tag list.

Exporting Predefined Tags
-------------------------

To export predefined tags for editing, perform the following steps:

#. Log in to the management console.
#. In the upper left corner of the page, click |image2|. Select **Management & Deployment** > **Tag Management Service**.
#. Click **Predefined Tags**.
#. You can export predefined tags in either of the following ways:

   a. Click **Export All**.

      The .csv file is generated, and all predefined tags are exported.

   b. Select the predefined tags to be exported and click **Export**.

      The .csv file is generated, and selected predefined tags are exported.

.. |image1| image:: /_static/images/en-us_image_0000001950886112.png
.. |image2| image:: /_static/images/en-us_image_0000001982565521.png

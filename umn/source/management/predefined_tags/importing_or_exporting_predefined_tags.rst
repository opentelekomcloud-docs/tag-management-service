:original_name: en-us_topic_0056266555.html

.. _en-us_topic_0056266555:

Importing or Exporting Predefined Tags
======================================

Constraints and Limitations
---------------------------

You can import a .csv file from a third party to TMS. The encoding format of the .csv file must be UTF-8.

Tag files or templates downloaded with Internet Explorer 9 cannot be imported to TMS via other browsers, and vice versa those downloaded with other browsers cannot be imported to TMS via Internet Explore 9.

If duplicate tags exist between the current environment and the imported file, the tags of the current environment will be overwritten after the import.

When you edit imported tags, the following rules need to be followed:

-  You can add up to 500 predefined tags.
-  You can enter a maximum of 36 and 43 characters for **Key** and **Value**, respectively. Both **Key** and **Value** can contain only digits, letters, hyphens (-), at signs (@), and underscores (_).

.. important::

   Predefined tag importation does not support .csv files that have been modified in Excel files. Attempting to import such files will produce garbled characters and result in an importation failure. To edit a .csv file, open it with notepad.

Importing Predefined Tags
-------------------------

If you have inventory tags, you can quickly import them to the TMS predefined tags to facilitate subsequent resource association.

To import predefined tags, perform the following steps:

#. Log in to the management console.

#. Under **Management & Deployment**, select **Tag Management Service**.

#. Click **Predefined Tags**.

#. Click **Download template (CSV file)**.

#. Fill in the template by referring to the format of existing tags.

#. Click **Import** and select the target file.

#. Click **OK**.

   The predefined tags are imported successfully and displayed in the predefined tag list.

Exporting Predefined Tags
-------------------------

To export predefined tags for editing, perform the following steps:

#. Log in to the management console.
#. Under **Management & Deployment**, select **Tag Management Service**.
#. Click **Predefined Tags**.
#. You can export predefined tags in either of the following ways:

   a. Click **Export All**.

      The .csv file is generated, and all predefined tags are exported.

   b. Select target predefined tags and click **Export**.

      The .csv file is generated, and selected predefined tags are exported.

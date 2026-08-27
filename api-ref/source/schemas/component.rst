:original_name: en-sd_schema_component.html

.. _en-sd_schema_component:

Component
=========

.. table:: **Table 1** Component

   +----------+--------------------+---------+-----------------------------------+
   |Parameter |Type                |Mandatory|Description                        |
   +==========+====================+=========+===================================+
   |id        |Integer (int64)     |Yes      |Specifies the component ID.        |
   +----------+--------------------+---------+-----------------------------------+
   |name      |String              |Yes      |Specifies the component name.      |
   +----------+--------------------+---------+-----------------------------------+
   |attributes|ComponentAttr object|Yes      |Specifies the component attributes.|
   +----------+--------------------+---------+-----------------------------------+

-  Example

   .. code-block:: json

      {
          "id": 218,
          "name": "Object Storage Service",
          "attributes": {
              "name": "category",
              "value": "Storage"
          }
      }

:original_name: en-sd_schema_component_attr.html

.. _en-sd_schema_component_attr:

ComponentAttr
=============

.. table:: **Table 1** ComponentAttr

   +---------+------+---------+---------------------------------------------+
   |Parameter|Type  |Mandatory|Description                                  |
   +=========+======+=========+=============================================+
   |name     |String|No       |Attribute name. Enum: category, region, type.|
   +---------+------+---------+---------------------------------------------+
   |value    |String|No       |Attribute value.                             |
   +---------+------+---------+---------------------------------------------+

-  Example

   .. code-block:: json

      {
          "name": "category",
          "value": "Storage"
      }

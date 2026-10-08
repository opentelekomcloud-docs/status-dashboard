:original_name: en-sd_topic_0000000022.html

.. _en-sd_topic_0000000022:

Get All Components
==================

Function
--------

This API is used to get all components.

URI
---

GET /v2/components

Request
-------

None.

Response
--------

.. table:: **Table 1** Response parameters

   +---------+--------------------------+-------------------------+
   |Parameter|Type                      |Description              |
   +=========+==========================+=========================+
   |data     |Array of Component objects|A list of all components.|
   +---------+--------------------------+-------------------------+

-  Example response

   .. code-block:: json

      [
          {
              "id": 218,
              "name": "Object Storage Service",
              "attributes": {
                  "name": "category",
                  "value": "Storage"
              }
          },
          {
              "id": 254,
              "name": "Auto Scaling",
              "attributes": {
                  "name": "category",
                  "value": "Compute"
              }
          }
      ]

Status Codes
------------

.. table:: **Table 2** Status codes

   +------+---------------------+
   |Status|Description          |
   +======+=====================+
   |200   |Successful operation.|
   +------+---------------------+

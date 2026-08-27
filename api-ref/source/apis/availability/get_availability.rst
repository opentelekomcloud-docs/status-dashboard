:original_name: en-sd_topic_0000000052.html

.. _en-sd_topic_0000000052:

Get Availability
================

Function
--------

This API is used to get availability data for components.

URI
---

GET /v2/availability

Request
-------

None.

Response
--------

.. table:: **Table 1** Response parameters

   +---------+--------------------------------------+---------------------------------+
   |Parameter|Type                                  |Description                      |
   +=========+======================================+=================================+
   |data     |Array of ComponentAvailability objects|Availability data for components.|
   +---------+--------------------------------------+---------------------------------+

-  Example response

   .. code-block:: json

      {
          "data": [
              {
                  "id": 218,
                  "name": "Auto Scaling",
                  "region": "EU-DE",
                  "availability": [
                      {
                          "year": 2024,
                          "month": 5,
                          "percentage": 99.999666
                      }
                  ]
              }
          ]
      }

Status Codes
------------

.. table:: **Table 2** Status codes

   +------+---------------------+
   |Status|Description          |
   +======+=====================+
   |200   |Successful operation.|
   +------+---------------------+

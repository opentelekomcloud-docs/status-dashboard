:original_name: en-sd_topic_0000000044.html

.. _en-sd_topic_0000000044:

Find an Event by ID
===================

Function
--------

This API is used to find an event by its ID.

URI
---

GET /v2/events/{event_id}

.. table:: **Table 1** Parameter description

   +---------+-------+---------+----------------------+
   |Parameter|Type   |Mandatory|Description           |
   +=========+=======+=========+======================+
   |event_id |Integer|Yes      |ID of event to return.|
   +---------+-------+---------+----------------------+

Request
-------

None.

Response
--------

.. table:: **Table 1** Response parameters

   +---------+---------------+------------------+
   |Parameter|Type           |Description       |
   +=========+===============+==================+
   |data     |Incident object|The event details.|
   +---------+---------------+------------------+

-  Example response

   .. code-block:: json

      {
          "id": 200,
          "title": "OpenStack Upgrade in regions EU-DE/EU-NL",
          "description": "The service is partially unavailable or its performance has decreased.",
          "impact": 1,
          "components": [218, 254],
          "start_date": "2024-01-15T10:00:00Z",
          "end_date": "2024-01-15T12:00:00Z",
          "system": false,
          "type": "incident",
          "updates": [
              {
                  "status": "in progress",
                  "text": "Investigating the issue.",
                  "timestamp": "2024-01-15T10:00:00Z"
              }
          ],
          "status": "in progress"
      }

Status Codes
------------

.. table:: **Table 2** Status codes

   +------+---------------------+
   |Status|Description          |
   +======+=====================+
   |200   |Successful operation.|
   +------+---------------------+
   |400   |Invalid ID supplied. |
   +------+---------------------+
   |404   |Event not found.     |
   +------+---------------------+

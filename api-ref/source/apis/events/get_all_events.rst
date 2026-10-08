:original_name: en-sd_topic_0000000042.html

.. _en-sd_topic_0000000042:

Get All Events
==============

Function
--------

This API is used to get all events with pagination.

URI
---

GET /v2/events

.. table:: **Table 1** Query parameters

   +----------+-------+---------+------------------------------------------------------------------------------------+
   |Parameter |Type   |Mandatory|Description                                                                         |
   +==========+=======+=========+====================================================================================+
   |type      |String |No       |Filter by event type (incident, maintenance or info). Can be a comma-separated list.|
   +----------+-------+---------+------------------------------------------------------------------------------------+
   |active    |Boolean|No       |Filter by active status for events.                                                 |
   +----------+-------+---------+------------------------------------------------------------------------------------+
   |status    |String |No       |Filter by the latest event status (e.g., resolved, fixing, completed).              |
   +----------+-------+---------+------------------------------------------------------------------------------------+
   |start_date|String |No       |Filter events active on or after this date (RFC3339 format).                        |
   +----------+-------+---------+------------------------------------------------------------------------------------+
   |end_date  |String |No       |Filter events active on or before this date (RFC3339 format).                       |
   +----------+-------+---------+------------------------------------------------------------------------------------+
   |impact    |Integer|No       |Filter by specific impact level (0=Maintenance, 1=Minor, 2=Major, 3=Outage).        |
   +----------+-------+---------+------------------------------------------------------------------------------------+
   |system    |Boolean|No       |Filter by whether the event was system-generated (true) or manually created (false).|
   +----------+-------+---------+------------------------------------------------------------------------------------+
   |components|String |No       |Filter by associated component IDs (comma-separated list of positive integers).     |
   +----------+-------+---------+------------------------------------------------------------------------------------+
   |page      |Integer|No       |The page number for pagination.                                                     |
   +----------+-------+---------+------------------------------------------------------------------------------------+
   |limit     |Integer|No       |The number of items to return. Default: 50. Allowed values: 10, 20, 50.             |
   +----------+-------+---------+------------------------------------------------------------------------------------+

Request
-------

None.

Response
--------

.. table:: **Table 2** Response parameters

   +----------+-------------------------+-----------------------------------+
   |Parameter |Type                     |Description                        |
   +==========+=========================+===================================+
   |data      |Array of Incident objects|A list of events matching criteria.|
   +----------+-------------------------+-----------------------------------+
   |pagination|Pagination object        |Pagination information.            |
   +----------+-------------------------+-----------------------------------+

If no events match the criteria, **data** is an empty array.

-  Example response

   .. code-block:: json

      {
          "data": [
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
          ],
          "pagination": {
              "pageIndex": 1,
              "recordsPerPage": 50,
              "totalRecords": 100,
              "totalPages": 2
          }
      }

Status Codes
------------

.. table:: **Table 3** Status codes

   +------+-----------------------------------------------+
   |Status|Description                                    |
   +======+===============================================+
   |200   |Successful operation. Returns a list of events.|
   +------+-----------------------------------------------+

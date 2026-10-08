:original_name: en-sd_topic_0000000023.html

.. _en-sd_topic_0000000023:

Get Target Component
====================

Function
--------

This API is used to get a target component by its ID.

URI
---

GET /v2/components/{component_id}

.. table:: **Table 1** Parameter description

   +------------+-------+---------+------------------------------------+
   |Parameter   |Type   |Mandatory|Description                         |
   +============+=======+=========+====================================+
   |component_id|Integer|Yes      |The ID of the component to retrieve.|
   +------------+-------+---------+------------------------------------+

Request
-------

None.

Response
--------

.. table:: **Table 1** Response parameters

   +---------+----------------+----------------------+
   |Parameter|Type            |Description           |
   +=========+================+======================+
   |data     |Component object|The component details.|
   +---------+----------------+----------------------+

-  Example response

   .. code-block:: json

      {
          "id": 218,
          "name": "Object Storage Service",
          "attributes": {
              "name": "category",
              "value": "Storage"
          }
      }

Status Codes
------------

.. table:: **Table 2** Status codes

   +------+---------------------------+
   |Status|Description                |
   +======+===========================+
   |200   |Successful operation.      |
   +------+---------------------------+
   |404   |The component is not found.|
   +------+---------------------------+
   |500   |Internal server error.     |
   +------+---------------------------+

For the **404** response, the response body follows this format:

.. code-block:: json

   {
       "errMsg": "component does not exist"
   }

For the **500** response, the response body follows the :ref:`InternalServerError <en-sd_schema_internal_server_error>` schema.

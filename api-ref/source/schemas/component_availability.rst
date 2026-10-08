:original_name: en-sd_schema_component_availability.html

.. _en-sd_schema_component_availability:

ComponentAvailability
=====================

.. table:: **Table 1** ComponentAvailability

   +------------+-----------------------------+---------+--------------------------------------------------+
   |Parameter   |Type                         |Mandatory|Description                                       |
   +============+=============================+=========+==================================================+
   |id          |Integer (int64)              |Yes      |Specifies the component ID.                       |
   +------------+-----------------------------+---------+--------------------------------------------------+
   |name        |String                       |Yes      |Specifies the component name.                     |
   +------------+-----------------------------+---------+--------------------------------------------------+
   |region      |String                       |Yes      |Specifies the region name.                        |
   +------------+-----------------------------+---------+--------------------------------------------------+
   |availability|Array of availability objects|Yes      |Specifies the availability data for the component.|
   +------------+-----------------------------+---------+--------------------------------------------------+

Each availability object contains:

.. table:: **Table 2** Availability object

   +----------+-------+---------+----------------------------------------------+
   |Parameter |Type   |Mandatory|Description                                   |
   +==========+=======+=========+==============================================+
   |year      |Integer|Yes      |Specifies the year.                           |
   +----------+-------+---------+----------------------------------------------+
   |month     |Integer|Yes      |Specifies the month.                          |
   +----------+-------+---------+----------------------------------------------+
   |percentage|Number |Yes      |Specifies the availability percentage (float).|
   +----------+-------+---------+----------------------------------------------+

-  Example

   .. code-block:: json

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

:original_name: en-sd_schema_incident_status.html

.. _en-sd_schema_incident_status:

IncidentStatus
==============

.. table:: **Table 1** IncidentStatus

   +---------+------------------+---------+-------------------------------+
   |Parameter|Type              |Mandatory|Description                    |
   +=========+==================+=========+===============================+
   |id       |Integer (int64)   |No       |Specifies the update ID.       |
   +---------+------------------+---------+-------------------------------+
   |status   |String            |No       |Specifies the status.          |
   +---------+------------------+---------+-------------------------------+
   |text     |String            |No       |Specifies the status text.     |
   +---------+------------------+---------+-------------------------------+
   |timestamp|String (date-time)|No       |Specifies the update timestamp.|
   +---------+------------------+---------+-------------------------------+

-  Example

   .. code-block:: json

      {
          "id": 0,
          "status": "resolved",
          "text": "issue resolved",
          "timestamp": "2024-01-15T12:00:00Z"
      }

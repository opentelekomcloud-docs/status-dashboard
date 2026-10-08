:original_name: en-sd_schema_incident.html

.. _en-sd_schema_incident:

Incident
========

.. table:: **Table 1** Incident

   +-----------+-----------------------+---------+---------------------------------------------------------+
   |Parameter  |Type                   |Mandatory|Description                                              |
   +===========+=======================+=========+=========================================================+
   |id         |Integer (int64)        |No       |Specifies the incident/event ID.                         |
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |title      |String                 |Yes      |Specifies the incident/event title.                      |
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |description|String                 |No       |Provides supplementary information.                      |
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |impact     |Integer                |Yes      |Impact level (0=Maintenance, 1=Minor, 2=Major, 3=Outage).|
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |components |Array of Integer       |Yes      |List of component IDs affected.                          |
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |start_date |String (date-time)     |Yes      |Start date in RFC3339 format.                            |
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |end_date   |String (date-time)     |No       |End date in RFC3339 format.                              |
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |system     |Boolean                |No       |Whether the incident/event was system-generated.         |
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |type       |String                 |Yes      |Type of event. Enum: incident, maintenance, info.        |
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |updates    |Array of IncidentStatus|No       |Array of status updates.                                 |
   +-----------+-----------------------+---------+---------------------------------------------------------+
   |status     |String                 |No       |Current status of the incident/event.                    |
   +-----------+-----------------------+---------+---------------------------------------------------------+

The **type** field can have the following values:

-  **incident**: An incident event.
-  **maintenance**: A maintenance event.
-  **info**: An informational event.

The **status** field can have the following values:

-  **analysing**: The incident is being analyzed.
-  **fixing**: The incident is being fixed.
-  **impact changed**: The impact level has changed.
-  **observing**: The incident is being observed.
-  **resolved**: The incident has been resolved.
-  **reopened**: The incident has been reopened.
-  **changed**: The incident has been changed.
-  **in progress**: The incident is currently being worked on.
-  **modified**: The incident has been modified.
-  **completed**: The incident has been completed.
-  **planned**: The incident is planned.
-  **active**: The incident is active.
-  **cancelled**: The incident has been cancelled.

-  Example

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
                  "id": 0,
                  "status": "in progress",
                  "text": "Investigating the issue.",
                  "timestamp": "2024-01-15T10:00:00Z"
              }
          ],
          "status": "in progress"
      }

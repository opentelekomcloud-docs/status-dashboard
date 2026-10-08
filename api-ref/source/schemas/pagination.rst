:original_name: en-sd_schema_pagination.html

.. _en-sd_schema_pagination:

Pagination
==========

.. table:: **Table 1** Pagination

   +--------------+-------+---------+---------------------------------------------+
   |Parameter     |Type   |Mandatory|Description                                  |
   +==============+=======+=========+=============================================+
   |pageIndex     |Integer|Yes      |Specifies the current page number.           |
   +--------------+-------+---------+---------------------------------------------+
   |recordsPerPage|Integer|Yes      |Number of records per page. Enum: 10, 20, 50.|
   +--------------+-------+---------+---------------------------------------------+
   |totalRecords  |Integer|Yes      |Total number of records.                     |
   +--------------+-------+---------+---------------------------------------------+
   |totalPages    |Integer|Yes      |Total number of pages.                       |
   +--------------+-------+---------+---------------------------------------------+

-  Example

   .. code-block:: json

      {
          "pageIndex": 1,
          "recordsPerPage": 50,
          "totalRecords": 500,
          "totalPages": 10
      }

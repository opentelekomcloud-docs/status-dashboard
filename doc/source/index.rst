==================================================
User Guide for the T Cloud Public Status Dashboard
==================================================

| Welcome to the T Cloud Public Status Dashboard - Your go-to resource for monitoring the availability of various components across different regions.
| This guide is tailored for IT professionals to help navigate the platform and extract valuable insights from the T Cloud Public.

Accessing the Status Website
----------------------------

Visit the Status Website at https://status.otc-service.com/.

Selecting Regions
-----------------

The platform supports multiple regions. Use the appropriate tab to select your desired region (e.g., **“EU-DE”** for Germany, **“EU-NL”** for the Netherlands, or **“GLOBAL”** for global services) to check service availability in that area.

Service Status
--------------

Services are grouped into categories such as **Compute**, **Network**, or **Storage**. Each service is accompanied by an icon (also known as a *semaphore*) indicating its current status:

-  |image1| **Green:** Service fully operational

-  |image2| **Yellow:** Minor Incident - Service is available but may have minor restrictions or reduced performance

-  |image3| **Red-orange:** Major Incident - Service is partially available but may cause noticeable impact or interruptions

-  |image4| **Red:** Service Outage - Service is unresponsive or facing serious issues

-  |image5| **Green with a dot:** Upcoming planned maintenance

-  |image6| **Blue wrench:** Ongoing maintenance

-  |image11| **Information:** Inform about relevant product information

Auto-update / refresh of the dashboard
--------------------------------------

The dashboard automatically refreshes every minute. A green dot at the bottom of the page indicates that the update is functioning properly. |image7|

Incident / Maintenance Displays
-------------------------------

| Active **Incidents** or **Maintenances** are displayed above the main status area.
| Incidents are grouped by services affected at the same time, while maintenances are shown separately.

Current events appear as follows:

.. image:: /_static/images/image8.png
   :target: /status-dashboard/_images/image8.png
   :alt: image8.png

-  use the gear icon |image9| to adjust the display settings according to your preferences.

-  click the arrow icon |image10| to navigate to a detailed view of the event.

For incidents, we regularly provide updates to our customers via the status dashboard.

History
-------

Access **“History”** via the top navigation bar to explore a comprehensive record of past incidents.

Component Availability
----------------------

| Navigate to **“Availability”** in the top navigation bar to view component availability grouped by service over the past months.
| This feature provides insights into long-term service performance by region.

.. note::
   Service outages directly impact the availability metrics.


The Status Dashboard is designed to track and report the health and performance
of external T Cloud Public APIs. It regularly checks configured endpoints,
collects timing and status data, and emits structured metrics to help teams
monitor API availability, latency, and reliability.


T Cloud Public App
------------------

Another method is to use the `T Cloud Public App <https://public.t-cloud.com/en/support/app>`__, which allows you to receive push notifications in case of status changes.

Tips for Effective Use
----------------------

-  **Bookmark** the status website for quick access during troubleshooting.

-  **Leverage incident history** to identify recurring issues and explore potential optimizations.

-  **Customize notifications** by region and service using the platform's alert settings.

| Thank you for using **T Cloud Public**.
| If you have any questions or encounter any issues, our support team is here to help.

**Happy monitoring!**

.. |image1| image:: /_static/images/image1.png
   :target: /status-dashboard/_images/image1.png
   :alt: image1.png
   :align: top
   :width: 0.32296in
   :height: 0.40631in
.. |image2| image:: /_static/images/image2.png
   :target: /status-dashboard/_images/image2.png
   :alt: image2.png
   :align: top
   :width: 0.31254in
   :height: 0.31254in
.. |image3| image:: /_static/images/image3.png
   :target: /status-dashboard/_images/image3.png
   :alt: image3.png
   :align: top
   :width: 0.29171in
   :height: 0.3438in
.. |image4| image:: /_static/images/image4.png
   :target: /status-dashboard/_images/image4.png
   :alt: image4.png
   :align: top
   :width: 0.29171in
   :height: 0.37505in
.. |image5| image:: /_static/images/image5.png
   :target: /status-dashboard/_images/image5.png
   :alt: image5.png
   :align: top
   :width: 0.33338in
   :height: 0.39589in
.. |image6| image:: /_static/images/image6.png
   :target: /status-dashboard/_images/image6.png
   :alt: image6.png
   :align: top
   :width: 0.30213in
   :height: 0.37505in
.. |image7| image:: /_static/images/image7.png
   :target: /status-dashboard/_images/image7.png
   :alt: image7.png
   :align: top
   :width: 0.30213in
   :height: 0.38547in
.. |image9| image:: /_static/images/image9.png
   :target: /status-dashboard/_images/image9.png
   :alt: image9.png
   :align: top
   :width: 0.31915in
   :height: 0.30711in
.. |image10| image:: /_static/images/image10.png
   :target: /status-dashboard/_images/image10.png
   :alt: image10.png
   :align: top
   :width: 0.30411in
   :height: 0.25783in
.. |image11| image:: /_static/images/image11.png
   :target: /status-dashboard/_images/image11.png
   :alt: image11.png
   :align: top
   :width: 0.33411in
   :height: 0.3783in

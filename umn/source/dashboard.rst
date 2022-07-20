=============
The Dashboard
=============

The main dashboard is the first thing a user will see when accessing the
`Status Dashboard <https://status.otc-service.com/>`__ (SD). The main
dashboard provides the high-level overview of the status of monitored
services of the Open Telekom Cloud (OTC).

Structure of the dashboard
==========================

.. figure:: /_static/images/image2.jpeg
   :width: 6.62222in
   :height: 4.44792in

   Structure of Status Dashboard of Open Telekom Cloud

Messages displayed on the dashboard
-----------------------------------

Our Service Team may post messages on the SD. Those messages are for
informing customers about issues on the Open Telekom Cloud and measures
taken for remediating them, or any other information that can be in interest
for our customers. Messages can be posted for the whole Open Telekom Cloud
globally or for a specific region only:

.. figure:: /_static/images/image3.jpeg
   :width: 4.875in
   :height: 2.29167in

   Global or region-specific messages

Messages about upcoming and ongoing maintenances can be displayed on the
main dashboard.

Errors detected during ongoing maintenance are treated differently by the
SD.

.. figure:: /_static/images/image4.jpeg
   :width: 4.875in
   :height: 2.275in

   Maintenance information

States of a service
===================

Services and functions may be in different states. They may have some issues
(slowdown, instability, failure, etc.) or may be fully down. Most likely,
our customers will see three different status icons showing the state of the
service:

|image1| The service operates normally

|image2| The service is having some issues (e.g. requests take longer than
3 seconds)

|image3| The service is highly unstable or completely down (wrong answer or
request takes longer than 10 seconds)

In addition, there are two statuses indicating a planned as well as an
ongoing maintenance:

|image4| Maintenance is planned for the service

|image5| Maintenance is ongoing for the service

The tables below are showing all possible color codes and their associated
statuses:

**Services**

.. table:: Possible color codes and their associated statuses
   :widths: 50 10 40

   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | Functions (weight)                                                | Color                                   | Message                                   |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | All good (1)                                                      | .. image:: /_static/images/image10.jpeg | All functions are up and running          |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | Less than half of the functions are slow (2)                      | .. image:: /_static/images/image10.jpeg | Some functions may respond slowly         |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | Greater or equal than half of the functions are slow (2)          | .. image:: /_static/images/image11.jpeg | Most of the functions may response slowly |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | Less than half of the functions are slowed down (3)               | .. image:: /_static/images/image11.jpeg | Some functions are overloaded             |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | Greater than or equal to half of the functions are slowed down(3) | .. image:: /_static/images/image12.jpeg | All functions are slowed down             |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | Less than half of the functions are unstable (4)                  | .. image:: /_static/images/image13.jpeg | Some functions are unstable               |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | Less than or equal half of the functions are unstable (4)         | .. image:: /_static/images/image14.jpeg | Most of functions are unstable            |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | 1 or less than half of functions down (5)                         | .. image:: /_static/images/image14.jpeg | Some functions are down                   |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+
   | Greater than or equal to half of the functions down (5)           | .. image:: /_static/images/image14.jpeg | Service is down                           |
   +-------------------------------------------------------------------+-----------------------------------------+-------------------------------------------+

The same for functions of a certain service:

.. table:: Color modes of functions

   +------------------------------+-----------------------------------------+----------------------------------+
   | Last 10                      | Color                                   | Message                          |
   +------------------------------+-----------------------------------------+----------------------------------+
   | All good                     | .. image:: /_static/images/image10.jpeg | All responses are up and running |
   +------------------------------+-----------------------------------------+----------------------------------+
   | 3 slow                       | .. image:: /_static/images/image11.jpeg | Function may respond slowly      |
   +------------------------------+-----------------------------------------+----------------------------------+
   | Last 3 slow                  | .. image:: /_static/images/image12.jpeg | Function is slowed down          |
   +------------------------------+-----------------------------------------+----------------------------------+
   | 3 response time is zero      | .. image:: /_static/images/image15.jpeg | Instability                      |
   +------------------------------+-----------------------------------------+----------------------------------+
   | Last 3 response time is zero | .. image:: /_static/images/image16.jpeg | Function is down                 |
   +------------------------------+-----------------------------------------+----------------------------------+

Main functions of the Status Dashboard
======================================

Selecting a certain region will show all services monitored in that region

Clicking on the global RSS link (|image20|) will download the RSS source (XML).
If your browser is equipped with an RSS reader, it will most likely offer
subscribing to that feed (depends on the RSS reader installed)

Hoovering the cursor over the "Status" message of the service will lead to a
small pop-up window with statuses of all monitored functions of the particular
service

.. image:: /_static/images/image18.png
   :width: 4.875in
   :height: 1.71389in

Clicking on the "Details" link ( ) will open a new browser tab with detailed
information about the service on a Grafana page

Clicking on the RSS link (|image21|) of the service will download the RSS
source (XML) for that single service

The status filters
==================

In case of an issue detected for a region, the global status icon will show the
worst state that exists in the region. Also, if a planned maintenance is
defined in the SD system, the global status icon will show the upcoming
(|image22|) or ongoing (|image23|) maintenance. In such cases it can be
annoying to scroll through the page to find the service affected. For more
convenient listing of services in particular states the status filter is
implemented:

.. figure:: /_static/images/image21.jpeg
   :width: 4.875in
   :height: 1.40764in

   Using the status filter

The RSS feed
============

The SD provides RSS feeds for informing customers about status changes in our
services. There are two types of RSS feeds:

#. Global RSS feed:

   Will contain messages about any service in the region that changes its state (having issue, going down, coming up again).

#. Service specific RSS feed:

   Will contain messages only for the particular service for which it was created.

Items (messages) in the feed are sorted by the time of the detection of the
state change. The newest message will be always the first (descending order).

You may subscribe to those RSS feeds using any decent RSS reader. Although the
SD does not provide push notification functions, using the RSS feed with a
short enough refresh period may give almost the same functionality as push
notification would do.

The RSS feed may contain the following information:

- State change of a service: getting into the error state and the recovery

- Reminder about messages published for customers on the dashboard

Any message will be kept only for 24 hours in the feed.

.. |image1| image:: _static/images/image5.jpeg
   :width: 0.25in
   :height: 0.25in
.. |image2| image:: /_static/images/image6.jpeg
   :width: 0.25in
   :height: 0.25in
.. |image3| image:: /_static/images/image7.jpeg
   :width: 0.25in
   :height: 0.23611in
.. |image4| image:: /_static/images/image8.jpeg
   :width: 0.30556in
   :height: 0.25in
.. |image5| image:: /_static/images/image9.jpeg
   :width: 0.23611in
   :height: 0.25in
.. |image20| image:: /_static/images/image17.jpeg
   :width: 0.25in
   :height: 0.23611in
.. |image21| image:: /_static/images/image17.jpeg
   :width: 0.25in
   :height: 0.23611in
.. |image22| image:: /_static/images/image19.jpeg
   :width: 0.30556in
   :height: 0.23611in
.. |image23| image:: /_static/images/image20.jpeg
   :width: 0.23611in
   :height: 0.23611in

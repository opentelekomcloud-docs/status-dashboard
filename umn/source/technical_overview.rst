==================
Technical Overview
==================

The SD is a simplified monitoring system, capable to show if a service provided
by the Open Telekom Cloud is alive, having issues or is down. The user can see
current status and historical data for longer than 6 months. The SD is a
high-level monitoring system providing information about general availability
of services offered by the OTC. The platform is also monitored using other,
more detailed, professional grade monitoring systems used by the OTC Operation
team. Those monitoring systems are not available publicly. Each customer should
acknowledge that monitoring of their own resources used in their own tenants is
a responsibility of the given customer [#]_. The OTC provides tools for
that (one may set up monitoring of owned resources using services offered by
the OTC, like Cloud Eye, Log Tank Service, Cloud Trace Service).

The system is sending queries like API requests to three or more functions of a
service. The SD decides about the state of the service by measuring the
response time and checking the HTTP response code in replies to API requests.

In a general case, functions of the service itself are tested. In some cases,
test requests are sent to real entities created for the testing. Example of
that is the Elastic IP (EIP) test, which sends requests to basic HTTP servers
on real virtual machines created in different availability zones.

The SD provides information about:

- availability of OTC services for all regions and their AZs

- maintenances

- messages from the Service Team towards customer in case of service interruption

- historical monitoring data

- RSS feeds for information about state changes of services

- availability of SLA relevant services

- filtering states and maintenances shown on the dashboard

- overview of potentially problematic services


Main system components
======================

SD consists of four main components:

- The data collector Data handling

- The main dashboard The Grafana

The data collector
------------------

The data collector is sending out API requests and checks replies to those.
Results are exposed using HTTP serving for consuming those by the central
database of the SD.

The data collector uses two simple facts for showing error conditions:

#. The response time for an API request cannot ever equal to zero.

   Based on this it is possible to use the zero value for showing the error
   state. If an error or request time-out (10 sec) happens, the data collector
   forcibly sets the response time to zero. The zero value is used for showing
   the error in the system and plays essential role in displaying state and
   availability calculation.

#. The response time for an API request cannot ever equal to any negative value.

   In the SD it is possible to define a period of time for services during
   which period a planned maintenance is conducted. Those maintenances are
   communicated to customers. Some of them may cause temporary outages in the
   service maintained. If the data collector detects an error during such time
   frame, it will set the response time to a small negative value (currently
   -0.2 sec). Using this trick, the maintenance can be clearly displayed on
   graphs and it can be excluded from availability calculations.

The SD system can use as many data collectors as needed.

Data handling
-------------

The SD uses a time series database system for collecting, storing and providing
data for dashboards. The DB used in the SD is a Prometheus time series DB.

The Prometheus is capable to fetch data from its data sources. It sends HTTP
requests to data collectors in 60 sec period for fetching data measured by
them.

The data retention time in the Prometheus DB is a bit more than 200 days.
Thanks to this we may provide consolidated availability data for our services
for the last half year.

The main dashboard
------------------

The main dashboard is the first thing a visitor sees when accessing the SD.
This is also a proprietary software written by the same team as the data
collector. It shows the overall status of OTC regions and statuses of all
services monitored in those regions.

The Grafana
-----------

For displaying detailed measurement data for services, a Grafana server is
used. Several dashboards are defined in the Grafana system for providing
detailed information about our services for any period during the data
retention time set up for the Prometheus DB.

The customer's viewpoint
========================

Main goal of the SD is to provide our customers with monitoring information
measured from their viewpoint. To achieve that, the SD system is in a data
center fully independent from the OTC platform. Thanks to this, the SD "sees"
the OTC just like a customer would see.

Redundancy in the data collection
=================================

The SD can consume data from arbitrary number of data collectors. Using this
feature, we installed two data collectors for each OTC regions. This way
measurements are done for both regions (Germany and Netherlands) from Munich
and from London. This redundancy makes it possible to ignore errors of a single
data collector or the network path from a certain data collector to the OTC.
The main dashboard will always display the best data available from all
collectors. This way issues outside of the OTC are masked (they still can be
seen on Grafana dashboards).

.. [#] Please also check chapter 5 of the `service description:
   <https://open-telekom-cloud.com/service-description>`__ The customer´ duties
   to cooperate

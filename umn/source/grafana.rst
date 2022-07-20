===================================
Grafana Pages For Detailed Analysis
===================================

For showing detailed measurement information about OTC services, a Grafana
server hosting several dashboards is implemented in the SD system.

Service details
===============

Details about a particular service are displayed on a special Grafana page. It
can be accessed by clicking on the "Details" icon (|image24|) on the main
dashboard.

.. figure:: /_static/images/image23.jpeg
   :width: 6.61111in
   :height: 4.14514in

   Detailed view of a service

On this dashboard some availability data (for the previous month and for the
current month so far) is displayed for any service selected from the main
dashboard. Below that, the detailed measurement data is displayed for all data
collectors sending test requests to the particular service (in our case, data
collectors in London and Munich. More planned...).

In the upper left corner of graphs an information link is available. Hoovering
the cursor above the information area the information appears in a pop-up. Some
of those are containing links that can be followed.

The SLA relevant availability
=============================

The availability is calculated for all services. The SLA [#]_ contains
three core services and guarantees certain availability for those. These
services are:

#. Elastic Computing Service (ECS)

#. Elastic Volume Service (EVS)

#. Object Storage Service (OBS)

Availability for those services is also calculated. Monthly graphs for the last
half year are collected in a separate Grafana page accessible from the
information area of the last month availability graph of any service:

.. figure:: /_static/images/image24.jpeg
   :width: 6.60625in
   :height: 3.80208in

   Availability of SLA relevant services

In contrast to the SLA itself, the Grafana page shows availability for four
services. The fourth one is the Elastic IP service. It is included into this
Grafana page, because SD checks EIP availability by sending HTTP requests to
virtual machines (ECS) deployed in different availability zones through their
associated public IP addresses. That way this check provides information not
only about the status of the EIP service, but also about health of existing
virtual machines created by the ECS service.

.. figure:: /_static/images/image25.jpeg
   :width: 6.61736in
   :height: 3.6875in

   Overview of SLA measuring [#]_


"All-in-one" dashboard
======================

Clicking on the name of the Grafana dashboard ("OTC KPI Drilldown") will take
the user to the list of available dashboards. There are two of them that can be
used separately: "OTC KPI" and "OTC Problematic services". Others require
parameters passed to them when calling from the main dashboard, or from another
Grafana dashboard.

The "all-in-one" dashboard is the one called "OTC KPI". It displays graphs for
all monitored services for any selected region and time frame:

.. figure:: /_static/images/image26.jpeg
   :width: 6.61319in
   :height: 3.51181in

   "All-in-one" dashboard

IT professionals may need to see all, or selected services on a single page.
Once all graphs on the page are synchronized with each-other and displaying the
same period, some correlations between those graphs may give important hints
about deeper analysis of the state of the system.

Although it is technically possible to request information on this page about
all services in a region for the whole time period of the data retention
defined in the system, is still not a good idea to do that. It won't provide
much useful information but will put a huge load on the SD system.

Problematic services
====================

If an issue appears on the OTC, then - depending on the failing system element
- several services may be affected. To easily see measurement data for those
services on a single page, the dashboard described above has been duplicated
and a special filter has been added to it.

As a result, the "OTC Problematic services" dashboard collects all services
having any issue during the selected time frame in the Grafana page.

It is important to understand, that on this dashboard all services providing
one slow response or error at least from one measuring location will be
displayed. It doesn't necessarily mean that those services are really having an
issue. It may happen that only one data collector shows an increased response
time or error which is not correlating with results from the other one. In such
a case the OTC service is working well, but a data collector may be affected by
some network latency or alike. One should always pay attention to the
correlation of graphs on different data collectors for understanding the status
of the OTC service monitored.

.. |image24| image:: /_static/images/image22.jpeg
   :width: 0.25in
   :height: 0.23611in

.. [#] Only in case an Enterprise Agreement 1.0 (EA1.0) or Enterprise Support
   Agreement 2.0 (ESA2.0) are contractually ordered. More details available
   `here.
   <https://open-telekom-cloud.com/resource/blob/data/173450/d4fc9622cfbf9f188d9cdc2a1630b62c/open-telekom-cloud-flyer-enterprise-agreement.pdf>`__

.. [#] EIP is not part of the SLA within Enterprise Agreement 1.0 (EA1.0) or
   Enterprise Support Agreement 2.0 (ESA2.0)

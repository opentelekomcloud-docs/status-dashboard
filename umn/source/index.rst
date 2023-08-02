=============================================================
Status Dashboard for Open Telekom Cloud Services: User Manual
=============================================================

The Status Dashboard provides users with an easily accessible and
comprehensive overview of all services within the Open Telekom
Cloud. This user manual aims to guide users on how to access the
dashboard and understand the displayed data. The dashboard is
accessible through any standard web browser by visiting the following
URL: https://status.otc-service.com/.

Background
==========

The Status Dashboard aggregates data from multiple independent
monitoring sites ("zones") to present a comprehensive and real-time
overview of service statuses. In the event that the primary status
service fails, a redundant monitoring zone takes over automatically to
ensure continuous monitoring and uninterrupted service
availability.

The monitoring zones scan all services within predefined timeframes to
check for availability. These data points are aggregated, and any
deviation from expected behavior automatically triggers the creation
of an incident. A service manager is then notified, responsible for
promptly resolving the issue. Users can monitor the progress of
resolving incidents directly on the status dashboard.


Accessing the Dashboard
=======================

1. Open your preferred web browser.

2. Enter the following URL in the address bar:
   https://status.otc-service.com/

3. The Status Dashboard main page will load, providing an overview of
   all monitored environments.


Using the Dashboard
===================

The Status Dashboard serves as a comprehensive tool to monitor and
track the status of various services within the Open Telekom
Cloud. There are several controls to obtain a status overview and
additional information.

  

Tabs for Monitored Environments
-------------------------------

- Below the top bar, one or more tabs are available, each representing
  different monitored environments.

- Click on the desired tab to view the status of services within that
  specific environment.

Service Tiles
-------------

Users can quickly assess the health of services through the intuitive
visual representation of service state icons. In case of any issues or
incidents, the dashboard automatically triggers notifications to the
appropriate service manager, ensuring prompt resolution.

- Once you have selected an environment, all services within that
  environment will be displayed as tiles below the tabs.

- Services are grouped into categories such as computer, network,
  storage, etc.

- Each service's current state is indicated by a small icon on the
  tile.

Status Values
-------------

The meaning of the service state icons is as follows:

- Green: Denotes a fully operational service.
  
- Yellow: Indicates that a limited number of probing requests have
  failed, but the service remains available.
  
- Red: Represents an outage of the service.
  
- Blue: Denotes a planned maintenance event for the service.

A legend is provided below the main section, explaining the various
icons and additional symbols used in the service view.

Top Bar Navigation
------------------

To return to the main pages of the Status Dashboard from any section,
click on the T-Logo located on the top bar.

On the same bar there's a pull-down menu with extra functions:

- Access the user documentation by clicking on the "User Manual" link.

- Review the incident history.

- Find out about service availability in the past months.

- Access the Service Manager backend (authorized personnel only).

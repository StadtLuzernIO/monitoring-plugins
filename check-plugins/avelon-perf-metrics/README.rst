Check avelon-tickets
====================

Overview
--------

Retrieve the performance data of the various data points of your Avelon Cloud and present them in a readable format.

What is the Avelon Cloud?
Avelon's products and services have been used in professional building operations for over 20 years. From commercial and industrial buildings to office buildings, airports, and railway facilities. The Avelon Cloud propels buildings into a professional era. Avelon takes care of security and maintenance throughout the entire usage period. With Avelon Cloud, operations become cheaper and more professional.

Notes:

To use this monitoring plugin, you need to have a REST API license from Avelon.
If you already have a license, log in to Avelon and click on Settings in the user menu at the top right. On the General tab, you will see a section called Public OAuth API Key. The Client ID and Client Secret displayed there are required to authenticate with our API (Monitoring-Plugin).

Links:

* `Avelon <https://avelon.com>`_
* `Avelon Cloud Platform <https://avelon.cloud>`_
* `Avelon Documentation <https://avelon.cloud/docs>`_
* `API Documentation <https://avelon.cloud/swagger/swagger-ui/index.html?urls.primaryName=Public%20API#>`_


Fact Sheet
----------

.. csv-table::
    :widths: 30, 70
    
    "Check Plugin Download",                "https://github.com/Linuxfabrik/monitoring-plugins/tree/main/check-plugins/avelon-perf-metrics"
    "Check Interval Recommendation",        "Once a minute"
    "Can be called without parameters",     "No"
    "Compiled for",                         "Linux, Windows"


Help
----

.. code-block:: text

    usage: avelon-perf-metrics [-h] [-V] [--always-ok] --client-id CLIENT_ID --client-secret CLIENT_SECRET [--insecure]
                               [--no-proxy] --password PASSWORD --username USERNAME [--test TEST] [--timeout TIMEOUT]

    Retrieve the performance data of the various data points of your Avelon Cloud and present them in a readable format.

    optional arguments:
      -h, --help            show this help message and exit
      -V, --version         show program's version number and exit
      --always-ok           Always returns OK.
      --client-id CLIENT_ID
                            Avelon API client_id.
      --client-secret CLIENT_SECRET
                            Avelon API client_secret.
      --insecure            This option explicitly allows to perform "insecure" SSL connections. Default: False
      --no-proxy            Do not use a proxy.Default: False
      --password PASSWORD   Avelon Cloud password.
      --username USERNAME   Avelon Cloud username.
      --test TEST           For unit tests. Needs "path-to-stdout-file,path-t


Usage Examples
--------------

.. code-block:: bash

    ./avelon-tickets --client-id CLIENT_ID --client-secret CLIENT_SECRET --username USER --password PASSWORD

Output:

.. code-block:: text

    Sytem Name                      ! ID      ! Label                                     ! Value        
    --------------------------------+---------+-------------------------------------------+--------------
    HG-17-1.OG-0.253-SO01-DP101-XI1 ! 1389384 ! Differenzdruck Kaltwasser Vorlauf DP101   ! 0.4 bar
    HG-17-1.OG-0.253-SO01-DP201-XI1 ! 1389312 ! Netzdruck Kaltasser DP201                 ! 1.1 bar
    HG-17-1.OG-0.253-SO01-DP202-XI1 ! 1389284 ! Netzdruck Trinkwasser Vorlauf DP202       ! 7.3 bar
    HG-17-1.OG-0.253-SO01-DP301-XI1 ! 1389292 ! Differenzdruck Kaltwasser DP301           ! 0.5 bar
    HG-17-1.OG-0.253-SO01-P201-SS1  ! 1389397 ! Pumpe P201 Drehzahl                       ! 0.0 %
    HG-17-1.OG-0.253-SO01-P202-SS1  ! 1389403 ! Pumpe P202 Drehzahl                       ! 58.0 %
    HG-17-1.OG-0.253-SO01-SK101-RM1 ! 1389281 ! Regelventil SK101 Rückmeldung             ! 33.0 %
    HG-17-1.OG-0.253-SO01-SK101-SS1 ! 1389298 ! Regelventil SK101                         ! 35.0 %
    HG-17-1.OG-0.253-SO01-SK201-SS1 ! 1389424 ! Regelventil SK201                         ! 66.0 %
    HG-17-1.OG-0.253-SO01-TT101-XI1 ! 1389287 ! Vorlauftemperatur primär TT101            ! 11.1 °C
    HG-17-1.OG-0.253-SO01-TT102-XI1 ! 1389375 ! Rücklauftemperatur primär TT102           ! 21.2 °C
    HG-17-1.OG-0.253-SO01-TT201-XI1 ! 1389296 ! Vorlauftemperatur TT201                   ! 15.8 °C
    HG-17-1.OG-0.253-SO01-TT201-XS1 ! 1389307 ! Vorlauftemperatur TT201 Sollwert          ! 16.0 °C
    HG-17-1.OG-0.253-SO01-TT202-XI1 ! 1389295 ! Vorlauftemperatur TT202                   ! 16.1 °C
    HG-17-1.OG-0.253-SO01-TT203-XI1 ! 1389290 ! Rücklauftemperatur TT203                  ! 23.0 °C
    HG-17-1.OG-0.253-SO01-TT204-XI1 ! 1389362 ! Vorlauftemperatur Notkühlung TT204        ! 23.7 °C
    HG-17-1.OG-0.253-SO01-TT205-XI1 ! 1389286 ! Rücklauftemperatur Notkühlung TT205       ! 23.5 °C
    HG-17-1.OG-0.253-SO01-WZ101-PM1 ! 1389304 ! Energie Zähler WZ101 Leistung             ! 6.9 kW
    HG-17-1.OG-0.253-SO01-WZ101-QM1 ! 1389353 ! Energie Zähler WZ101 Durchfluss           ! 0.7 m³/h
    HG-17-1.OG-0.253-SO01-WZ101-TM1 ! 1389348 ! Energie Zähler WZ101 Vorlauftemperatur    ! 22.1 °C
    HG-17-1.OG-0.253-SO01-WZ101-TM2 ! 1389390 ! Energie Zähler WZ101 Rücklauftemperatur   ! 13.7 °C
    HG-17-1.OG-1.370-SO01-RT301-XI1 ! 1389343 ! Raumtemperatur WG RT301                   ! 28.7 °C
    HG-17-1.OG-1.370-SO01-RT301-XI2 ! 1389325 ! Raumfeuchte WG RT301                      ! 45.0 % rh
    HG-17-1.OG-1.370-SO01-RT302-XI1 ! 1389342 ! Raumtemperatur WG RT302                   ! 32.7 °C
    HG-17-1.OG-1.370-SO01-RT302-XI2 ! 1389329 ! Raumfeuchte WG RT302                      ! 39.0 % rh
    HG-17-1.OG-1.370-SO01-RT303-XI1 ! 1389387 ! Raumtemperatur KG RT303                   ! 23.1 °C


States
------

* Always returns OK.


Perfdata / Metrics
------------------

Performance data is collected from all data points. The name and type are generated based on the automatically read data points.:

.. csv-table::
    :widths: 25, 15, 60
    :header-rows: 1
    
    Name,                               Type,                   Description                                           
    <data_point systemName>,            <data_point value>,     This is a data point from the Avelon Cloud System.
    ...,                                ...,                    ...,


Credits, License
----------------

* Authors: `Linuxfabrik GmbH, Zurich <https://www.linuxfabrik.ch>`_
* License: The Unlicense, see `LICENSE file <https://unlicense.org/>`_.

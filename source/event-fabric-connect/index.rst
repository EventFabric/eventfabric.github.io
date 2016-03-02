Event Fabric Connect
====================

Event Fabric Connect is a standalone component you can download and run on your
own computer or on a server, it allows the consumption of events that are not
accessible from the internet or directly from the browser and for that reason
need to be sent to Event Fabric before they can be used.

.. note::

    Event Fabric Connect is currently in Beta, if you have any problem please
    contact us and we will help you solve your problem as soon as we can.

Requirements
------------

* Java Runtime 1.7 or higher

  + On windows visit `java.com <https://www.java.com/>`_ for installers

* Windows, Linux or Mac OS X
* A Modern Web Browser

  + Firefox
  + Chrome
  + Internet Explorer 11
  + Microsoft Edge
  + Safari

Installing
----------

The download is a zip file, just extract it's content on any folder.

Running
-------

On windows double click run.bat or run it from a command line tool.

On a unix like system you can run run.sh to run the server in the foreground or
use start-service.sh and stop-service.sh to run it as a service.

On successful execution it should display a message similar to::

    Starting with Configuration:
    {"server" {"host" "0.0.0.0", "port" 8081},
     "auth"
     {"username" "admin",
      "secret" "******",
      "password" "******",
      "token_duration_hours" 1}}

    Event Fabric Connect available from this machine at

    http://localhost:8081/index.html

    To access from another machine
    replace localhost for this machine's IP address or hostname

Now you can open the page http://localhost:8081/index.html to access Event Fabric Connect,
the default credentials are:

Username
    admin
Password
    secret

You can change them by editing the config.toml file with a text editor and
restarting Event Fabric Connect.

Usage
-----

You can see Event Fabric Connect being used to integrate several sources in this videos:

* `Event Fabric Connect Apache Kafka Support  <https://www.youtube.com/watch?v=4NBTJN_nGHk>`_
* `Event Fabric Business Dashboard Demo  <https://www.youtube.com/watch?v=rmiXV576Bio>`_ 
* `Event Fabric Connect Integration: SQL, MQTT, HTTP/JSON and IRC  <https://www.youtube.com/watch?v=OhQPF3vquCY>`_


Troubleshooting
---------------

If you have a problem using Event Fabric Connect please contact us via email
at info@event-fabric.com and we will help you solve it.

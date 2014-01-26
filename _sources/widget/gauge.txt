.. _gauge-widget:

Gauge
=====

.. figure:: ../../img/gauge.gif
   :align: center

Field Templates
---------------

Required
........

.. figure:: ../../img/gauge-fields-required.png
   :align: center

Optional
........

.. figure:: ../../img/gauge-fields-optional.png
   :align: center

Fields
------

Bold field names are required fields, others are optional.

.. table::

   ==========  =====    ======================================
   Field Name  Type     Description
   ==========  =====    ======================================
   **val**     Text     Value to define needle position
   **label**   Text     Text to display below the gauge
   color       Color    Background color
   ==========  =====    ======================================

Actions
-------

add
...

Increase the value identified by *label* by *val* or 1 if *val* isn't provided.

Useful to accumulate by an identifier.
    
substract
.........

Decrease the value identified by *label* by *val* or 1 if *val* isn't provided.

set
...

Set the value identified by *label* to *val* or 1 if *val* isn't provided.

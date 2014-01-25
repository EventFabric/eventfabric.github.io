.. _odometer-widget:

Odometer Widget
===============

.. figure:: ../../img/odometer.gif
   :align: center

Field Templates
---------------

Required
........

.. figure:: ../../img/odometer-fields-required.png
   :align: center

Optional
........

.. figure:: ../../img/odometer-fields-optional.png
   :align: center

Fields
------

Bold field names are required fields, others are optional.

.. table::

   ==========  =====    ======================================
   Field Name  Type     Description
   ==========  =====    ======================================
   **val**     Text     Value to use according to action
   **label**   Text     Text to display below the odometer
   color       Color    Background color
   action      Text     Name of the action, by default "set"
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

Library
-------

http://github.hubspot.com/odometer/

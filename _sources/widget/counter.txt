.. _counter-widget:

Counter Widget
==============

.. figure:: ../../img/counter-widget.png
   :align: center

Field Templates
---------------

.. figure:: ../../img/counter-fields.png
   :align: center

Fields
------

Bold field names are required fields, others are optional.

.. table::

   ==========  =====    ======================================
   Field Name  Type     Description
   ==========  =====    ======================================
   **val**     Text     Value to use according to action
   **label**   Text     Text to display below the counter
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


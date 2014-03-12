.. _bubble-widget:

Bubble Chart
============

.. figure:: ../../img/bubble.gif
   :align: center

Field Templates
---------------

Required
........

.. figure:: ../../img/bubble-fields-required.png
   :align: center

Optional
........

.. figure:: ../../img/bubble-fields-optional.png
   :align: center

Fields
------

Bold field names are required fields, others are optional.

.. table::

   ==========  ======    ======================================
   Field Name  Type      Description
   ==========  ======    ======================================
   **val**     Number    Size of the bubble (default 1)
   **label**   Text      Identifier for the serie of this value
   **x**       Number    X coordinate of the value
   **y**       Number    Y coordinate of the value
   color       Color     Bubble color
   action      Text      Name of the action, by default "set"
   ==========  ======    ======================================

Actions
-------

append
...

Add a bubble to the serie.
    
set
...

Set the value identified by *label* to *val* or 1 if *val* isn't provided.

remove
......

Removes the value identified by *label* from the displayed values.

Library
-------

http://www.humblesoftware.com/flotr2/

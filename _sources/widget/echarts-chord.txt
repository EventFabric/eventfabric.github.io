.. _echarts-chord-widget:

Chord Chart
===========

.. figure:: ../../img/echarts-chord.gif
   :align: center

Field Templates
---------------

Required
........

.. figure:: ../../img/echarts-fields-required.png
   :align: center

Optional
........

.. figure:: ../../img/echarts-fields-optional.png
   :align: center

Fields
------

Bold field names are required fields, others are optional.

.. table::

   ==========  ======    ==================================================
   Field Name  Type      Description
   ==========  ======    ==================================================
   **val**     Number    Weight of the current chord
   **from**    Text      Identifier for the category where the chord starts
   **to**      Text      Identifier for the category where the chord ends
   action      Text      Name of the action, by default "add"
   ==========  ======    ==================================================

Actions
-------

add
...

Increase the weight of the chord or connection by *val* or 1 if *val* isn't provided.

Useful to accumulate by an identifier.

substract
.........

Decrease the weight of the chord by *val* or 1 if *val* isn't provided.

set
...

Set the weight of the chord to *val* or 1 if *val* isn't provided.

remove
......

Removes the chord that connects *from* and *to*

Library
-------

http://echarts.baidu.com/index-en.html

.. _odometer-misc-widget:

Odometer
========

Required Fields
---------------

==========  =====    ======================================
Field Name  Type     Description
==========  =====    ======================================
val         Text     Value to use according to action
label       Text     Text to display below the value
==========  =====    ======================================

Optional Fields
---------------

==========  =====    ======================================
Field Name  Type     Description
==========  =====    ======================================
color       Color    Background color
action      Text     Name of the action, by default "set"
==========  =====    ======================================

Actions
-------

========== ======================================================
Action     Description
========== ======================================================
add        Add the value in **val** to the current amount
set        Set the value in **val** as the odometer value
substract  Substract the value in **val** from the current amount
========== ======================================================

.. youtube:: ZSkY-F-oGzA
    :width: 100%

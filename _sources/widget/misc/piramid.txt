.. _piramid-misc-widget:

Piramid
=======

Required Fields
---------------

==========  =====    ========================================================
Field Name  Type     Description
==========  =====    ========================================================
val         Text     Value to use according to action
label       Text     Identifier for the new entry
side        Text     Side to place the bar, can be "left" or "right"
serie       Text     Identifier for the serie where the bar will be displayed 
==========  =====    ========================================================

Optional Fields
---------------

==========  =====    ======================================
Field Name  Type     Description
==========  =====    ======================================
color       Color    Background color for bar
labelColor  Color    Color for the bar text
action      Text     Name of the action, by default "set"
==========  =====    ======================================

Actions
-------

========== ======================================================
Action     Description
========== ======================================================
add        Add the value in **val** to the current amount in bar
set        Set the value in **val** as the bar value
========== ======================================================

.. youtube:: z-1lA-xrALI
    :width: 100%

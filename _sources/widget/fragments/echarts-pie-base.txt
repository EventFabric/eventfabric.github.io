
Required Fields
---------------

==========  ======    ======================================
Field Name  Type      Description
==========  ======    ======================================
val         Number    Number to user for action
label       Text      Identifier for the label of this value
serie       Text      Identifier for the serie of this value
==========  ======    ======================================

Optional Fields
---------------

==========  ======    ======================================
Field Name  Type      Description
==========  ======    ======================================
color       Color     Background color
action      Text      Name of the action, by default "add"
==========  ======    ======================================

Actions
-------

========== ===================================================================
Action     Description
========== ===================================================================
add        Add the value in **val** to the current amount
set        Set the value in **val** as the odometer value
substract  Substract the value in **val** from the current amount
remove     Remove the value identified by *label* from the displayed values
========== ===================================================================


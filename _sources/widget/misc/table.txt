.. _table-misc-widget:

Table
=====

Required Fields
---------------

==========   ======    ======================================
Field Name   Type      Description
==========   ======    ======================================
val          List      List of columns for the row
label        Text      Identifier for the row
==========   ======    ======================================

Optional Fields
---------------

==========   =============    ======================================
Field Name   Type             Description
==========   =============    ======================================
color        Color or List    Background color
labelcolor   Color or List    Text color
==========   =============    ======================================

*color* and *labelColor* can either be a color (applies to the whole row) or a list of colors (one color for each column).

If a list of colors is specified leaving a column empty uses the default color
for that column.

.. youtube:: I0pPYluyP4A
    :width: 100%

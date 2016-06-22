.. _data-grid-widget:

Data Grid
=========

Required Fields
---------------

==========  ======    ========================================================
Field Name  Type      Description
==========  ======    ========================================================
val         Object    Object with fields configured in data-grid config
==========  ======    ========================================================

Optional Fields
---------------

==========  =====    ======================================
Field Name  Type     Description
==========  =====    ======================================
label       Text     Identifier for new row
color       Color    Background color for row
labelColor  Color    Color for row text
==========  =====    ======================================

If a new row has the same label as an existing one, the old one will be
replaced by the new one.

Widget Configuration
====================

Title
    Column title
Field Name
    Name of the field in the **val** object to get this column's content
Type
    Type of the column's content, the type will change how the value in val for
    this column is interpreted and displayed
Text Align
    Column alignment
Sort Direction
    Default sort direction for this column
Sort Priority
    Priority in sorting for this column, sorting will be done in order of
    priority, sorting first by columns with smaller numbers, and then by bigger
    ones
Size Proportion
    If all columns have size of 1 all have equal width, if one has 2 it will
    have twice the width as those with 1
Value Prefix
    Text to add before the value in the table cell
Value Suffix
    Text to add after the value in the table cell
Display Condition
    An expression describing a condition to indicate when this column should be
    displayed, if the condition is false then the column won't be displayed, if
    left empty it will be always displayed, example: '(min-width: 700px)

.. youtube:: Jr19_WXxze4
    :width: 100%

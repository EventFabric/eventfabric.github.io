.. _image-map-ol-widget:

Image Map
=========

Required Fields
---------------

==========   ======    ======================================
Field Name   Type      Description
==========   ======    ======================================
x            Number    X coordinate of the new entry
y            Number    Y coordinate of the new entry
type         Text      Type to place at location
==========   ======    ======================================

Valid Types
===========

The **type** field can be one of the following values:

shape
    draw a shape at the given coordinates
heat
    add a heat point in the heat map at the given coordinates
cluster
    add a cluster point in the cluster map at the given coordinates
icon
    add an icon at the given coordinates

Optional Fields
---------------

The following optional fields apply to all values of type.

==========   =============    ======================================
Field Name   Type             Description
==========   =============    ======================================
id           Text             identifier of current point
==========   =============    ======================================

If **id** is set in the current entry and there's already an entry with that
id, the old one will be replaced with this entry.

Optional Fields for Shape Type
------------------------------

==========   =============    ======================================
Field Name   Type             Description
==========   =============    ======================================
shape        Text             Type of shape to draw
==========   =============    ======================================

The **shape** field can be one of:

rectangle
    draw a rectangle at x,y. It requires two extra numeric fields **width** and **height**
circle
    draw a circle at x,y. It requires an extra numeric fields **radius**

Optional Fields for Heat Type
-----------------------------

==========   =============    ======================================
Field Name   Type             Description
==========   =============    ======================================
weight       Number           How "hot" is the current point
==========   =============    ======================================

Optional Fields for Icon Type
-----------------------------

==========   =============    ======================================
Field Name   Type             Description
==========   =============    ======================================
path         Text             Path to the icon to use
==========   =============    ======================================

Actions
-------

Actions will ignore the **type** field.

====================  =========================================================
Action 
====================  =========================================================
clear                 Clear all image map's content
clear-layer           Clear one layer's content
set-layer-visibility  Toggle one layer's visibility
====================  =========================================================

Clear Layer Action
..................

The **clear-layer** action requires a **layer** field to be set, it can contain
one of the following values:

shape
    clear shape layer
heat
    clear heat layer
cluster
    clear cluster layer
icon
    clear icon layer

Set Layer Visibility Action
...........................

The **set-layer-visibility** action requires a **layer** field to be set, see
previous section for valid values.

It also requires a **visible** field to be set to **true** or **false** depending
if you want to show (**true**) or hide (**false**) the layer.


.. youtube:: yCuHS52a2-M
    :width: 100%

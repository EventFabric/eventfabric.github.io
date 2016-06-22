.. _map-ol-widget:

Map
===

Required Fields
---------------

==========   ======    ======================================
Field Name   Type      Description
==========   ======    ======================================
lat          Number    Latitude coordinate of the new entry
lng          Number    Longitud coordinate of the new entry
==========   ======    ======================================

Optional Fields
---------------

===========  =============    ================================================
Field Name   Type             Description
===========  =============    ================================================
id           Text             Identifier of current point
label        Text             Label to display below the icon
description  Text             If set, when icon is clicked,
                              a dialog displaying description's content
                              will be displayed
icon         Text             Path to the icon to use
===========  =============    ================================================

If **id** is set in the current entry and there's already an entry with that
id, the old one will be replaced with this entry.

Actions
-------

====================  =========================================================
Action 
====================  =========================================================
clear                 Clear map's content
center                Center map at current coordinates
====================  =========================================================

.. youtube:: TKjwG91Eb8E
    :width: 100%

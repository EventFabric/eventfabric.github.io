.. _3d-globe-widget:

3D Globe
========

Required Fields
---------------

==========   ======    ======================================
Field Name   Type      Description
==========   ======    ======================================
lat          Number    Latitude coordinate of the new entry
lng          Number    Longitud coordinate of the new entry
val          Number    Size of the line at lat,lng
==========   ======    ======================================

Optional Fields
---------------

===========  =============    ================================================
Field Name   Type             Description
===========  =============    ================================================
label        Text             Identifier of current point
===========  =============    ================================================

If **label** is set in the current entry and there's already an entry with that
id, the old one will be replaced with this entry.

.. youtube:: YC8PFv8_vkc
    :width: 100%

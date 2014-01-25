.. _graph-widget:

Graph Widget
============

.. figure:: ../../img/graph-widget.png
   :align: center

Field Templates
---------------

.. figure:: ../../img/graph-fields.png
   :align: center

Fields
------

Bold field names are required fields, others are optional.

.. table::

   ==========  =====    ======================================
   Field Name  Type     Description
   ==========  =====    ======================================
   **val**     Text     Value to define needle position
   **label**   Text     Text to display below the graph
   color       Color    Background color
   ==========  =====    ======================================

=====
Graph
=====

The Graph widget allows modelling a graph and manipulating it by triggering
actions on the widget, actions allow to focus nodes, change attributes on
nodes, send values between them, and increase one of the four counters
available on each node.

First the graph must be built in the same way as it's done on the edit option
on a dashboard, then when ready right click on the widget title bar and select
"Save" to save the layout.

Actions
-------

change-node
...........

Change the attributes of node identified by *id* with the attributes and
values in *value*.

.. table::

   ==========  ======    ======================================
   Field Name  Type      Description
   ==========  ======    ======================================
   **id**      Text      Node identifier
   **value**   Object    Node attributes to change
   ==========  ======    ======================================

Possible keys and values for the *value* field:

.. table::

   ==================  ======    ======================================
   Field Name          Type      Description
   ==================  ======    ======================================
   **fill**            Text      Color to fill the shape
   **fill-opacity**    Number    Opacity of fill color from 0.0 to 1.0
   **stroke**          Text      Color for the shape's stroke
   **stroke-opacity**  Number    Opacity for the shape's stroke
   ==================  ======    ======================================

focus
.....

Focus the node identified by *id*.

.. table::

   ==========  ======    ======================================
   Field Name  Type      Description
   ==========  ======    ======================================
   **id**      Text      Node identifier
   ==========  ======    ======================================

send
....

Send *value* from the node identified by *id* until the last connected node or
just travel a number of *hops* if specified.

.. table::

   ==========  ======    ======================================
   Field Name  Type      Description
   ==========  ======    ======================================
   **id**      Text      Node identifier
   **value**   Any       Value to send
   hops        Number    Number of hops to travel
   ==========  ======    ======================================

incr
....

Increase bubble counter *cid* in node *id* by *value*.

available *cid* values are:

* top-left
* top-right
* bottom-left
* bottom-right

.. table::

   ==========  ======    ======================================
   Field Name  Type      Description
   ==========  ======    ======================================
   **id**      Text      Node identifier
   **cid**     Text      Bubble identifier
   **value**   Number    Amount to increment (default 1)
   ==========  ======    ======================================

.. _source-element:

Source
======

.. figure:: ../../img/source-element.png
   :align: center

A source is an element that makes events available to Event Fabric, at the moment
the supported sources are:

* Event Fabric Source
* Sample Source
* PubNub
* Firebase


Other sources will be added in the future via apps that can be activated when
needed per dashboard.

.. _source:

Event Fabric Source
-------------------

This can be considered the standard event source, to configure you have to
specify a channel and a username, after configuring, any event sent to that
channel and by that username will be emitted by that source element.

.. _samplesource:

Sample Event Source
-------------------

Used to generate events without an actual source, mainly to prototype a
dashboard or try something new.

.. _selected:

Event Selected
--------------

This source emits an event each time an event is clicked on a widget which
supports event selection (like news ticker, table etc.).


.. _selected-filter:

Event Selected with Filter
--------------------------

This source emits an event each time an event is clicked on a widget which
supports event selection (like news ticker, table etc.), before emitting the
event it filters the ones that are not in the filter list.

.. _pubnub:

PubNub
------

Receives events from a PubNub channel

http://www.pubnub.com/

.. table::

   ==================  =======  ==========================================================================
   Field Name          Type     Description
   ==================  =======  ==========================================================================
   **PubNub Channel**  Text     PubNub Channel
   **Use Auth Key**    Boolean  Use Auth Key?
   Auth Key            Text     Custom authentication token used by PAM
   Subscribe Key       Text     This key allows the client access to a data channel on the PubNub network.
   Publish Key         Text     This key allows access to sending data to a data channel.
   **SSL**             Boolean  Enable SSL?
   ==================  =======  ==========================================================================

.. _firebase:

Firebase
--------

Receives events from a Firebase channel

https://www.firebase.com/

.. table::

   =================  =====  ==========================================================
   Field Name         Type   Description
   =================  =====  ==========================================================
   **Firebase URL**   Text   URL that specifies the root of the data you want to access
   =================  =====  ==========================================================

.. _endpoint-element:

EndPoint
========

.. figure:: ../../img/endpoint-element.png
   :align: center


Sends an event to an external service

.. _endpoint:

Event Fabric
------------

Sends an event to Event Fabric backend

.. _pubnub:

PubNub
------

Sends an event to a PubNub endpoint

http://www.pubnub.com/

.. table::

   ==================  =======  ======================================
   Field Name          Type     Description
   ==================  =======  ======================================
   **PubNub Channel**  Text     Channel
   **Use Auth Key**    Boolean  Use Auth Key
   Auth Key            Text     Auth Key
   Subscribe Key       Text     Subscribe Key
   Publish Key         Text     Publish Key
   **SSL**             Boolean  SSL
   ==================  =======  ======================================

.. _firebase:

Firebase
--------

Sends an event to a Firebase endpoint

https://www.firebase.com/

.. table::

   =================  =====  ======================================
   Field Name         Type   Description
   =================  =====  ======================================
   **Firebase URL**   Text   URL that specifies the root of the data you want to access
   =================  =====  ======================================



.. _template-widget:

Template
========

.. figure:: ../../img/template.gif
   :align: center

The Template widget allows to display fields from an event on an HTML document
created using a visual editor, to configure just create any kind of document
you wish to display on the editor and insert placeholders for the values from
the event which will be replaced when a new event is received.

Placeholders
------------

Placeholders are inserted between curly brackets like this::

    The value of username is {username}

where {username} will be replaced by the username field from the received event.

Library
-------

http://akdubya.github.io/dustjs/

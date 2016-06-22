.. _template-misc-widget:

Template
========

The template widget allows to display fields from an event on an HTML document
created using a visual editor, to configure just create any kind of document
you wish to display on the editor and insert placeholders for the values from
the event which will be replaced when a new event is received.

Placeholders
------------

Placeholders are inserted between curly brackets like this::

    The value of username is {username} he is {details.age} years old

where {username}  will be replaced by the username field from the received
event and {details.age} will try to get the field **age** from the object
**details** and replace it in the document.

.. youtube:: P3iSl86CubE
    :width: 100%

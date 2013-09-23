.. _state-element:

State
=====

.. figure:: ../../img/loader-element.png
   :align: center

The state element loads a configured number of events from a set of specified
sources. When the dashboard loads, events are loaded, sorted by the time they
were originally received and sent to the connected elements.

This is done to "replay" events when the dashboard loads to fill it before
sources start receiving events.

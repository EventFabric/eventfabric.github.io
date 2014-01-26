.. _calendar-widget:

Calendar
========

.. figure:: ../../img/calendar.gif
   :align: center


Field Templates
---------------

Required
........

.. figure:: ../../img/calendar-fields-required.png
   :align: center

Optional
........

.. figure:: ../../img/calendar-fields-optional.png
   :align: center

Fields
------

Bold field names are required fields, others are optional.

.. table::

   ===============  ===========  ======================================
   Field Name       Type         Description
   ===============  ===========  ======================================
   **start**        Number       Timestamp when the event starts
   **label**        Text         Event description
   id               Number/Text  Event identifier
   end              Number       Timestamp when the event finalized
   allday           Boolean      True if the event lasts all day
   color            Color        Background color
   borderColor      Color        Border color
   textColor        Color        Text color
   action           Text         Name of the action, by default "add"
   ===============  ===========  ======================================

If the identifier is setted, a new event with the same identifier will replace the old one

Actions
-------

remove
......

Removes the event in the calendar identified by *id* from the displayed values.

Library
-------

http://arshaw.com/fullcalendar/

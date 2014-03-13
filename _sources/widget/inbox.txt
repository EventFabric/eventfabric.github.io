.. _inbox-widget:

Inbox
=====

.. figure:: ../../img/inbox.gif
   :align: center

Field Templates
---------------

.. figure:: ../../img/inbox-fields-1.png
   :align: center

.. figure:: ../../img/inbox-fields-2.png
   :align: center

.. figure:: ../../img/inbox-fields-3.png
   :align: center

Fields
------

Bold field names are required fields, others are optional.

.. table::

   ==========  =====    ============================================
   Field Name  Type     Description
   ==========  =====    ============================================
   **action**  Text     object the describes what to do with the row
   ==========  =====    ============================================

Actions
-------

append
......

Add a new row at the end of the inbox

.. table::

   ===========  ======  ============================================
   Field Name   Type    Description
   ===========  ======  ============================================
   *name*       Text    Name of the action: append
   *id*         Text    Row identifier
   title        Text    Text with the title of the row
   description  Text    Text with the description of the row
   date         Number  Timestamp with the date
   count        Number  Number of message with this description
   tags         List    List with tags for the row
   ===========  ======  ============================================

prepend
.......

Add a new row at the beginning of the inbox

.. table::

   ===========  ======  ============================================
   Field Name   Type    Description
   ===========  ======  ============================================
   *name*       Text    Name of the action: prepend
   *id*         Text    Row identifier
   title        Text    Text with the title of the row
   description  Text    Text with the description of the row
   date         Number  Timestamp with the date
   count        Number  Number of message with this description
   tags         List    List with tags for the row
   ===========  ======  ============================================

update
......

.. table::

   ===========  =====   ===============================================
   Field Name   Type    Description
   ===========  =====   ===============================================
   *name*       Text    Name of the action: update
   *field*      Text    Field to update(title, desc, date, count, tags)
   *id*         Text    Row identifier
   *value*      Text    New value for the field
   ===========  =====   ===============================================


remove
......

.. table::

   ===========  =====   ============================================
   Field Name   Type    Description
   ===========  =====   ============================================
   *name*       Text    Name of the action: remove
   *id*         Text    Row identifier
   ===========  =====   ============================================

sort
....

.. table::

   ===========  =======  ============================================
   Field Name   Type     Description
   ===========  =======  ============================================
   *name*       Text     Name of the action: sort
   *by*         Text     Field used to sort
   *ascending*  Boolean  Order ascending or descending
   ===========  =======  ============================================

mark
....

.. table::

   ===========  =======  ================================================
   Field Name   Type     Description
   ===========  =======  ================================================
   *name*       Text     Name of the action: mark
   *type*       Text     Type of mark(selected, unselected, read, unread)
   *id*         Text     Row identifier
   ===========  =======  ================================================

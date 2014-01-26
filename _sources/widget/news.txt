.. _news-widget:

News Ticker
===========

.. figure:: ../../img/news.gif
   :align: center

Field Templates
---------------

Required
........

.. figure:: ../../img/news-fields-required.png
   :align: center

Optional
........

.. figure:: ../../img/news-fields-optional.png
   :align: center

Fields
------

Bold field names are required fields, others are optional.

.. table::

   ==========  =====    ======================================
   Field Name  Type     Description
   ==========  =====    ======================================
   **val**     Text     Text to display as the new
   label       Text     Identifier for the new
   color       Color    Background color
   labelColor  Color    Color for the text font
   ==========  =====    ======================================

If two news are sent with the same label, the last one will replace the first one

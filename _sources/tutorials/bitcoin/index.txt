Bitcoin Dashboard Tutorial
==========================

We start by creating a new dashboard, selecting the **Create Dashboard**
action at the top right of the screen.

We give it a name (in my case "Bitcoin") and we select the apps that we want to
use, in this case we need the standard widgets and the firebase data source, so
we select "Widgets" and "Firebase Source".

.. figure:: ./img/demo-1.png
   :align: center

After the dashboard is created and we are in it, we go to the editor by selecting
the **Edit** action at the top right.

Now in the editor canvas we create a new Data Source by drag and drop of a Data
Source element.

.. figure:: ./img/demo-2.png
   :align: center

Once we have it we can give it a more descriptive name by selecting it and
clicking on its label.

With this action the label becomes a text entry and we can change it's name,
after which we press enter.

.. figure:: ./img/demo-3.png
   :align: center

After naming it we want to configure our first `firebase
<https://www.firebase.com/>`_ data source.

For this we select our source and click on it again or we right click on it.

This will display the actions we can do on it, in this case we select the
**Settings** action which is the leftmost option.

.. figure:: ./img/demo-4.png
   :align: center

This will display the settings dialog where first we need to select what kind of
data source we want to create, in our case we select the **Firebase** type and click **OK**.

.. figure:: ./img/demo-5.png
   :align: center

Now we have the firebase specific configuration, here we need to provide the
address of the object we want to watch for changed, in this case we want to
get the changes in the bitcoin prince, for this we use the public data set for
bitcoin that is located at https://publicdata-bitcoin.firebaseio.com/

We select **Wrap Data** option to wrap the received data in a standard Event
Fabric event and set **Channel** to bitcoin and **Username** to our username.

In type we have to select what type of changed are we listening to, in our case
we use the **value** type, details of what they mean are available at the
`firebase reference for the *on* method <https://www.firebase.com/docs/javascript/firebase/on.html>`_

After we finished configuring our data source we click **OK**.

.. figure:: ./img/demo-6.png
   :align: center

At this point it should get the first value of the object and signal it by
displaying a green bubble at the bottom right with a number representing how many
changes have been received by the data source.

.. figure:: ./img/demo-7.png
   :align: center

We can click on the bubble to see the received value, we can see in the value field
that it contains an object with three attributes (ask, bid, last) whose values
are text with those values (text is green and italic, numbers are blue and bold).

.. figure:: ./img/demo-8.png
   :align: center

Now we need to transform the received data to display it in some way in the dashboard,
for this we create a new **transformer** by drag and drop.

.. figure:: ./img/demo-9.png
   :align: center

We give it a name and open the actions menu to select the settings action.

.. figure:: ./img/demo-10.png
   :align: center

Almost all widgets need at least a **val** value available to know what to display,
for this we can go to the **Templates** section on the left panel, expand it and
select the **Set Value** section and then drag and drop the available template.

.. figure:: ./img/demo-11.png
   :align: center

The widget that we are going to use expects the label for the value in the **label** variable,
to create this block we do as before by expanding the **Templates** section and selecting the
**Set Label** Template.

.. figure:: ./img/demo-12.png
   :align: center

We then connect the two blocks together and change the values that they receive
by removing the right part and adding what we need.

In the case of **val** we need to transform the text representing the number to
an actual decimal number, for this we use the **to decimal** block available on
the **Text Section**.

The **to decimal** block expects an input which is of type text and produces a
decimal number as a result, the input will be the **ask** field inside the
**value** object, for this we use the **get value** block that looks for a field
inside the **value** object and we provide the name *ask* to that block.

For the **label** variable we create a text block and set the content of the text to *Ask*.

.. figure:: ./img/demo-13.png
   :align: center

Now that we have the source and the transformer we need to connect them, we do
this by opening the actions menu on the source and we select the **connect action**
after this we drag the connection and click on the target of the connection,
in this case the transformer.

.. figure:: ./img/demo-14.png
   :align: center

After this we have the two elements connected.

.. figure:: ./img/demo-15.png
   :align: center

We can wait for a new event to come in to see the events flowing or we can refresh
the browser to force at least the current value to flow through the connection.

.. figure:: ./img/demo-16.png
   :align: center

When the transformer received the event we can see two bubbles appearing, one
on the left for the received value and one on the right for the transformed
value, we click on the bubble on the right to see the result of the
transformation and at the bottom of the last event we can see our two fields
**val** and **label** with the correct content.

.. figure:: ./img/demo-17.png
   :align: center

But we still have to display this information in some widget, for this we
create a widget element and name it to *Ask Price*.

.. figure:: ./img/demo-18.png
   :align: center

We open the actions menu to configure it.

.. figure:: ./img/demo-19.png
   :align: center

Select **odometer** widget type and click **OK**.

.. figure:: ./img/demo-20.png
   :align: center

And leave settings by default and click **OK**.

.. figure:: ./img/demo-21.png
   :align: center

Now we connect the transformer to the widget as before.

Again, we can wait for a value change or we can refresh the browser to see the
last value flow to the widget.

.. figure:: ./img/demo-22.png
   :align: center

We can close the editor and see the odometer displaying the value.

.. figure:: ./img/demo-23.png
   :align: center

Now create a similar transformer for the bid value.

.. figure:: ./img/demo-24.png
   :align: center

Connect in the same way as before.

.. figure:: ./img/demo-25.png
   :align: center

Do the same for last value.

.. figure:: ./img/demo-26.png
   :align: center

Now we have three widgets displaying the three available values
.. figure:: ./img/demo-27.png
   :align: center
   :scale: 70%

Now we want to display the values over time, for this we create a new widget.

.. figure:: ./img/demo-28.png
   :align: center

Select the Chart widget type.

.. figure:: ./img/demo-29.png
   :align: center

Select the "Show Legend" option.

.. figure:: ./img/demo-30.png
   :align: center

Connect the three transformers to the chart widget.

.. figure:: ./img/demo-31.png
   :align: center

Wait for events of refresh to see the chart populating.

.. figure:: ./img/demo-32.png
   :align: center

Create a new widget.

.. figure:: ./img/demo-33.png
   :align: center

Select the **News Ticker** widget type.

.. figure:: ./img/demo-34.png
   :align: center

Select both options.

.. figure:: ./img/demo-35.png
   :align: center

Now to avoid having a mess of connections we will use the hub element, but
first we need to remove the connections to the chart widget, we do this by
clicking on the connection we want to remove and selecting the **Remove
Connection** icon.

.. figure:: ./img/demo-36.png
   :align: center

To clean up the connections disconnect all the connections to chart and create
a hub element. Then connect the three transformers to the hub and the hub to
the chart widget.

.. figure:: ./img/demo-37.png
   :align: center

Create a new transformer for the news ticker

.. figure:: ./img/demo-38.png
   :align: center

Now we need to set the **val** field to the text we want to display on the
news ticker widget, in this case we build a string by joining several pieces
of text, we use the markdown markup to make a piece of text bold by surrounding
it by two asterisks like this \*\*bold text\*\* results in **bold text**.

You can find more information about markdown in the `markdown syntax documentation <http://daringfireball.net/projects/markdown/syntax>`_

Finally we need to delete the **label** var since the news ticker works
differently if it's set (it replace the value with that label instead of adding
the value on top).

.. figure:: ./img/demo-40.png
   :align: center

Now we connect the hub to our transformer and the transformer to the news ticker.

.. figure:: ./img/demo-41.png
   :align: center

Close the editor to see the News Ticker populate either by waiting for a new
event or by refreshing.

.. figure:: ./img/demo-42.png
   :align: center
   :scale: 70%

Finally click the lock action at the bottom left to set the dashboard to read
only and we are done!

.. figure:: ./img/demo-43.png
   :align: center
   :scale: 70%


Slots
=====

Slots have a number of components that can be assigned to them.
Below is an example of a basic slot. 


.. code-block:: yaml

   '0': #Index to be placed at, starting at 0
     amount: 1 #Amount of item to place in the slot, if you just need one of the item this is optional 
     icon: "DIRT" #Icon for the slot

More complex example of a slot.

.. code-block:: yaml

   '0': #Index to be placed at, starting at 0
     icon: "DIRT" #Icon for the slot
     name: "&cDirt but red" #Name supports color codes
     lore: #Lore for the item
     - "&cThere is dirt in this slot"
     functions: #Functions to run on click
     - "broadcast: &fThis is a simple test"
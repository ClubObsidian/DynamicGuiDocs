Guis
=====

Guis like slots can have functions and failfunctions.
Below is an example of a gui.
If you do not know how any function works take a look at the `function documentation. <../functions>`_

.. code-block:: yaml

   gui-title: "&c&lTest GUI"
   rows: 5
   mode: "set" #Set will set items at the index, starting at 1
               #Where as 'add' will add items into the gui instead of setting at a specific index
   close: false #Whether or not slots will close the gui, false will not close the gui
   locations: 
   - "0,64,0,world" #Locations the gui can be clicked on in the world
   npc-ids:
   - '0' #Npc ids that the gui will be registered to
   alias:
   - "test" #Command aliases

   functions:
   - "permission: gui.test" #Permission needed to open the gui
   - "sound: LAVA,1.0,1.0" #Sound will be played if player has the permission

   permission-failfunctions:
   - "pmsg: &4You do not have access to this gui!" 
   #Player will be messaged if they do not have access
   #Any function can be used in this section
   #If any function fails in this area the functions will not continue
   #past the failed function

   '0':
     icon: "EXP_BOTTLE"
     name: "&6Level test"
     lore:
     - "&cYou have to have at least level 1337 for this to pass"
     functions:
     - "checklevel: 1337" #Checks to see if the user has 1337 exp
     - "broadcast: &cLevel check has passed, you have at least level 1337"
   '1':
     icon: "BEDROCK"
     name: "&fConsole command test"
     functions:
     - "executec: say Broadcasting from console, this test passed"
   '2':
     icon: "PAPER"
     name: "&fGui test"
     functions:
     - "gui: blank"
   '3':
     icon: "BARRIER"
     name: "&cClose Test"
     close: true #Since close is set to true, this will override the gui close setting
   '4':
     icon: "WORKBENCH"
     name: "&6Broadcast Test!"
     lore:
     - "Used for testing message broadcasting"
     functions:
     - "broadcast: &cBroadcast test is working!" #Broadcasts when clicked
   '5':
     icon: "STONE"
     name: "&4Set data test"
     functions:
     - "setdata: 1" #Sets the data to 1 when clicked
   '6':
     icon: "ENCHANTMENT_TABLE"
     name: "&bEnchanting test"
     functions:
     - "setenchants: DURABILITY,1" #Adds durability 1 to the item when clicked
   '7':
     icon: "REDSTONE"
     name: "&cName test"
     functions:
     - "setname: &fName test passed" #Sets the name of the item when clicked
     - "broadcast: Name test passed" #Broadcasts if the name was set
   '9':
     icon: "SAND"
     name: "&aRemove test"
     functions:
     - "removeslot: this" #Removes the item when clicked
     - "broadcast: &bRemove passed" #Broadcasts if the removal was successful
   '10':
     icon: "DIRT"
     name: "&aType test"
     functions:
     - "settype: GRASS" #Sets the item type to grass
     - "broadcast: &aType test passed" #Broadcasts if the item type was updated
   '11':
     icon: "DIAMOND_BLOCK"
     name: "&2Money Pay test"
     functions:
     - "moneywithdraw: 100"
     - "broadcast: &aPay test passed"
   '13':
     icon: "SAND"
     name: "&aRemove load test"
     load-functions: #Fuctions that happen on load, before the gui opens
     - "removeslot: this" #Removes this slot
     - "broadcast: &bRemove load test passed" #Broadcasts if successfully removed
     functions:
     - "broadcast: Why is this broadcasting, you got removed" #Function that can be ran if the slot does not get removed

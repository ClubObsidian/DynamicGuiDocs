Functions
=========

Functions are the building blocks for customizable guis in DynamicGui.
With functions you can customize `guis <../gui>`_ and `slots <../slot>`_.
Below are the built-in functions for DynamicGui, addons may add more.
If you are interested in making functions take a look at the `developer docs <../functionapi>`_.

=========
Broadcast
=========

The broadcast function is used to send a message to all players on the server.

Usage::

   broadcast: This is a test message!

Broadcasts the message "This is a test message!" to all players.

===========
Check Level
===========

Check a player's exp level.

Usage::

   checklevel: 1000 
   
The function would require the player to have level 1000.


==========================
Execute Command As Console
==========================

Executes a command for the player as console.

Usage::

   executec: say Hello from the server!

Executes the say command from console.


==========================
Execute Command As Player
==========================

Makes a player execute a command.

Usage::

   executep: spawn

Makes a player execute the spawn command.


========
Gui open
========

Makes a player open a gui.

Usage::

   gui: test

Makes a player open a gui named "test".


=============
No Permission
=============

Checks if a player does not have a permission.

Usage::

   nopermission: some.permission

Checks if the player does not have the permission "some.permission".


==============
Pay with money
==============

Allows a player to pay money.

Usage::

   pay: 1000

Makes the player pay 1000 if they have the balance avaliable.


==========
Permission
==========

Checks if the player has a permission.

Usage::
   
   permission: some.permission

Checks if the player has the permission "some.permission".


==============
Player Message
==============

Sends the player a message.

Usage::
   
   pmsg: Hello!
   
Sends the player the message "Hello!".


===========
Remove Slot
===========

Removes the current slot.

Usage::

   removeslot: this
 
Removes the slot from which the function is called.


=====================
Send player to server
=====================

Sends the player to a server.

Usage::

   send: testserver
   
Sends the player to the server "testserver".


================
Set data on slot
================

Set data on the current slot, can be used in 1.12 and below.

Usage::

   setdata: 1
   
Sets the data value of the current slot to 1.


====================
Set enchants on slot
====================

Sets enchants on the current slot.




================
Set lore on slot
================



================
Set name on slot
================



================
Set type on slot
================



=====
Sound
=====



=========
Statistic
=========



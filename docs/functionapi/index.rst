Function Api
============

The function manager is what is responsible for the registration of functions. Below you will find out how to write functions and add the functions to the function manager so they can be used in guis.

As a note any built-in functions should be platform independent, if you want more information on this see the `implementing a server type documentation. <../server>`_ This does not apply to addon plugins.


=================
Making a function
=================

All functions have to extend the Function class. The function class allows you to work with the player and manipulate guis.

Below is an example of a simple function that... todo


===============
Function owners
===============

Most functions do not need to worry about the owner of the function. However there are certain operations where it would be useful to know the owner of the function. In DynamicGui function owners are split up slots and guis. Slots refer to the individual slots in a gui and a gui is the whole gui including the slots that make up the gui.


===========================
Making a slot only function
===========================

Slot functions are slot only and are to be used if a functions can only interact with a slot.


==========================
Making a gui only function
==========================

Gui functions are gui only and can be used if a function needs to manipulate the gui on creation and on opening.


=================
Adding a function
=================




Remote Guis
===========

Remote guis are treated the same as regular guis but are loaded from a remote location, e.g. a webserver. These guis
have to be specified in the config.yml under the "remote-guis" section. If the location of a remote
gui cannot be resolved on runtime then an older backup of the file will be loaded. Below is an example
of a remote gui being loaded from Github.

.. code-block:: yaml

   remote-guis:
     remote: #Remote identifier
       file-name: "remote.yml" #File name
       url: "https://raw.githubusercontent.com/ClubObsidian/DynamicGUIExamples/master/examples/remote.yml"
Setting up Home Assistant
=========================

.. _hainstallation:

Installing Home Assistant Container
-----------------------------------

.. code:: bash

   docker run -d \
   --name homeassistant \
   --privileged \
   --restart=unless-stopped \
   -e TZ=Europe/Brussels \
   -v /<PATH_TO_YOUR_CONFIG>:/config \
   --network=host \
   ghcr.io/home-assistant/home-assistant:stable


*<PATH_TO_YOUR_CONFIG>* points at the folder where you want to store your configuration.

.. _haexposingdevices:

Exposing devices
----------------

In order to use Zigbee or other integrations that require access to devices, you need to map the appropriate device into the container.

.. code:: bash

   docker run ... --device /dev/ttyUSB0:/dev/ttyUSB0 ...

Accessing Home Assistant
------------------------

Once the Home Assistant Container is running, Home Assistant should be accessible using **http://<hostname-or-hostipv4>:8123** (replace with the hostname or IP of the system).

.. autosummary::
   :toctree: generated

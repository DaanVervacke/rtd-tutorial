Setting up Home Assistant
=========================

.. _hainstallation:

Installing Home Assistant Container
-----------------------------------

Open up your favourite terminal and enter the following command:

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

The default webportal port is 8123. Specify ``--publish 8123:<YOUR_PREFERRED_PORT>`` to use a custom port.

.. _haexposingdevices:

Exposing devices
----------------

In order to use Zigbee or other integrations that require access to devices, you need to map the appropriate device into the container.

.. code:: bash

   docker run ... --device /dev/ttyUSB0:/dev/ttyUSB0 ...

Accessing Home Assistant
------------------------

Once the Home Assistant Container is running, Home Assistant should be accessible using **http://<HOSTNAME_OR_IP>:<YOUR_PREFERRED_PORT>** (replace with the hostname/IP of the system and your preferred port, 8123 by default).

.. autosummary::
   :toctree: generated

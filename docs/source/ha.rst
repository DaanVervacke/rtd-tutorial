Setting up Home Assistant
=========================

.. _haintroduction:

Installing Home Assistant Container
-----------------------------------

.. note::

   <PATH_TO_YOUR_CONFIG> points at the folder where you want to store your configuration.

.. code:: bash

   docker run -d \
   --name homeassistant \
   --privileged \
   --restart=unless-stopped \
   -e TZ=Europe/Brussels \
   -v /<PATH_TO_YOUR_CONFIG>:/config \
   --network=host \
   ghcr.io/home-assistant/home-assistant:stable


Once the Home Assistant Container is running Home Assistant should be accessible using http://<host>:8123 (replace with the hostname or IP of the system).

.. autosummary::
   :toctree: generated

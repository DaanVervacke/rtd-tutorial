Setting up ESPHome
=========================

.. _esphomeinstallation:

Installing ESPHome Container
----------------------------

Open up your favourite terminal. We'll start by pulling the ESPHome Docker image.

.. code:: bash

   docker pull ghcr.io/esphome/esphome

Connect your ESP32/ESP8266 to your device via USB.

Now let’s setup a configuration file. 
Fortunately, ESPHome has a friendly setup wizard that will guide you through creating your first configuration file. 
For example, if you want to create a configuration file called ``myfirstconfig.yaml``:

.. code:: bash

   docker run \
   --rm \
   -v "${PWD}":/config \
   -it ghcr.io/esphome/esphome \
   wizard \
   myfirstconfig.yaml

.. _esphomeconfiguration:

Configure ESPHome
-----------------

If all goes well you'll be greated by this screen:

.. image:: images/esphome_intro.png
   :alt: ESPHome intro

Let's go over each step.

1. Choose a name for your ESPHome node, we'll go with *myfirstnode*
   
   .. image:: images/esphome_step1.png

2. Pick your microcontroller model, in our case: *ESP32*.

   .. image:: images/esphome_step2.png

3. Pick your board, if you're unsure about your boardtype please consult the following page:
   https://docs.platformio.org/en/latest/platforms/espressif32.html#boards

   

.. autosummary::
   :toctree: generated

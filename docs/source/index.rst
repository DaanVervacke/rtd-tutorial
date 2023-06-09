Home Assistant, ESPHome & Pyscript
==================================

.. _mainintroduction:

Introduction
------------

These docs will explain how to set-up a Home Assistant instance with seamless support for:

- ESP32 & ESP8266 microcontrollers
- Python scripts

This will allow us to:

- Configure ESP8266/ESP32 microcontrollers by simple yet powerful configuration files and control them remotely through Home Assistant.
- Write Python functions and scripts that can implement a wide range of Home Assistant automation, logic and triggers.  

This guide requires basic knowledge about:

- Linux & Bash
- `Docker <https://www.docker.com/>`_
- `Home Assistant <https://www.home-assistant.io/>`_
- ESP32 GPIO pins

.. note::

   This guide assumes that you already have an operating system setup and a container runtime installed (like Docker).

.. _mainconnections:

Connections
-----------

The goal of this guide is to create a simple game (Simon Says) that utilizes HA, our ESP32 and some Philips Hue lights.
Please check out the full schematic below.

.. image:: images/connections.png

It's recommend to follow the table of contents order, **step by step**.

.. _maincontents:

Contents
--------

.. toctree::

   ha
   esphome
   pyscript

.. note::

   This project is under active development.

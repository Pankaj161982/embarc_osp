.. _example_sec_mbedtls_dtls_server:

FreeRTOS mbed TLS Example: DTLS Server
######################################

Overview
********

This example takes reference from mbedtls **dtls_server** to test dtls client functionality.


Detailed Description
====================

* Extra Required Tools

* Extra Required Peripherals

    - Digilent PMOD WIFI(MRF24WG0MA)
    - SD Card to store certification file, key file

.. note::
   EMSDP has board WiFi module, no need to use PMOD WiFI.

.. note::
   The memory footprint of this example is larger then
   the default configuration of |iotdk|. Without optimization ,this example doesnot support |iotdk|


Buidling and Running
********************

1. Before building this example, it's required to get the mbedtls code and apply specific patch through the ``apply_embarc_patch.sh`` by the following commands

.. code-block:: console

   cd <embarc_root>/middleware/mbedtls
   sh apply_embarc_patch.sh


2. Copy the ``tests`` dir in ``middleware/mbedtls`` into the SD card of secure server node, it will load CA file and key file.

3. When initialization finished and network connected, run **main** in ntshell, it will try to do dtls communication.

4. In pc node or mbedtls dtls_client node, run the client application to connect to the server node.

Sample Output
=============

.. code-block:: console
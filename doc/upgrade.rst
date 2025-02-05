Upgrading with nRF Connect for Mobile
######################################

Prepare your device for DFU by replacing the existing
bootloader with the one that uses your public key.

-  Build a new bootloader by compiling the Bootloader project using
   either Keil μVision or GCC.

-  Program the compiled bootloader onto the device. Remember to program
   the **Soft Device** as well for the OTA-DFU to function properly.

-  Copy the `public_key.c` file to
   `<InstallFolder>\\project\\bootloader_secure\\dfu_public_key.c`.

The following procedure requires a phone or tablet with `nRF
Connect for mobile`_ installed to run DFU.

1. Transfer the zip package that will be used for DFU to your phone.

2. Power on the device and open nRF Connect on your phone.

3. Tap **Scan** and select your device from the list
   of discovered devices.

.. note::
    The discovered devices list is not automatically refreshed when they
    stop advertising. If you have problems connecting to a device from
    the list, refresh the list.

.. image:: images/image3.png
   :width: 1.84in
   :height: 3.28in
   :align: center

Activating DFU mode
--------------------

4. Expand the Secure DFU Service section. There are two icons to the
   right of the DUF Control Point area.

   a. Tap the icon to the right to turn notifications on/off.

   b. Tap the icon to the left to enable bootloader (DFU)
      mode. Tap **OK** when prompted to reset the device.

.. note::
    The device now enters DFU mode. Go to the **Scanner** tab and start
    scanning. A device with the same name but “DFU” added appears in the list of
    discovered devices.

.. list-table::
    :widths: 50 50

    * - |image1|
      - |image2|

Running DFU
------------

4. Connect to the new device by tapping the DFU icon.

Uploading the ZIP file
=======================

5. Select **Distribution packet (ZIP)** and navigate to the package that
   you uploaded earlier.

.. image:: images/image4.png
   :width: 1.88in
   :height: 3.36in
   :align: center

6. The package is now uploaded to the device

.. |image1| image:: images/image1.png
   :width: 1.86in
   :height: 3.31in
   :align: middle

.. |image2| image:: images/image2.png
   :width: 1.87in
   :height: 3.33in
   :align: middle

.. _nRF Connect for mobile: https://www.nordicsemi.com/eng/Products/Nordic-mobile-Apps/nRF-Connect-for-mobile-previously-called-nRF-Master-Control-Panel
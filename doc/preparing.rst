.. _preparing:

Preparing for OTA-DFU
#####################

The following procedures assume that you want to update the device with your own custom firmware.
To do this, you must complete the following steps:

1. Generate your own public and private key pair.
#. Generate a device firmware update (DFU) package that is signed with your key and contains your custom firmware.

To complete these steps, you require `nRF Util <https://github.com/NordicSemiconductor/pc-nrfutil>`_.

Generating a key pair
*********************

Cryptographic keys are required to sign and validate a DFU package.
Before generating your custom DFU package, you must generate your own private-public key pair.

To generate a new private key, run the following command with nrfutil installed::

  nrfutil keys generate private-key.pem

The command generates a new key file in the folder where you ran the command.
Make sure you keep this key secret.

Now, generate a public key from the private one::

  nrfutil keys display --key pk --format code private-key.pem --out_file dfu_public_key.c

Generating a DFU package
************************

Run ``nrfutil pkg generate`` to generate a zip file that you can later use to update the device firmware.
You can find detailed information about the command in the `nRF Util documentation <https://infocenter.nordicsemi.com/topic/ug_nrfutil/UG/nrfutil/nrfutil_pkg.html>`_.
For example, enter the following command::

  nrfutil pkg generate --application <path_to_hex_file> --application-version 0 --hw-version 52 --sd-req 0x98 --key-file private-key.pem dfu-app.zip

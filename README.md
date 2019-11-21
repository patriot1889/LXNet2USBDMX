# Qlab2USBDMX

Qlab2USBDMX is a small utility that bridges the gap between Art-Net and an OpenDMX/uDMX USB interface, specifically for Qlab.

## Download
https://github.com/patriot1889/LXNet2USBDMX/releases

## Qlab settings
For Qlab2USBDMX to work correctly, the _Use broadcast mode for Art-Net lighting_ setting must be enabled. The _Art-Net Lighting Network Interface_ must also be set to _Automatic_. (https://qlab.app/docs/v4/general/qlab-preferences/)

## Usage
Upon launch, an ArtNet socket is created, the relays to OpenDMX and/or uDMX are started providing the correct drivers are installed and the devices are present.

After that, Qlab is launched. It is advised to use Qlab2USBDMX as a launcher for Qlab if you are wanting to use the OpenDMX or uDMX interfaces. This ensures that the ArtNet socket is live before Qlab loads. If Qlab is already open when you open Qlab2USBDMX, you must visit the _QLab Preferences..._ panel and change the _Art-Net Lighting Network Interface_ to _Automatic_. If _Automatic_ is already selected then select a different interface and then re-select _Automatic_.

This application is not intended to replace the officially compatible DMX interfaces for Qlab. This application comes with no warranties and is therefore used at your own risk.

Qlab2USBDMX was developed as a quick fix to enable such interfaces to work with Qlab at short notice - potentially saving a show, or to provide a way to test DMX output with cheaper interfaces. Of course, feel free to use it as you wish but it is always recommended to use officially supported interfaces in show critical conditions.

### OpenDMX
OpenDMX USB widgets are available from ENTTEC. An OpenDMX widget is a USB-to-Serial-to-EIA-485 converter.
You can make your own using an FTDI "Friend" such as this one from Adafruit and a MAXIM 481 driver IC.

The OpenDMX USB interface requires an FTDI D2XX driver (http://www.ftdichip.com/Drivers/D2XX.htm).
To use the D2XX driver with the most recent versions of OSX, it is also necessary to install D2XXHelper (https://www.ftdichip.com/Drivers/D2XX/MacOSX/D2xxHelper_v2.0.0.pkg).
Qlab2USBDMX requires d2xx 1.4.16.

### uDMX
uDMX USB tiny bus powered interfaces are available from https://www.anyma.ch/research/udmx/

The uDMX USB interface requires libusb-compat to be installed. See https://www.anyma.ch/libusb-compat/


#### Credits
This application is heavily based on LXNet2USBDMX from Claude Heintz.
https://www.claudeheintzdesign.com/lx/lxnet2opendmx_about.html


Figure 53 and QLab are registered trademarks of Figure 53 LLC.

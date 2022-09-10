# Out of the box

## Inventory

1) The hub with RaspberryPi4 and micro-SD (uSD) card inserted
2) One (1) USB-C power-adapter (USA 120V)
4) One (1) USB-C to USB-C cord 
5) One (1) 10ft Ethernet cable 
6) One (1) USB to micro-USB cable to charge the motion detectors
7) Two (2) Shelly motion detectors
8) One (1) Shelly humditity and temperature sensor
9) One (1) Shelly moisture sensor
10) One (1) Shelly gas sensor
11) Three (3) Lithium-Ion batteries; 1 for H&T, 1 for Flood; 1 spare
12) Two (2) pair (4 total) Command(tm) adhesive strips for motion sensors

## Setup sensors

**Download the Shelly app** for Apple [iOS](https://apps.apple.com/us/app/shelly-cloud) or Google [Android](https://play.google.com/store/apps/details?id=allterco.bg.shelly).

The Shelly Motion sensors may require charging before they can be added to the Wifi network, etc.  The USB to micro-USB cable provided may be plugged into any standard charger for smartphone, .. or may be plugged into the rear of the hub.  USB ports closest to the Ethernet port are USB-3 and should have power.

The Shelly Flood and H&T sensors require batteries (included); refer to the device documentation, but the flood sensor opens with a slight counter-clockwise turn between the top and bottom; it is similar for the H&T sensor.  Both sensors have small buttons to enable, for example if the sensor goes to sleep.

The spare battery may be required for the H&T sensor which appears to draw more energy than anticipated (or documented).

All Shelly sensors are “included” to the Wifi network using the Shelly app on your smartphone.  Refer to the Shelly documentation.

Included devices may be accessed in the Shelly app through the 

## Setup hub

1. Remove hub from box and remove wrapping; there is a plastic sleeve with a SD-to-uSD converter card with uSD card inside
2. Remove uSD card from converter/carrier and insert into slot on front of hub; refer to documentation for enclosure inside box for uSD card placement
3. Remove power-supply from box and remove wrapping; insert one end of USB-C cable into power-supply
4. Insert Ethernet cable into rear of hub
5. Insert other end of ethernet cable into switch or router.
6. Plug-in power-supply to 120V socket
7. Plug other end of USB-C cable into rear of enclosure
8. Press hub power-on button on rear of enclosure

Wait for approximately 20 minutes and then launch Home Assistant app on your smartphone.

If you have previously installed the app, select the orange gear in the lower right corner when the app starts; then select the Debug option at the end and select Reset.

When the app starts (or has been reset), it will search the network for the hub; by default the hub is named “homeassistant” on the local network, e.g. [http://homeassistant.local:8123/](http://homeassistant.local:8123/) is the default Web address (n.b. 8123 is the port number).

After the app has scanned the network and found your local hub you will be able to configure the app to access the smartphone information as well as enable notifications and then create the Owner account (i.e. “independent adult”) by providing a name (e.g. “Karen Martin”) and then a password if the automated default login name is acceptable.

Refer to the [HOMEASSISTANT.md](https://github.com/ageathome/core/blob/main/docs/HOMEASSISTANT.md) guide.

Once these steps are complete you should be able to access the basic installation of Home-Assistant on the local network using the Owner account, i.e login name and password.

The Owner account should be customized to enable “Advanced Mode” — this mode enables specifying automatics updates; customizations are accessed through the last panel item which should be the Owner name (e.g. “Karen Martin” with default icon of “KM”).

# Installation

The Age@Home software is packaged as a Home-Assistant add-on; these add-ons are provided through an Add-on Store that is accessed through the Settings panel item on the left.

## Hub

Refer to the [QUICKSTART.md](https://github.com/ageathome/core/blob/main/docs/QUICKSTART.md)

The Settings view lists multiple items; select the Add-ons item which will lead to a page listing all installed add-ons.

If no add-ons are installed a link to the Add-on Store is provided at the top-left; alternatively the store may be accessed through the button in the lower-right.

The add-ons listed in the store are cataloged by software repositories on the Internet; the Age@Home repository is located at “http://github.com/ageathome/addons” and contains a single entry for the Age@Home add-on.

NOTE: After adding the repository the browser session requires a refresh, which may require a re-login to the Owner account.

The add-on should then be installed by selecting the add-on in the Settings:Addons listing.  This will display the add-on, indicating operational status and four options.  The option for automatic updates is shown only if “Advanced Mode” has been enabled for the Owner.

Start on boot, Watchdog, and Automatic updates should be enabled; the add-on panel item may be enabled, but currently provides very limited functionality for testing.

Configuration options not required, but will probably be required at some point (e.g. external system monitoring).

Start the add-on; the system will reboot oncel download and setup of the Age@Home software is completed; expect 30-60 minutes depending on Internet connection.

After the system has restarted you will be able to use smartphone app with the Owner user name and password.

Setup will have identified missing sensors and provide appropriate local notifications.


## Sensors

Once the four sensors (2x motion, 1 H&T, 1 flood) have been added to the WiFi network using the Shelly smartphone app those sensors may then be added to Age@Home.

Select the Settings panel item and then Devices & Services from the available settings.  Select the discovered Shelly sensors or select the Add Integration button and then enter “Shelly” which should display any discovered Shelly sensors.

If the H&T or Flood (aka “moisture”) sensors are not found the small button inside should be pushed to wake-up the sensor; a small red light will flash on the sensor when it is awake.  Repeating the Add Integration step may be required.

Similarly, the Motion sensor may require awakening; it has two small holes on the bottom on either side of the micro-USB port — there is a rubber cover for this area which may need to be removed; one hole provides a light and the other a recessed switch which may be depressed using a pin or paperclip.

Pressing the Shelly Motion recessed button one time will wake it up; 5 times will make it reboot; and 15 times will reset to factory (IIRC, check included sensor manual).

Once devices have been integrated into the system they may be placed in appropriate locations; it is recommended to awaken each sensor in its desired area prior to final installation, e.g. single press of recenssed button on motion sensor prior to attaching to wall.

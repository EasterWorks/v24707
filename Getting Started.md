First:
The very first thing you will need to do is connect the printer to your own network. If you do not have an ethernet drop available for the printer, then you'll need to edit the wpa-supplicant.conf file on the Raspberry Pi's MicroSD card via the following:
- With the printer powered off, flip the printer over and open the electronics bay.
- Locate the Raspberry Pi installed in the electronics bay and remove the MicroSD card.
- Insert the MicroSD card into your computer (you will likely need a USB adapter).
- Open the MicroSD card and search for the file named "wpa_supplicant.conf".
- Edit the lines where "SSID" and "PSK" are to match your WiFi SSID and the password for it. Ideally, use a dedicated 2.4ghz WiFi network.
- Re-insert the MicroSD card into the Raspberry Pi, close it up, and power it on.
- Wait ~3-5 minutes for the Raspberry Pi to fully boot and connect to the network.

Second:
After connecting the printer to your network, you will need to find the IP address.
- In your web browser, navigate to your router/modem's interface (this will often be https://192.168.0.1).
- Look for the list of connected devices. One of them should say Mainsail, RaspberryPi, Klipper, or Voron.
- You may also be able to navigate directly to the printer's web console at http://mainsailos.local/.

Third:
The Raspberry Pi installed in this printer has the default password "raspberry". You should change this as soon as you're able to navigate to the printer's web console via the following:
- Download an application to your computer called PuttySSH.
- Enter the printer's web console address (obtained in step 2) for the connection properties and connect.
- Sign in with the following credentials: 
- Username: pi
- Password: raspberry
- Run the following command (re-enter the password above if prompted): sudo passwd
- Enter the password you would like to use moving forward. Make sure you document this password for future needs!

With the above steps complete, the printer is now fully ready to use on your network. You can upload prints to the printer and control its functions via the printer's web interface, or via web integration in your slicer of choice (for example, OrcaSlicer).

Before continuing with your first print, please see the folder "Slicer Configuration".


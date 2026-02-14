Display stats on the MiniPTFT 135x240 from Adafruit Industries on the Raspberry Pi (see https://www.adafruit.com/product/4393).

A modification of https://github.com/adafruit/Adafruit_CircuitPython_RGB_Display/blob/main/examples/rgb_display_minipitftstats.py now that "getsize" seems to have been removed from the Pillow library.

The rest of the setup can be found in https://learn.adafruit.com/adafruit-mini-pitft-135x240-color-tft-add-on-for-raspberry-pi/python-setup, this is just a script to display some basic stats.

To get this to work reliably at boot I had to call it via crontab "crontab -e", then add in:
@reboot sleep 10 && /home/username/stats.py


(where/home/username/stats.py is the full path to the script)

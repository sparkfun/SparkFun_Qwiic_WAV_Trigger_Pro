



## MIDI Host Firmware

Running the WAV Trigger Pro as a MIDI USB Host requires uploading new firmware. You can upload new firmware to the board over USB, USB-to-Serial converter like the [Serial Basic]() connected to the serial PTH pins, or with an STLink debugger and the JTAG header. We strongly recommend uploading over USB since all you need is a USB-C cable, closing the BOOT jumper/tying BOOT to GND, and a computer with the STM32 Cube Programmer software. This guide only covers uploading new firmware over USB-C.

Start by downloading the correct version of STM32 from [this page](https://www.st.com/en/development-tools/stm32cubeprog.html). Note, downloading does require submitting a valid e-mail and clicking a confirmation link sent to that e-mail. Once downloaded, follow the installation instructions and then open Cube Programmer and you should be greeted by a screen similar to the image below:

**Screenshot of cube programmer - Mark L**

You'll also need the USB MIDI Host Firmware, you can download that from the [GitHub repository]() or from robertsonics' [downloads page](). Take note of the file location as you'll need to point the Cube Programmer software to that location.

### BOOT Jumper

Prior to connecting the WAV Trigger Pro, close the BOOT PTH jumper (either using headers and a jumper connector/jumper wire or simply temporarily pulling BOOT to GND) to set the STM32 into BOOT Mode. The board should stay in BOOT mode until reset or power cycle.

### Upload New Firmware

With the board in BOOT mode, return to the Cube Programmer software and switch to the "Erasing & Programming" view by clicking the second icon on the left side of the window. Next, either enter the filepath for the new firmware or click "Browse" to naivgate to the new firmware file. On the right side of the window, select "USB" on the drop-down menu for programmer type. The USB port <i>should</i> automatically detect which port the WAV Trigger is on but if not, click the refresh button and manually select the port, then click "Connect".

Make sure everything is configured properly and then click "Start Programming" to begin uploading the new firmware. This should take only a few seconds and once it's complete, disconnect the BOOT jumper (if needed) and press the RESET button. The WAV Trigger Pro should now appear as a USB audio device **Verify w/Firmware - Mark L**.

## Hardware Adjustments

Now we need to adjust the HST/DEV solder jumpers to configure the board to act as a USB Host. Locate these jumpers on the underside of the board and sever the trace connecting the "Center" and "Right" pads and then carefully solder the "Center" and "Left" pads together. After adjusting these jumpers your board should look similar to the photo below:



Next, prepare to connect the power supply for the MIDI assembly by either soldering wires directly to the <b>5V</b> and <b>GND</b> pins or soldering headers to these pins for a removeable power connection. 

## Completed Assembly


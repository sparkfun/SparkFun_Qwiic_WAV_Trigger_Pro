



The Qwiic WAV Trigger Pro can be controlled over a Qwiic (I<sup>2</sup>C) connection with a development board using the WAV Trigger Pro Qwiic Arduino Library. The Qwiic interface works with the WAV Trigger Pro in both MIDI Device (default) or MIDI Host. 

## Qwiic Assembly

Using the WAV Trigger Pro over Qwiic is simple as it just requires a connection to a Qwiic-enabled development board using a Qwiic cable. If your preferred development board does not have a Qwiic connector, you can use this [Qwiic breadboard adapter cable](https://www.sparkfun.com/products/17912) to connect to the I<sup>2</sup>C bus.

The first example in the Qwiic WAV Trigger Pro Arduino Library sets up four I/O pins on a connected Arduino development board (in this case, the [RedBoard Artemis](https://www.sparkfun.com/products/15444)) so we've wired up four push-buttons on a breadboard connected to I/O pins 4 through 7:

<figure markdown>
[![Photo of Qwiic assembly.](./assets/img/WAV_Trigger_Pro-Qwiic_Assembly.jpg){ width="600"}](./assets/img/WAV_Trigger_Pro-Qwiic_Assembly.jpg "Click to enlarge")
</figure>

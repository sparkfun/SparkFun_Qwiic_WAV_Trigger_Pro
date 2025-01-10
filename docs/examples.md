---
icon: simple/arduino
---

## Required SD Image

The examples included in the WAV Trigger Pro Qwiic library assume users have an SD card with the demo image loaded onto it. You can download a ZIP of the image by clicking the button below:

<center>
[WAV Trigger Pro Keyboard Demo SD Image (ZIP)](./assets/demos/Keyboards_demo_card.zip){ .md-button .md-button--primary }  
</center>

## Code to Note

All four examples include similar setups to initialize the WAV Trigger Pro on the I<sup>2</sup>C bus, return the firmware version string and number of available audio tracks. All of these steps have a message printed out over serial so to view them open the [Arduino serial monitor](https://learn.sparkfun.com/tutorials/terminal-basics/arduino-serial-monitor-windows-mac-linux) with the baud set to <b>9600</b> to see these messages. If any of these fail, the code will print out "WAV Trigger Pro response not available".

## Example 1 - Loop Track

The first example demonstrates how to loop a single track (in this case, a 440Hz sine wave) continuously. Open the example by navigating in Arduino to "File > Examples > SparkFun WAV Trigger Pro Qwiic > Example_01_Loop_Track" or copy the code below into a blank sketch. 

??? "Example 1 - Loop Track"

    ```
	--8<-- "https://raw.githubusercontent.com/robertsonics/WAV_Trigger_Pro_Qwiic_Arduino_Library/refs/heads/master/examples/Example_01_Loop_Track/Example_01_Loop_Track.ino"
	```

The example initializes the WAV Trigger Pro over I<sup>2</sup>C along with the other checks outlined above and then plays the sine wave file on loop at -20dB in stereo (centered), with a 1 second attack using the command: <code>wtp.trackPlayPoly(100, -20, BALANCE_MID, 1000, 0, LOOP_FLAG);</code>

## Example 2 - Play Tracks

The second example demonstrates how to loop through a sequence of tracks. It continuously plays the eight spoken number tracks in sequential order alternating output between the left and right audio channels.

??? "Example 2 - Play Tracks"

    ```
	--8<-- "https://raw.githubusercontent.com/robertsonics/WAV_Trigger_Pro_Qwiic_Arduino_Library/refs/heads/master/examples/Example_02_Play_Tracks/Example_02_Play_Tracks.ino"
	```

## Example 3 - Mix Tracks

The third example shows how to mix several tracks to play together. It starts the mix with an ambient music track, then plays a dialog track followed by a fade into a second music track.

??? "Example 3 - Mix Tracks"

    ```
	--8<-- "https://raw.githubusercontent.com/robertsonics/WAV_Trigger_Pro_Qwiic_Arduino_Library/refs/heads/master/examples/Example_03_Mix_Tracks/Example_03_Mix_Tracks.ino"
	```

## Example 4 - MIDI

The fourth example demonstrates how to use MIDI commands to play tracks on the WAV Trigger Pro. The example cycles between playing a combination of tracks to create a piano chord, percussion tracks and a second piano chord.

??? "Example 4 - MIDI"

    ```
	--8<-- "https://raw.githubusercontent.com/robertsonics/WAV_Trigger_Pro_Qwiic_Arduino_Library/refs/heads/master/examples/Example_04_MIDI/Example_04_MIDI.ino"
	```
The main loop plays these tracks by sending a MIDI message for the selected tracks using the <code>sendMidiMsg</code> function.
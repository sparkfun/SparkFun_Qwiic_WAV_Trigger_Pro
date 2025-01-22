## Serial Console Interface

The WAV Trigger Pro firmware (both Device & Host) sets the STM32 UART pins (RX/TX) up to be used with a [serial terminal](https://learn.sparkfun.com/tutorials/terminal-basics) like the Arduino Serial monitor. It works by sending ASCII commands to trigger playing, looping and stopping tracks, loading presets and also device status which can help provide important information about a connected &micro;SD card's performance. This serial interface works simultaneously with everything else running on the board. Refer to the [Audio Output & Serial Console](./audio.md) section of this guide for more information on these commands.

## Status LED Information

The green STAT LED can provide some basic information on the current status of the Qwiic WAV Trigger Pro.

* 3 Quick Blinks - No problems. Both the &micro;SD card and WAV files were found
    * After the initial pattern, the STAT LED will flash quickly every couple seconds as a "Heartbeat"
    * Goes solid while audio is playing
* 1 Long then 1 Short Blink (Repeating) - No &micro;SD card found
* 1 Long then 2 Short Blinks (Repeating) - File system error
* 1 Long then 3 Short Blinks (Repeating) - No WAV Fils found on &micro;SD card
* 1 Long then 4 Short Blinks (Repeating) - Memory error

## Running Temperature

The Qwiic WAV Trigger Pro does run a little warm though in our testing it did not provide any adverse effects and is within the operating temperature range of the STM32. If you plan to continuously power and use the board over a long period of time or have it in an enclosed space, you may want to attach a small heat sink to the STM32 IC.

## Preset Demos

Robertsonics has created a couple of sample SD card images for Keyboard and Percussion USB MIDI demos. Each image includes sets of WAV and Preset files in a ZIP download. All you need to do is download the image, unzip it and load it onto an empty and formatted &micro;SD card and plug the card into the WAV Trigger Pro.

### Keyboard Demo

The Keyboard demo is intended for use with a MIDI keyboard and includes three sets of instrument sounds - piano, strings and organ - over the same 3-octave range. It also includes four presets that select one or more of the instruments to be available with different performance parameters. You can download the SD image and Preset sheet from the links below:

<center>
[WAV Trigger Pro Keyboard Demo SD Image](https://drive.google.com/file/d/1-uz4BdS7XvQwcvetIbcqXZCmbQjFlUzG/view?usp=sharing){ .md-button .md-button--primary }  
</center>

<center>
[WAV Trigger Pro Keyboard Demo Preset Sheet](https://docs.google.com/spreadsheets/d/1rwLasRLAfwSD74WbSEi_ZzUZDugceNfaMRffIZ08Qa0/edit?gid=0#gid=0){ .md-button .md-button--primary}
</center>

### Percussion Demo

The Percussion demo is intended for use with a velocity-sensitive pad MIDI controller to demonstrate things like velocity mapping and multiple actions per MIDI note. It includes a selection of effects, dialog and percussion. The preset file includes comments to help explain how the demo works. You can download the SD image and Preset sheet for the demo from the links below:

<center>
[WAV Trigger Pro Percussion Demo SD Image](https://drive.google.com/file/d/10YIjcX3KPo2wQbK0kOHm8vAypqxIgcHO/view?usp=sharing){ .md-button .md-button--primary }  
</center>

<center>
[WAV Trigger Pro Percussion Demo Preset Sheet](https://docs.google.com/spreadsheets/d/1vp9_36zpnPWcXSzHMWwwxRJSGP73pbZOnCWk7p7_FoQ/edit?gid=0#gid=0){ .md-button .md-button--primary}
</center>

## General Troubleshooting

!!! info
    <p><span class="glyphicon glyphicon-question-sign" aria-hidden="true"></span> <strong>Not working as expected and need help? </strong></p>
    <p>If you need technical assistance and more information on a product that is not working as you expected, we recommend heading on over to the <a href="https://www.sparkfun.com/technical_assistance">SparkFun Technical Assistance</a> page for some initial troubleshooting.</p>
    <center>
    [SparkFun Technical Assistance Page](https://www.sparkfun.com/technical_assistance){ .md-button .md-button--primary }
    </center>
    <p>If you can't find what you need there, you'll need a <a href="https://forum.sparkfun.com/ucp.php?mode=register">Forum Account</a> to search product forums and post questions.<p>
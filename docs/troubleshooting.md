## UART Command Interface

The WAV Trigger Pro firmware (both Device & Host) sets the STM32 UART pins (RX/TX) up to be used with a [serial terminal](https://learn.sparkfun.com/tutorials/terminal-basics) like the Arduino Serial monitor. It works by sending ASCII commands to trigger playing, looping and stopping tracks, loading presets and also device status which can help provide important information about a connected &micro;SD card's performance. This serial interface works simultaneously with everything else running on the board. Refer to the [Audio Output & UART Interface](./audio.md) section of this guide for more information on these commands.

## Status LED Information

The green STAT LED can provide some basic information on the current status of the Qwiic WAV Trigger Pro.

* 3 Quick Blinks - No problems. Both the &micro;SD card and WAV files were found
    * After the initial pattern, the STAT LED will flash quickly every couple seconds as a "Heartbeat"
    * Goes solid while audio is playing
* 1 Long then 1 Short Blink (Repeating) - No &micro;SD card found
* 1 Long then 2 Short Blinks (Repeating) - File system error
* 1 Long then 3 Short Blinks (Repeating) - No WAV Fils found on &micro;SD card
* 1 Long then 4 Short Blinks (Repeating) - Memory error

## Preset Demos

Robertsonics has created a couple of demontstration downloads that include a ZIP image of a demo SD card (includes WAV files & preset .csv files) along with a corresponding Preset spreadsheet for both a Keyboard and Percussion demo. If you're having trouble getting your own Preset and WAV files working on your WAV Trigger Pro, try loading one of these onto your SD card to verify the board is working properly. You can also refer to the Preset spreadsheet files to get started creating your own Preset file. All of these files are available for doownloading clicking the buttons below:

**Update SD Image Links - ML**

<center>
[WAV Trigger Pro Keyboard Demo SD Image (ZIP)](){ .md-button .md-button--primary }  
</center>

<center>
[WAV Trigger Pro Percussion Demo (ZIP)](){ .md-button .md-button--primary }
</center>

<center>
[Keyboard Demo Preset Sheet (XLSX)](./assets/demos/Keyboards1.xlsx){ .md-button .md-button--primary}
</center>

<center>
[Percussion Demo Preset Sheet (XLSX)](./assets/demos/Percussion.xlsx){ .md-button .md-button--primary}
</center>

## General Troubleshooting

!!! info
    <p><span class="glyphicon glyphicon-question-sign" aria-hidden="true"></span> <strong>Not working as expected and need help? </strong></p>
    <p>If you need technical assistance and more information on a product that is not working as you expected, we recommend heading on over to the <a href="https://www.sparkfun.com/technical_assistance">SparkFun Technical Assistance</a> page for some initial troubleshooting.</p>
    <center>
    [SparkFun Technical Assistance Page](https://www.sparkfun.com/technical_assistance){ .md-button .md-button--primary }
    </center>
    <p>If you can't find what you need there, you'll need a <a href="https://forum.sparkfun.com/ucp.php?mode=register">Forum Account</a> to search product forums and post questions.<p>
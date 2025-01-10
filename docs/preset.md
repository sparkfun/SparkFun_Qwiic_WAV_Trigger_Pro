



## Preset File Overview

The Qwiic WAV Trigger Pro assigns functions to MIDI notes using a spreadsheet format we'll refer to as "Presets". These presets can be made using any spreadsheet application (Excel, Google Sheets, etc.) that can export to a `.csv` file. The Presets configure how all 127 MIDI notes function including which track to play, playback actions, pitch offset, attack/release velocity, and even to call another Preset stored on the &micro;SD card. 

As you may imagine, the Preset contains a *lot* of information so we'll go into detail below on how each column in the file works.

### Preset File Naming Convention

When creating a Preset, make sure to export it to a .csv file named "set_nnnn.csv" where "nnnn" is a 4-digit number with leading zeroes. For example, a preset file named "set_0001.csv" would be Preset 1, "set_0002" would be Preset 2 and so on. On reset, the WAV Trigger Pro looks for and loads the preset “set_0001.csv” automatically, if present, otherwise it will initialize to a default preset.

Functions that load presets (Column 4 - Action and Column 5 - Track/Preset) refer to the preset number in the filename. For example, setting a MIDI note to load a preset named "set_0123.csv" requires setting the action in Column 4 to "Load Preset" and the Track/Preset value in Column 5 to "123". 

### Preset Demos

Robertsonics has created a couple of demontstration downloads that include a ZIP image of a demo SD card (includes WAV files & preset .csv files) along with a corresponding Preset spreadsheet for both a Keyboard and Percussion demo. You can download the SD images by clicking the buttons below:

**Update links to SD Images - ML**

<center>
[WAV Trigger Pro Keyboard Demo SD Image (ZIP)](){ .md-button .md-button--primary }  
</center>

<center>
[WAV Trigger Pro Percussion Demo (ZIP)](){ .md-button .md-button--primary }
</center>

And if you'd like to download and review or modify a Preset sheet for the demos, you can download them by clicking the buttons below:

<center>
[Keyboard Demo Preset Sheet (XLSX)](./assets/demos/Keyboards1.xlsx){ .md-button .md-button--primary}
</center>

<center>
[Percussion Demo Preset Sheet (XLSX)](./assets/demos/Percussion.xlsx){ .md-button .md-button--primary}
</center>

## Column Overview

Each line in Preset files use fourteen columns that cover all MIDI notes' possible function and behavior assignments. The list below outlines each column and how to use them:

* <b>Column 1 - Command:</b> Any line that does not begin with a field starting with the character ‘#” in Column 1 is considered a comment and ignored. If the line contains ‘#NOTE’ in the first column, then that line is expected to be a complete Note Action description with the following format:

* <b>Column 2 - MIDI Note number (0 - 127):</b> Each MIDI Note number may appear in a Note Action line up to 8 times (any more than 8 will be ignored.) Each Action line will assign one function to the corresponding MIDI Note to be executed on Note-On/Note-Off events. In this way, a single MIDI Note can perform up to 8 actions.

* <b>Column 3 - MIDI Channel number (0 - 16):</b> Each action can be assigned to either a specific MIDI channel or any channel (Omni). MIDI Channels are numbered 0 - 15, while a value of 16 will cause the channel number to be ignored so that the note on any channel will perform the action. Using multiple actions, a single MIDI note can play different sounds on different channels.

* <b>Column 4 - Action:</b> There are currently 5 available actions defined. These are contained within a list at the top of the spreadsheet (within the red box) and the action field is a drop-down selection for that list. The available actions are:

    * <b>Play Note:</b> This is the normal behavior of a MIDI Note, namely a Note-On starts the track and a Note-Off stops the track. The volume is scaled by the MIDI Note-On velocity.

    * <b>Trigger:</b> A Note-On starts the track with a velocity of 127. Both the MIDI Note-On velocity and the corresponding Note-Off are ignored.

    * <b>Stop Track:</b> This action is triggered by the Note-On event and stops the specified track;

    * <b>Stop All:</b> This action is triggered by the Note-On event and stops all tracks.

    * <b>Load Preset:</b> This action is triggered by the Note-On message and loads the specified preset file from the microSD card.

* <b>Column 5 - Track/Preset:</b> This field is the target track number or preset number for the action. Tracks are numbered 0 to 4095, while presets are numbered 0 to 9999.

<b>Column 6 - Pitch Offset:</b> Any action that causes a track to play can specify a pitch offset of -700 to +700 cents (100 cents is one musical semitone.) A pitch offset of 0 will cause the track to play with no offset.

<b>Columns 7 and 8 - Attack and Release:</b> These fields will introduce a volume ramp up or down when the track starts and stops. Specified in milliseconds.

<b>Column 9 - Loop:</b> A value of 0 means the track will stop when it reaches the end. A value of 1 will cause the track to seamlessly loop until it is stopped.

<b>Column 10 - Lock:</b> The WAV Trigger Pro has a voice stealing algorithm. If when a track is started, there are no voices available, the oldest running voice will be “stolen” to play the new track. Putting a value of 1 in the Lock field will prevent the track from having its voice stolen if this happens. This can be useful if you have a backing track that you don’t want to get cut off.

<b>Columns 11 and 12 - Min and Max Velocity:</b> These fields determine a range of MIDI Note Velocities that will trigger the action. If a Note-On velocity falls outside this range, the track will not be started. Multiple Play Note actions defined for a single Note number with different ranges allows for different tracks to be triggered based on velocity.

<b>Column 13 - Gain (-80 to 0):</b> This value controls the maximum volume for the track. The gain is set in dB, with 0 being no attenuation and -80 being pretty much silence. For the action Play Note, the gain is scaled by the MIDI Note-On velocity.

<b>Column 14 - Balance (0 - 127):</b> This value controls the Left/Right channel balance of the track. A value of 0 is Left channel only, while a value of 127 is Right channel only. A value of 64 results in equal Left and Right channels.
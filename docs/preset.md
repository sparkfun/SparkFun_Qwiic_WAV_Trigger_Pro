



## Preset File Overview

The Qwiic WAV Trigger Pro assigns functions to MIDI notes using a spreadsheet format we'll refer to as "Presets". These presets can be made using any spreadsheet application (Excel, Google Sheets, etc.) that can export to a `.csv` file. The Presets configure how all 127 MIDI notes function including which track to play, playback actions, pitch offset, attack/release velocity, and even to call another Preset stored on the &micro;SD card. 

As you may imagine, the Preset contains a *lot* of information so we'll go into detail below on how each column in the file works.

### Preset File Naming Convention

When creating a Preset, make sure to export it to a .csv file named "set_nnnn.csv" where "nnnn" is a 4-digit number with leading zeroes. For example, a preset file named "set_0001.csv" would be Preset 1, "set_0002" would be Preset 2 and so on. On reset, the WAV Trigger Pro looks for and loads the preset “set_0001.csv” automatically, if present, otherwise it will initialize to a default preset.

Functions that load presets (Column 4 - Action and Column 5 - Track/Preset) refer to the preset number in the filename. For example, setting a MIDI note to load a preset named "set_0123.csv" requires setting the action in Column 4 to "Load Preset" and the Track/Preset value in Column 5 to "123". 

### Default Preset

On power up or reset, the WAV Trigger looks for and attempts to automatically load Preset 1 (set_0001.csv). If that file does not exist on the SD card then it loads an internal default preset with the following action assignments:

MIDI Notes 1-8 have an action type 2, Trigger, Edge and set to trigger the corresponding track number with a gain of 0, center panned, attack/release time of 0ms and no flags set. This sets the eight trigger pins to toggle tracks 1-8 polyphonically, very similar to the behavior from the original WAV Trigger and Tsunami.

MIDI Notes 9-127 have an action type 1, Play and set to play the corresponding track number with a gain of 0, center panned, attack/release time of 0ms, full velocity and gain scaling with no flags set. This sets MIDI notes 9-127 to play tracks 9-127 as velocity sensitive MIDI notes that respond to both Note-On and Note-Off messages.

## Column Overview

Each line in Preset files use fourteen columns that cover all MIDI notes' possible function and behavior assignments. The list below outlines each column and how to use them:

* <b>Column 1/A - Command:</b> Assigning an action to a MIDI note number requires entering "#NOTE" in this column. Anything else here will cause the entire row to be considered a comment and ignored.

* <b>Column 2/B - MIDI Note number (0 - 127):</b> Each MIDI Note number may appear in a Note Action line up to 8 times in any particular order in the Preset file (any more than 8 will be ignored.) Each Action line will assign one function to the corresponding MIDI Note to be executed on Note-On/Note-Off events. In this way, a single MIDI Note can perform up to 8 actions.

* <b>Column 3/C - MIDI Channel number (0 - 15):</b> Each action can be assigned to either a specific MIDI channel or any channel (Omni). If the number in this column is 0 - 15 the action only occurs for the corresponding MIDI channel. A value of 16 sets the action to occur for any MIDI channel (Omni). Using multiple actions, a single MIDI note can play different sounds on different channels.

* <b>Column 4/D - Action:</b> There are currently 7 available actions defined. These are contained within a list at the top of the spreadsheet (within the red box) and the action field is a drop-down selection for that list. The available actions are:

    * <b>Action Type 01: Play Note:</b> This is the normal behavior of a MIDI Note. The track number set in column 5/E starts with a MIDI Note-On message with a target volume proportional to the MIDI velocity. A MIDI Note-Off commessagemand stops the track.

    * <b>Action Type 02: Trigger, Edge:</b> This action ignores both MIDI velocity and the corresponding MIDI Note-Off message. A track with this action is polyphonic and mixed with any previous instance of this action's track.

    * <b>Action Type 03: Trigger, Level:</b> This action ignores MIDI velocity and stops the track with the corresponding Note-Off message.

    * <b>Action Type 04: Trigger, Conditional:</b> This action type ignores MIDI velocity and the track will not start if a previous instance of this track is still playing.

    * <b>Action Type 05: Stop Track:</b> This action stops a track with the specified release time.

    * <b>Action Type 06: Stop All:</b> This action stops all tracks currently playing.

    * <b>Action Type 07: Load Preset:</b> This action loads the specified preset file in Column 5/E.

* <b>Column 5/E - Track/Preset:</b> This field sets the target track number or preset number for the action specified in Column 4/D. For action types 1-6 this refers to the track number. For action type 7 this refers to the preset number. Tracks are numbered 0 to 4095, while presets are numbered 0 to 9999.

* <b>Column 6/F - Pitch Offset:</b> This value refers to the sample-rate offset applied to the track when started. Any action that causes a track to play can specify a pitch offset of -700 to +700 cents (100 cents equalling one musical semitone.) A pitch offset of 0 will cause the track to play with no offset.

* <b>Columns 7/G and 8/H - Attack and Release:</b> MIDI note attack and release time specified in milliseconds.

* <b>Column 9/I - Loop Flag:</b> A value of 1 in this column causes the track to seamlessly loop from end to beginning until it is stopped.

* <b>Column 10/J - Lock Flag:</b> The WAV Trigger Pro has a voice stealing algorithm. If when a track is started, there are no voices available, the oldest running voice will be “stolen” to play the new track. Putting a value of 1 in the Lock field prevents the track from having its voice stolen if this happens. This can be useful if you have a backing track that you don’t want to get cut off.

* <b>Column 11/K - Pitch Bend Flag:</b> A value of 1 in this column causes the track to be modified by any MIDI Pitch Bend messages.

* <b>Columns 12/L and 13/M - Min and Max Velocity:</b> For action type 1, any MIDI Note-On message with a velocity outside this range is ignored.

* <b>Column 14/N and 15/O - Min and Max Velocity Gain:</b> For action type 1, sets the gain range scaled to the velocity range. This means the gain at the min velocity matches the min velocity gain and the gain at the max velocity matches the max velocity gain.

* <b>Column 16/P - Balance (0 - 127):</b> This value controls the Left/Right channel balance of the track. A value of 0 is Left channel only, while a value of 127 is Right channel only. A value of 64 means center panned audio between Left and Right channels.

### Preset Demos

Robertsonics has created a couple of sample SD card images for Keyboard and Percussion USB MIDI demos. Each image includes sets of WAV and Preset files in a ZIP download. All you need to do is download the image, unzip it and load it onto an empty and formatted &micro;SD card and plug the card into the WAV Trigger Pro.

#### Keyboard Demo

The Keyboard demo is intended for use with a MIDI keyboard and includes three sets of instrument sounds - piano, strings and organ - over the same 3-octave range. It also includes four presets that select one or more of the instruments to be available with different performance parameters. You can download the SD image from the link below:

<center>
[WAV Trigger Pro Keyboard Demo SD Image](https://drive.google.com/file/d/1-uz4BdS7XvQwcvetIbcqXZCmbQjFlUzG/view?usp=sharing){ .md-button .md-button--primary }  
</center>

#### Percussion Demo

The Percussion demo is intended for use with a velocity-sensitive pad MIDI controller to demonstrate things like velocity mapping and multiple actions per MIDI note. It includes a selection of effects, dialog and percussion. The preset file includes comments to help explain 

<center>
[WAV Trigger Pro Percussion Demo SD Image](https://drive.google.com/file/d/10YIjcX3KPo2wQbK0kOHm8vAypqxIgcHO/view?usp=sharing){ .md-button .md-button--primary }  
</center>
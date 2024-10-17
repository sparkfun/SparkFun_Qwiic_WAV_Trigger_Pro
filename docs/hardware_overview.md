---
icon: material/cog
---

In this section we'll take a closer look at the components on the WAV Trigger Pro (Qwiic).

## STM32H Microcontroller

The WAV Trigger Pro uses the STM32H750VBTx CPU.

## Power Inputs

The WAV Trigger Pro has three options for powering the board; USB-C, Qwiic, or dedicated through-hole pins.

### USB-C

The USB-C connector on the board provides both a serial connection along with a power input. By default, when plugging the board in over USB-C to a computer, it will appear as a USB MIDI Device. When the WAV Trigger Pro is configured to act as a USB MIDI Host and powered through the dedicated through-hole power pins, the USB-C connector can supply <b>500mA@5V</b> to a connected USB MIDI device. Running the WAV Trigger Pro as a USB MIDI Host requires uploading alternate firmware as well as modifying the appropriate solder jumpers. Read on to the [USB MIDI Host Assembly]() section for detailed information on this configuration.

### Qwiic Connector

The board includes a pair of Qwiic connectors to integrate it into SparkFun's [Qwiic ecosystem](). These connectors provide both an I<sup>2</sup>C connection as well as power (<b>3.3V</b>) to the WAV Trigger Pro.

### Through-Hole Power Pins

This pair of 0.1"-spaced plated through-hole (PTH) pins labeled <b>5V</b> and <b>GND</b> accept a supply voltage of <b>5V</b>. This power input is primarily intended for running the WAV Trigger Pro as a USB MIDI Host.

## Polyphonic Engine

The operation of the WAV Trigger Pro's polyphonic engine is proprietary to [Robertsonics](https://www.robertsonics.com). While we cannot go into exact details on how this works, here are some highlights of the engine's functionality:

* Up to 4096 uncompressed 16-bit, 44.1kHz mono and stereo WAV files (CD Quality)
* Polyphonic - Play and mix 24 tracks independently and simultaneously with independent pitch control
* MIDI notes can trigger up to 8 independent actions, routing tracks to any combination of outputs
* Up to 8 velocity range assignments per note to trigger alternate samples
* Each event provides independent pitch offset (in cents) allowing for true multi-sampling
* Seamless looping over arbitrary track length
* 

### MIDI Control

The WAV Trigger Pro introduces MIDI-USB host and device capabilities. The board can function as either a USB-MIDI device or USB-MIDI host. When acting as a USB-MIDI host and powered independently it can power a connected MIDI device with <b>500mA@5V</b>. This means you can have complete USB-MIDI interactivity with the WAV Trigger Pro with <i>no</i> computer required! Do note, running the WAV Trigger Pro as a MIDI-USB host requires uploading alternate firmware as well as physically adjusting the appropriate solder jumpers. Read on to the "MIDI Host Assembly" section for complete instructions.

### Trigger Control

The board also includes eight independent trigger inputs routed to through-hole pins. All eight trigger pins can be individually configured.

### Qwiic (I<sup>2</sup>C) Control

This WAV Trigger also includes a pair of Qwiic connectors to integrate with SparkFun's [Qwiic ecosystem](). Users can use this in tandem with the [**link needed - Mark L** Arduino Library]() to toggle audio tracks.

### Audio Output

The WAV Trigger Pro has two channels for audio output routed to through-hole pins. Soldering to these pins is required for the audio output to work properly. If you have never soldered before or want some tips, check out our [How to Solder: Through Hole Soldering Tutorial](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering).

### Presets

The WAV Trigger Pro introduces <i>Presets</i>! Presets are managed through spreadsheet .csv files (Excel or Google Sheets) loaded onto a connected &micro;SD card which describe up to 8 actions per MIDI note, based on channel and velocity. Each action can start and independent track with individual gain, balance, attack, release, and pitch. This allows multiple sounds to be mixed in performance. Assigning velocity ranges allows for velocity switching per note. 

If you've used previous WAV Triggers before, these Preset files take the place of the configuration app. You can have multiple presets stored on the file that you can switch between. Read on to the "Configuration File" section of this guide for detailed information on how to setup and use these files.

## &micro;SD Card Slot

The &micro;SD card holder on the WAV Trigger Pro is on the back/reverse side of the board. This card is used to store <code>.wav</code> files, initialization <code>.ini</code> file (optional), and preset <code>.csv</code> file. 

## Pinout

### Trigger Pins

The WAV Trigger Pro has eight PTH trigger pins mapped to MIDI note numbers called in the Preset file.

### Audio Output

The WAV Trigger Pro has two channel (stereo) output routed <i>only</i> to PTH pins labeled <b>L</b>, <b>R</b>, and <b>G</b>.

### STM UART & Boot

The STM32's serial UART (RX/TX) pins and BOOT pin are routed to PTHs. These pins primarily function to set the STM32 into BOOT mode for uploading new firmware to the board. The BOOT pin is routed directly next to a Ground pin to make closing this pin jumper easy.

### Power Input

When not using USB or Qwiic for power, connect a <b>5V</b> supply to power the board. 

## LEDs

The board has two LEDs on board labeled <b>PWR</b> and <b>STAT</b>. The red <b>PWR</b> LED indicates whenever the board is powered. The green STAT LED provides helpful information on the current status of the WAV Trigger. On reset, the STAT LED blinks in the following patterns:

* 3 Quick Blinks - No problems. Both the &micro;SD card and WAV files were found
    * After the initial pattern, the STAT LED will flash quickly every couple seconds as a "Heartbeat"
    * Goes solid while audio is playing
* 1 Long then 1 Short Blink (Repeating) - No &micro;SD card found
* 1 Long then 2 Short Blinks (Repeating) - File system error
* 1 Long then 3 Short Blinks (Repeating) - No WAV Fils found on &micro;SD card
* 1 Long then 4 Short Blinks (Repeating) - Memory error

## Solder Jumpers

The WAV Trigger Pro has six solder jumpers. The list below outlines their names, functionality, default states and any notes on their use.

* <b>HST/DEV</b> - This pair of three-way solder jumpers work with the <b>VBUS</b> jumper to switch the functionality of USB-MIDI control between acting as a Device or Host. 
* <b>VBUS</b> - 
* 

## Board Dimensions
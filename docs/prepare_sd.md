



The Qwiic WAV Trigger Pro requires a &micro;SD card to store and load WAV and Preset files. 

## Recommended SD Cards & Format

This and other WAV Trigger boards from robertsonics interact differently with SD cards than what manufacturers typically expect. WAV Triggers rely on fast and, more importantly, reliable file access with small timeout windows. The WAV Trigger Pro firmware is only compatible with SD cards formatted to either a <b>FAT16</b> or <b>FAT32</b>. 

We strongly recommend using cards that use one of these formats by default. If you are using a larger capacity SD card that uses another format (exFAT, etc.), you <b>must</b> format it to <b>FAT32</b> and set the max allocation size to 32k. You can set both of these using the Qwiic Format application in Windows.

Robertsonics has done some fairly extensive testing with his previous WAV Trigger boards and has some great write ups on SD card performance and the unique requirements of the WAV Trigger boards. These offer a few recommendations though some of the recommended cards may no longer be available or have updated versions of them:

* [MicroSD Cards for Audio - 2024](https://www.robertsonics.com/blog/microsd-cards-for-audio-2024)
* [MicroSD Cards for Audio - 2021](https://www.robertsonics.com/blog/2021/03/25/2021-microsd-card-update)

## Format &micro;SD Card

If you're using a brand new SD card, you may not need to format it though it may come with pre-installed files that could cause performance issues with the WAV Trigger Pro. The Quick Format option in Windows is the usually the simplest method to properly format the µSD card.

## &micro;SD Card Contents & Naming Convention

The SD Card should only contain <code>.wav</code> audio files and <code>.csv</code> Preset files following the proper naming convention. Preset files, as covered in the previous section, should be named "set_nnnn.csv" where "nnnn" is a 4-digit number with leading zeroes (eg. "set_0001.csv" would be Preset 1). WAV files should be named "nnnn.wav" where "nnnn" is a 4-digit number with leading zeros. If you'd like, you can add a descriptor to the audio filenames by adding an underscore to the file name followed by the descriptor (eg. "0123_piano.wav").

### Audio File Format

If your audio files are using another format, you'll need to convert them to 16-bit, 44.1kHz mono or stereo WAV format. There's many options for converting audio files but the WAV Trigger Pro does not support WAV files with any additional header information or metadata. Some audio recording programs, such as Pro Tools, write additional information at the start of the file. An easy way to remove the unnecessary header information is to utilize [Audacity](http://www.audacityteam.org/). Users can use this software to export a file as WAV (Microsoft) signed 16-bit PCM and clear out the metadata containing the header infromation (i.e. title, artist, genre, etc.).

The following video gives a brief demonstration of the Audacity export process.

<center>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/pu6zvnoPTfQ?si=7Rf66krO_RQSI0k0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</center>
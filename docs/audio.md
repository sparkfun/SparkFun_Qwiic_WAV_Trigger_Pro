



## Audio Output Pins

The audio output of the WAV Trigger Pro is routed to three 0.1"-spaced headers labeled <b>L</b>, <b>G</b> and <b>R</b>. This requires some through-hole soldering of either wires or headers to connect to your preferred audio output. For the purposes of this guide we'll be soldering headers to these pins to connect to a [SparkFun TRRS 3.5MM Jack Breakout](https://www.sparkfun.com/products/11570) to plug a pair of headphones into.

The WAV Trigger Pro requires soldering to these pins regardless of how it is configured and used so make sure to complete this step at some point during your preferred assembly.

### Soldering

??? note "New to soldering?"
	If you have never soldered before or need a quick refresher, check out our [How to Solder: Through-Hole Soldering](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering) guide.
	<p align="center">
		<a href="https://learn.sparkfun.com/tutorials/5">
		<img src="https://cdn.sparkfun.com/c/264-148/assets/e/3/9/9/4/51d9fbe1ce395f7a2a000000.jpg" alt="Tutorial's thumbnail"><br>
        How to Solder: Through-Hole Soldering</a>
	</p>

Start by locating the three-pin PTH header with the labels <b>R</b>, <b>G</b> and </b>L</b>. Depending on whether you prefer a permanent soldered connection or something removeable, solder either wire or male/female headers to these pins like the photo below shows with male headers soldered:

<figure markdown>
[![Photo showing male headers soldered to the Audio PTHs](./assets/img/WAV_Trigger_Pro-Audio_PTHs.jpg){ width="600"}](./assets/img/WAV_Trigger_Pro-Audio_PTHs.jpg "Click to enlarge")
</figure>

If you're using the TRRS Breakout like we are, make sure to solder male/female headers or wire to the pins on that breakout like this:

<figure markdown>
[![Photo showing headers soldered to TRRS breakout.](./assets/img/WAV_Trigger_Pro-TRRS_Breakout.jpg){ width="600"}](./assets/img/WAV_Trigger_Pro-TRRS_Breakout.jpg)
</figure>

### Wiring

Next connect the TRRS Breakout (or your preferred audio output) to the WAV Trigger's audio pins. Make the following connections if you're connecting the WAV Trigger to the TRRS 3.5mm Breakout:

<table>
    <tr>
        <th>WAV Trigger Pro</th>
        <th>TRR Breakout</th>
        <th>Color</th>
    </tr>
    <tr>
        <td>R</td>
        <td>RING1</td>
        <td>RED</td>
    </tr>
    <tr>
        <td>G</td>
        <td>SLEEVE</td>
        <td>BLACK</td>
    </tr>
    <tr>
        <td>L</td>
        <td>TIP</td>
        <td>YELLOW</td>
    </tr>
</table>

<figure markdown>
[![Photo showing WAV Trigger Pro connected to TRRS Breakout](./assets/img/WAV_Trigger_Pro-Audio_Assembly.jpg){ width="600"}](./assets/img/WAV_Trigger_Pro-Audio_Assembly.jpg "Click to enlarge")
</figure>
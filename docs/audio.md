



## Audio Output Pins

The audio output of the WAV Trigger Pro is routed to three 0.1"-spaced headers labeled <b>L</b>, <b>G</b> and <b>R</b>. This requires some through-hole soldering of either wires or headers to connect to your preferred audio output. For the purposes of this guide we'll be soldering headers to these pins to connect to a [SparkFun TRRS 3.5MM Jack Breakout](https://www.sparkfun.com/products/11570) to plug a pair of headphones into.

All three assembly options (Trigger, Qwiic & USB) require soldering to these pins so make sure to complete this step at some point during your preferred assembly.

### Soldering

??? note "New to soldering?"
	If you have never soldered before or need a quick refresher, check out our [How to Solder: Through-Hole Soldering](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering) guide.
	<p align="center">
		<a href="https://learn.sparkfun.com/tutorials/5">
		<img src="https://cdn.sparkfun.com/c/264-148/assets/e/3/9/9/4/51d9fbe1ce395f7a2a000000.jpg" alt="Tutorial's thumbnail"><br>
        How to Solder: Through-Hole Soldering</a>
	</p>

Locate the three-pin PTH header with the labels <b>R</b>, <b>G</b> and </b>L</b>. Depending on whether you prefer a permanent soldered connection or something removeable, solder either wire or male/female headers to these pins like the photo below shows:

**Photo of soldered audio pins - Mark L**

### Wiring

After soldering to the audio pins, take care to wire up each channel with a common ground. In this guide, we're connecting the audio output to a TRRS breakout so we make the following connections:

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

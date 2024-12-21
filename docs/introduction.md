---
icon: material/book-open-page-variant
---

# Hookup Guide


## Introduction
<!-- Single Product Card -->

<div class="grid cards desc" markdown>

-    <a href="https://www.sparkfun.com/products/25860">
    **<SparkFun Qwiic WAV Trigger Pro>**<br>
    **SKU:** WIG-25860

    ---

    <figre markdown>
    ![Product Thumbnail](<Product Image Link>)
    </figure></a>

    <center>
    <article class="video_desc">
    <iframe src="<Embedded Video>" title="Product Showcase: <Official Product Name>" frameborder="0" allow="accelerometer; autoplay; clipboard-write;encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </article>
    </center>

-    The Qwiic WAV Trigger Pro is the latest evolution of the line of high-fidelity polyphonic audio players. The WAV Trigger Pro improves on the previous versions with a more powerful processor, enhanced MIDI processing - including velocity switching and multi-timbral support - and MIDI USB Device (Default) <b>and</b> MIDI USB Host support, all in a smaller 1.75" x 1.5" footprint! <br><br>
The Qwiic WAV Trigger Pro supports up to 4096 uncompressed 16-bit, 44.1kHz mono and stereo WAV files matching CD audio quality. The WAV Trigger Pro supports polyphony and can play and mix up to 24 tracks simultaneously and independently with exceptionally low latency (7ms typically). Control track playback via either 8 programmable trigger inputs, I<sup>2</sup>C (Qwiic), or MIDI (USB or Serial UART). The board can function as both a USB MIDI device <i>and</i> host meaning if the WAV Trigger Pro has power in USB MIDI Host mode it can supply up to 500mA@5V to a connected MIDI device over USB-C allowing for USB MIDI control with no computer required.

    <center>
    [Purchase from SparkFun :fontawesome-solid-cart-plus:{ .heart }](https://www.sparkfun.com/products/25860){ .md-button .md-button--primary }
    </center>

</div>

## Required Materials

The Qwiic WAV Trigger Pro requires a few additional items to get up and running properly. If you'd like to follow along with the examples in this tutorial, you'll want at least the following items along with a pair of <i>corded</i> headphones. If you'd like to follow the USB MIDI Host example, make sure you have a USB MIDI device like a MIDI Keyboard or Pad.

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/14743">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/1/2/9/7/2/14743-USB_3.1_Cable_A_to_C_-_3_Foot-01.jpg)
    </figure>

    ---

    **USB 3.1 Cable A to C - 3 Foot**<br>
    CAB-14743</a>

</div>

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/14832">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/1/3/1/0/2/14832-microSD_Card_with_Adapter_-_32GB__Class_10_-02.jpg)
    </figure>

    ---

    **microSD Card with Adapter - 32GB (Class 10)**<br>
    COM-14832</a>

</div>

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/11570">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/7/5/4/6/11570-01.jpg)
    </figure>

    ---

    **SparkFun TRRS 3.5mm Jack Breakout**<br>
    BOB-11570</a>

</div>

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/501">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/3/4/1/00501-1.jpg)
    </figure>

    ---

    **IC Hook Test Leads**<br>
    CAB-00501</a>

</div>

### Qwiic & Arduino Materials

Users who wish to use the Qwiic WAV Trigger Pro with the Qwiic ecosystem and Arduino library, you may need one or more of the following products:

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/18158">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/1/7/4/8/7/18158-SparkFun_RedBoard_Plus-01.jpg)
    </figure>

    ---

    **SparkFun RedBoard Plus**<br>
    DEV-18158</a>

</div>

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/22925">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/3/0/8/6/22925_QwiicPocket_Feature1.jpg)
    </figure>

    ---

    **SparkFun Qwiic Pocket Development Board - ESP32-C6**<br>
    DEV-22925</a>

</div>

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/17260">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/1/6/2/4/7/17260-Flexible_Qwiic_Cable_-_50mm-01.jpg)
    </figure>

    ---

    **Flexible Qwiic Cable - 50mm**<br>
    PRT-17260</a>

</div>

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/17258 ">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/1/6/2/4/5/17258-Flexible_Qwiic_Cable_-_200mm-01.jpg)
    </figure>

    ---

    **Flexible Qwiic Cable - 200mm**<br>
    PRT-17258 </a>

</div>

### Soldering Tools & Accessories

The Qwiic WAV Trigger Pro does require some through-hole soldering for the best, permanent installation and uses. Users will need to at least solder to the audio output pins along with the serial UART (TX/RX) pins for updating the firmware when necessary. If you need any soldering tools or materials, check out the following products: 

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/25926">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/6/6/4/6/TOL-25926-Hakko-FX-888DX-Soldering-Station-feature.jpg)
    </figure>

    ---

    **Hakko FX-888DX Soldering Station**<br>
    TOL-25926</a>

</div>

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/24063">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/4/3/8/5/KIT-24063-PINECIL-Soldering-Iron-Kit-Feature.jpg)
    </figure>

    ---

    **PINECIL Soldering Iron Kit**<br>
    TOL-24063</a>

</div>

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/8865">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/1/3/2/08865-01.jpg)
    </figure>

    ---

    **Hook-up Stranded Wire - Red (22 AWG)**<br>
    PRT-08865</a>

</div>

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/8867">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/1/3/4/08867-01.jpg)
    </figure>

    ---

    **Hook-up Stranded Wire - Black (22 AWG)**<br>
    PRT-08867</a>

</div>

## Suggested Reading

Below, are a few tutorials that may help users familiarize themselves with various aspects of this product:

<div class="grid cards" markdown align="center">

-   <a href="https://learn.sparkfun.com/tutorials/<Tutorial ID>">
    <figure markdown>
    ![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/<Thumbnail Link>.jpg)
    </figure>

    ---

    **<Tutorial Name>**</a>

-   <a href="https://docs.sparkfun.com/<GitHub Repo Name>">
    <figure markdown>
	![Tutorial Thumbnail](https://docs.sparkfun.com/<GitHub Repo Name>/docs/assets/img/thumbnail.jpg)
	</figure>

    ---

    **<Product Name> Hookup Guide**</a>

</div>
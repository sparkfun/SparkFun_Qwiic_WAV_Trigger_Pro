---
icon: material/book-open-page-variant
---

# Hookup Guide


## Introduction
<!-- Single Product Card -->

<div class="grid cards desc" markdown>

-    <a href="https://www.sparkfun.com/sparkfun-qwiic-wav-trigger-pro.html">
    **SparkFun Qwiic WAV Trigger Pro**<br>
    **SKU:** WIG-25860

    ---

    <figre markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/600-600/assets/parts/2/6/5/4/7/WIG-25860-WAV-Trigger-Pro-Feature.jpg)
    </figure></a>

    <center>
    <article class="video_desc">
    <iframe src="https://www.youtube.com/embed/Q4csFhDtCt4?si=DIoStJnbMPkLKFM2" title="Product Showcase: SparkFun Qwiic WAV Trigger Pro" frameborder="0" allow="accelerometer; autoplay; clipboard-write;encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </article>
    </center>

-    The Qwiic WAV Trigger Pro is the latest evolution of the line of high-fidelity polyphonic audio players from robertsonics. The Qwiic WAV Trigger Pro improves on the previous versions with a more powerful processor, enhanced MIDI processing - including velocity switching and multi-timbral support - and MIDI USB Device (Default) <b>and</b> MIDI USB Host support, all in a smaller 1.75" x 1.5" footprint! <br><br>
The Qwiic WAV Trigger Pro supports up to 4096 uncompressed 16-bit, 44.1kHz mono and stereo WAV files matching CD audio quality. The WAV Trigger Pro supports polyphony and can play and mix up to 24 tracks simultaneously and independently with exceptionally low latency (7ms typically). Control track playback via either 8 programmable trigger inputs, I<sup>2</sup>C (Qwiic), or MIDI (USB, Serial UART, or Qwiic). The board can function as both a USB MIDI device <i>and</i> host meaning if the WAV Trigger Pro has power in USB MIDI Host mode it can supply up to 500mA@5V to a connected MIDI device over USB-C allowing for USB MIDI control with no computer required.

    <center>
    [Purchase from SparkFun :fontawesome-solid-cart-plus:{ .heart }](https://www.sparkfun.com/sparkfun-qwiic-wav-trigger-pro.html){ .md-button .md-button--primary }
    </center>

</div>

## Required Materials

The Qwiic WAV Trigger Pro requires a few additional items as well as some through-hole soldering to get up and running properly. If you'd like to follow along with the examples in this tutorial, you'll want at least the following items along with a pair of <i>corded</i> headphones. If you'd like to follow the USB MIDI Host example, make sure you have a USB MIDI device like a MIDI Keyboard or Pad.

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/14743">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/1/2/9/7/2/14743-USB_3.1_Cable_A_to_C_-_3_Foot-01.jpg)
    </figure>

    ---

    **USB 3.1 Cable A to C - 3 Foot**<br>
    CAB-14743</a>

-   <a href="https://www.sparkfun.com/products/14832">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/1/3/1/0/2/14832-microSD_Card_with_Adapter_-_32GB__Class_10_-02.jpg)
    </figure>

    ---

    **microSD Card with Adapter - 32GB (Class 10)**<br>
    COM-14832</a>

-   <a href="https://www.sparkfun.com/products/11570">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/7/5/4/6/11570-01.jpg)
    </figure>

    ---

    **SparkFun TRRS 3.5mm Jack Breakout**<br>
    BOB-11570</a>

-   <a href="https://www.sparkfun.com/break-away-headers-straight.html">
    <figure markdown>
    ![Product Thumbnail](https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/0/0/00116-02-L.jpg)
    </figure>

    ---

    **Break Away Headers - Straight**<br>
    PRT-00116</a>

-   <a href="https://www.sparkfun.com/jumper-wires-connected-6-m-f-20-pack.html">
    <figure markdown>
    ![Product thumbnail](https://www.sparkfun.com/media/catalog/product/cache/a793f13fd3d678cea13d28206895ba0c/1/2/12794-00.jpg)
    </figure>

    ---

    **Jumper Wires - Connected 6" (M/F, 20 pack)**</br>
    PRT-12794</a>

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

-   <a href="https://www.sparkfun.com/products/22925">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/3/0/8/6/22925_QwiicPocket_Feature1.jpg)
    </figure>

    ---

    **SparkFun Qwiic Pocket Development Board - ESP32-C6**<br>
    DEV-22925</a>

-   <a href="https://www.sparkfun.com/products/17260">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/1/6/2/4/7/17260-Flexible_Qwiic_Cable_-_50mm-01.jpg)
    </figure>

    ---

    **Flexible Qwiic Cable - 50mm**<br>
    PRT-17260</a>

-   <a href="https://www.sparkfun.com/products/17258 ">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/1/6/2/4/5/17258-Flexible_Qwiic_Cable_-_200mm-01.jpg)
    </figure>

    ---

    **Flexible Qwiic Cable - 200mm**<br>
    PRT-17258 </a>

</div>

### Soldering Tools & Accessories

The Qwiic WAV Trigger Pro does require some through-hole soldering for the best, permanent installation and uses. Users will need to at least solder to the audio output pins as they are routed to a 0.1"-spaced PTH header. If you need any soldering tools or materials, check out the following products: 

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/25926">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/6/6/4/6/TOL-25926-Hakko-FX-888DX-Soldering-Station-feature.jpg)
    </figure>

    ---

    **Hakko FX-888DX Soldering Station**<br>
    TOL-25926</a>

-   <a href="https://www.sparkfun.com/products/24063">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/4/3/8/5/KIT-24063-PINECIL-Soldering-Iron-Kit-Feature.jpg)
    </figure>

    ---

    **PINECIL Soldering Iron Kit**<br>
    TOL-24063</a>

-   <a href="https://www.sparkfun.com/products/8865">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/1/3/2/08865-01.jpg)
    </figure>

    ---

    **Hook-up Stranded Wire - Red (22 AWG)**<br>
    PRT-08865</a>

-   <a href="https://www.sparkfun.com/products/8867">
    <figure markdown>
    ![Product Thumbnail](https://cdn.sparkfun.com/r/455-455/assets/parts/2/1/3/4/08867-01.jpg)
    </figure>

    ---

    **Hook-up Stranded Wire - Black (22 AWG)**<br>
    PRT-08867</a>

</div>

## Suggested Reading

Before getting started with this guide and the Qwiic WAV Trigger Pro, you may want to read through some of the tutorials linked below if you're not familiar with the concepts covered in them:

<div class="grid cards hide col-4" markdown align="center">

-   <a href="https://learn.sparkfun.com/tutorials/midi-tutorial">
    <figure markdown>
    ![MIDI Tutorial](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/4/0/8/midi-ports.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/midi-tutorial">**MIDI**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/8">
    <figure markdown>
    ![Serial Communication](https://cdn.sparkfun.com/c/264-148/assets/7/d/f/9/9/50d24be7ce395f1f6c000000.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/8">**Serial Communication**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/82">
    <figure markdown>
    ![I2C](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/8/2/I2C-Block-Diagram.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/82">**I2C**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/62">
    <figure markdown>
    ![Logic Levels](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/62">**Logic Levels**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/61">
    <figure markdown>
    ![Installing Arduino IDE](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/6/1/arduinoThumb.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/61">**Installing Arduino IDE**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/15">
    <figure markdown>
    ![Installing an Arduino Library](https://cdn.sparkfun.com/c/178-100/assets/b/e/4/b/2/50f04b99ce395fd95e000001.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/15">**Installing an Arduino Library**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/112">
    <figure markdown>
    ![Serial Terminal Basics](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/1/1/2/terminalThumb.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/112">**Serial Terminal Basics**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/664">
    <figure markdown>
    ![How to Work with Jumper Pads and PCB Traces](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/664">**How to Work with Jumper Pads and PCB Traces**
    </a>
</div>

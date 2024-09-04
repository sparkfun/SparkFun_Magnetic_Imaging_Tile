


The [SparkFun Magnetic Imaging Tile - 8x8](https://www.sparkfun.com/products/26092) uses an array of 64 hall effect sensors to convert magnetic fields to the visual spectrum. That's right! You can now see magnetic fields in real time! As is to be expected, there are caveats: the magnetic sensors used on the tile are some of the most sensitive on the market but you need to be within 1 to 2 centimeters of the tile to get a good image.

<div class="grid cards" style="width:500px; margin: 0 auto;" markdown>

-   <a href="https://www.sparkfun.com/products/26092">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/6/9/4/3/26943-Magnetic-Imaging-Tile-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Magnetic Imaging Tile - 8x8">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/26092">
      <b>SparkFun Magnetic Imaging Tile - 8x8</b>
      <br />
      SEN-26092
      <br />
      <center>[Purchase from SparkFun :fontawesome-solid-cart-plus:](https://www.sparkfun.com/products/26092){ .md-button .md-button--primary }</center>
    </a>
</div>

The demo shown in the animated GIFs don't quite give the Magnetic Imaging Tile justice! The frame rate of gifs is too low! Please see [Peter's demo video](https://www.youtube.com/watch?v=vxOuoWygxy0) for some amazing visuals.

<div style="text-align: center;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/vxOuoWygxy0?si=k2MAxdDgUQiwu3nT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

In this tutorial, we'll go over the hardware and how to hookup the sensor to an Arduino. We will also go over an Arduino and Processing example to get started.



### Required Materials

To follow along with this tutorial, you will need the following materials. You may not need everything though depending on what you have. Add it to your cart, read through the guide, and adjust the cart as necessary.



<div class="grid cards col-4" markdown>

<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/10215">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/4/5/5/8/10215-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="USB Micro-B Cable - 6 Foot">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/10215">
      <b>USB Micro-B Cable - 6 Foot</b>
      <br />
      CAB-10215
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14812">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/3/0/7/9/14812-SparkFun_RedBoard_Turbo_-_SAMD21_Development_Board-01b.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun RedBoard Turbo - SAMD21 Development Board">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14812">
      <b>SparkFun RedBoard Turbo - SAMD21 Development Board</b>
      <br />
      DEV-14812
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/26092">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/6/9/4/3/26943-Magnetic-Imaging-Tile-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Magnetic Imaging Tile - 8x8">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/26092">
      <b>SparkFun Magnetic Imaging Tile - 8x8</b>
      <br />
      SEN-26092
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/553">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/7/8/00553-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Break Away Male Headers - Right Angle">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/553">
      <b>Break Away Male Headers - Right Angle</b>
      <br />
      PRT-00553
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9140">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/2/5/5/7/09140-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wires Premium 6" M/F Pack of 10">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9140">
      <b>Jumper Wires Premium 6" M/F Pack of 10</b>
      <br />
      PRT-09140
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Other Microcontrollers

We'll be using the RedBoard Turbo - SAMD21 Development Board for the examples in this tutorial. The Arduino code also compatible with SAMD microcontrollers like the SAMD21 Dev Breakout, SAMD21 Mini Breakout, and SparkFun Thing Plus - SAMD51. You can also use a Teensy as well. Just make sure to solder headers (or wires) to the board and include a compatible USB cable with the development board.

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/13672">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/1/1/1/5/13672-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun SAMD21 Dev Breakout">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/13672">
      <b>SparkFun SAMD21 Dev Breakout</b>
      <br />
      DEV-13672
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/13664">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/1/0/9/2/13664-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun SAMD21 Mini Breakout">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/13664">
      <b>SparkFun SAMD21 Mini Breakout</b>
      <br />
      DEV-13664
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/16997">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/5/9/3/8/16997-Teensy_4.0_with_Headers-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Teensy 4.0 (Headers)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/16997">
      <b>Teensy 4.0 (Headers)</b>
      <br />
      DEV-16997
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14713">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/9/2/7/14713-SparkFun_Thing_Plus_-_SAMD51-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Thing Plus - SAMD51">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14713">
      <b>SparkFun Thing Plus - SAMD51</b>
      <br />
      DEV-14713
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>

While the ChipKit MAX32 is not listed in the SparkFun catalog, you can also use it with the Magnetic Imaging Tile.



### Tools

You will need a soldering iron, solder, and [general soldering accessories](https://www.sparkfun.com/categories/49) for a secure connection when using the plated through holes.

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/14456">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/1/2/4/9/0/14456-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Soldering Iron - 60W (Adjustable Temperature)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14456">
      <b>Soldering Iron - 60W (Adjustable Temperature)</b>
      <br />
      TOL-14456
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9163">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/5/8/7/09162-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Solder Lead Free - 15-gram Tube">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9163">
      <b>Solder Lead Free - 15-gram Tube</b>
      <br>
      TOL-09163
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11375">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/7/1/2/0/11375-Hook-Up_Wire_-_Assortment__Solid_Core__22_AWG_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Hook-Up Wire - Assortment (Stranded, 22 AWG)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11375">
      <b>Hook-Up Wire - Assortment (Stranded, 22 AWG)</b>
      <br />
      PRT-11375
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/12630">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/9/3/1/2/12630-Hakko-Wire-Strippers-30AWG-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Wire Strippers - 30AWG (Hakko)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12630">
      <b>Wire Strippers - 30AWG (Hakko)</b>
      <br />
      TOL-12630
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11952">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/4/2/2/11952-Hakko-Flush-Cutters-feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Flush Cutters - Hakko">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11952">
      <b>Flush Cutters - Hakko</b>
      <br />
      TOL-11952
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Prototyping Accessories

Depending on your setup, you may want to use IC hooks for a temporary connection. However, you will want to solder header pins to connect devices to the plated through holes for a secure connection. We opted for right angle headers for the SparkFun Magnetic Imaging Tile as well as M/F jumpers to connect to the SparkFun RedBoard Turbo - SAMD21 Development Board to reduce the amount of soldering.

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/12002">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/5/0/3/12002-Breadboard_-_Self-Adhesive__White_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Breadboard - Self-Adhesive (White)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12002">
      <b>Breadboard - Self-Adhesive (White)</b>
      <br />
      PRT-12002
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9741">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/6/9/6/09741-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="IC Hook with Pigtail">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9741">
      <b>IC Hook with Pigtail</b>
      <br>
      CAB-09741
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/553">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/7/8/00553-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Break Away Male Headers - Right Angle">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/553">
      <b>Break Away Male Headers - Right Angle</b>
      <br />
      PRT-00553
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9140">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/2/5/5/7/09140-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wires Premium 6" M/F Pack of 10">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9140">
      <b>Jumper Wires Premium 6" M/F Pack of 10</b>
      <br />
      PRT-09140
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Suggested Reading

If you aren’t familiar with the following concepts, we also recommend checking out a few of these tutorials before continuing.

<div class="grid cards col-4" markdown>

-   <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/5/Soldering_Action-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Solder: Through-Hole Soldering">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering">
      <b>How to Solder: Through-Hole Soldering</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/6/1/arduinoThumb.jpg" style="width:264px; height:148px; object-fit:contain;" alt="Installing Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <b>Installing Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/redboard-turbo-hookup-guide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/8/5/1/14812-SparkFun_RedBoard_Turbo_-_SAMD21_Development_Board-01.jpg" style="width:264px; height:148px; object-fit:contain;" alt="RedBoard Turbo Hookup Guide">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/redboard-turbo-hookup-guide">
      <b>RedBoard Turbo Hookup Guide</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG" style="width:264px; height:148px; object-fit:contain;" alt="Installing Board Definitions in the Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <b>Installing Board Definitions in the Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/serial-peripheral-interface-spi">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/1/6/spiThumb_Updated2.png" style="width:264px; height:148px; object-fit:contain;" alt="Serial Peripheral Interface (SPI)">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/serial-peripheral-interface-spi">
      <b>Serial Peripheral Interface (SPI)</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/logic-levels">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png" style="width:264px; height:148px; object-fit:contain;" alt="Logic Levels">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/logic-levels">
      <b>Logic Levels</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/analog-vs-digital">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/3/7/6/6/0/51c48875ce395f745a000000.png" style="width:264px; height:148px; object-fit:contain;" alt="Analog vs. Digital">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/analog-vs-digital">
      <b>Analog vs. Digital</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>

!!! note
    This is a collaboration with Peter Jansen of the "[Open Source Science Tricorder Project](http://www.tricorderproject.org/)". All credit goes to him! You can read about his work on the project on [Hack A Day](https://hackaday.io/project/18518-iteration-8/log/91551-a-third-high-speed-magnetic-imager-tile).

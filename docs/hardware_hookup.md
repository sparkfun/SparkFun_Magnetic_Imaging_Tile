### Connecting via PTH

For temporary connections to the PTHs, you could use IC hooks to test out the pins. However, you'll need to solder headers or wires of your choice to the board for a secure connection. You can choose between a combination of [header pins and jumper wires](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all), or [stripping wire and soldering the wire](https://learn.sparkfun.com/tutorials/working-with-wire/all) directly to the board.

<div class="grid cards col-2" markdown>

-   <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/5/Soldering_Action-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Solder: Through Hole Soldering">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <b>How to Solder: Through Hole Soldering</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->

-   <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/0/5/0/0/f/5138de3cce395fbb1b000002.JPG" style="width:264px; height:148px; object-fit:contain;" alt="Working with Wire">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <b>Working with Wire</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>

For the scope of this tutorial, we will use right angle, male headers. Insert the right angle headers on the top side and solder the header pins from the bottom. Of course, you can also insert the right angle header so that the pins face toward the multiplexors similar to Peter's demo video.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/26943_Magnetic_Imaging_Tile_Hall_Effect_Sensors_Soldering_Headers.jpg"><img src="../assets/img/26943_Magnetic_Imaging_Tile_Hall_Effect_Sensors_Soldering_Headers.jpg" width="600px" height="600px" alt="Headers Being Soldered to the Magnetic Imaging Tile"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Headers Being Soldered to the Magnetic Imaging Tile</i></td>
    </tr>
  </table>
</div>

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; border: solid 1px #cccccc;">Magnetic Imaging<br />Tile Pinout
            </th>
            <th style="text-align: center; border: solid 1px #cccccc;"> SAMD21 Pinout<br />(i.e. RedBoard Turbo, SAMD21 Mini, etc.)
            </th>
            <th style="text-align: center; border: solid 1px #cccccc;"> Teensy Pinout<br />(i.e. Teensy v3.1, v3.5, v4.0, v4.1, etc.)
            </th>
            <th style="text-align: center; border: solid 1px #cccccc;"> SAMD51 Pinout<br />(i.e. SAMD51 Thing Plus, etc.)
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
        </tr>
        <tr>        
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">OUT</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">A1</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">A1</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">A1</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#fff3cd"><font color="#000000">SCK</font>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#fff3cd"><font color="#000000">13</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#fff3cd"><font color="#000000">13</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#fff3cd"><font color="#000000">24</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">MISO</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">12</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">12</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">22</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">CS</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">10</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">10</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">10</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffffff"><font color="#000000">CLR</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffffff"><font color="#000000">8</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffffff"><font color="#000000">8</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffffff"><font color="#000000">5</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffdaaf"><font color="#000000">CLK</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffdaaf"><font color="#000000">9</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffdaaf"><font color="#000000">9</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffdaaf"><font color="#000000">9</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">3.3V</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">3V3</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">3.3V</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">3V3</font>
            </td>
        </tr>
    </table>
</div>

!!! note
    If you are using a development board with [updated SPI terminology](https://learn.sparkfun.com/tutorials/serial-peripheral-interface-spi/receiving-data), MISO may be labeled as POCI.

We will be using the RedBoard Turbo with female headers already installed on the board. For users that are using a different board, now would be a good time to solder headers or wires to the board. Below is an example with female headers soldered on the SAMD51 Thing Plus. Additionally, there are stackable headers soldered on the SAMD21 Mini Breakout so that the board can be inserted into a breadboard.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/26943_SAMD51_Thing_Plus_SAMD21_Mini_Breakout.jpg"><img src="../assets/img/26943_SAMD51_Thing_Plus_SAMD21_Mini_Breakout.jpg" width="600px" height="600px" alt="Headers soldered on the SAMD51 Thing Plus and SAMD21 Mini Breakout"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Headers soldered on the SAMD51 Thing Plus and SAMD21 Mini Breakout</i></td>
    </tr>
  </table>
</div>


### Connecting a Micrcontroller to the Magnetic Imaging Tile

We recommend using a microcontroller with sufficient RAM. While the example code can compile and function with Arduinos with an ATmega328P, the frames are limited. For the scope of the tutorial, we used a SAMD21. Of course, users can also use a Teensy and ChipKit as well.

Below is the Fritzing diagram of the RedBoard Turbo - SAMD21 connected to the Magnetic Imaging Tile.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/RedBoard_Turbo_SAMD21_Magnetic_Imaging Tile_bb.jpg"><img src="../assets/img/RedBoard_Turbo_SAMD21_Magnetic_Imaging Tile_bb.jpg" width="600px" height="600px" alt="Fritzing Diagram of RedBoard Turbo SAMD21 Connected to Magnetic Imaging Tile"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Fritzing Diagram of RedBoard Turbo SAMD21 Connected to Magnetic Imaging Tile</i></td>
    </tr>
  </table>
</div>


After soldering headers to the Magnetic Imaging Tile, wire the board to the RedBoard Turbo using jumper wires. Then connect a micro-b USB cable to power and program the RedBoard Turbo.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/26943-Magnetic_Imaging_Tile_Hall_Effect_Sensors_RedBoard_Turbo_SAMD51.jpg"><img src="../assets/img/26943-Magnetic_Imaging_Tile_Hall_Effect_Sensors_RedBoard_Turbo_SAMD51.jpg" width="600px" height="600px" alt="RedBoard Turbo - SAMD21 Connected to Magnetic Imaging Tile"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>RedBoard Turbo - SAMD21 Connected to Magnetic Imaging Tile</i></td>
    </tr>
  </table>
</div>

You can also connected any SAMD21 to the Magnetic Imaging Tile. Below shows a Fritzing diagram of the SAMD21 Mini Breakout connected to the Magnetic Imaging Tile. When using other development boards, you may need to solder additional headers or wires to the board. Depending on the microcontroller, you may also need to redefine the pins in the Arduino example code in order to properly connect to the SPI port.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/SAMD21_Mini_Breakout_Magnetic_Imaging Tile_bb.jpg"><img src="../assets/img/SAMD21_Mini_Breakout_Magnetic_Imaging Tile_bb.jpg" width="600px" height="600px" alt="Top View"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Fritzing Diagram of SparkFun SAMD21 Mini Breakout Board Connected to Magnetic Imaging Tile</i></td>
    </tr>
  </table>
</div>

After soldering headers (or wires) on your microcontroller and Magnetic Imaging Tile, wire the boards together. The connect a micro-b USB cable to power and program the SAMD21 Mini Breakout.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/26943_Magnetic_Imaging_Hall_Effect_Sensors_SAMD21_Mini_Breakout.jpg"><img src="../assets/img/26943_Magnetic_Imaging_Hall_Effect_Sensors_SAMD21_Mini_Breakout.jpg" width="600px" height="600px" alt="SAMD21 Mini Breakout Connected to Magnetic Imaging Tile"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>SAMD21 Mini Breakout Connected to Magnetic Imaging Tile</i></td>
    </tr>
  </table>
</div>

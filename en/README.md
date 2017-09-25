{% callout %}<b>Photosensitive Seizure Warning:</b> This project involves bright flashing lights! It may not be suitable if there are sufferers of epilepsy present.
{% endcallout %}

1. In this project you will sew LED lights to a t-shirt and program them to flash and change colours by writing code! 

2. The LEDs will be controlled by the Adafruit Flora. You may also use an Adafruit Gemma, LilyPad Arduino or LilyPad Arduino USB; some small code changes will be needed such as the number of the output pin and the board setup in the Arduino IDE.
 * _Note:_ the Gemma does not work with Linux. It also won't work with a USB 3.0 port, so you must have a USB 2.0 port or hub to connect the Gemma to the computer.

3. Download and install the Arduino IDE from [dojo.soy/wear2-arduino-ide](http://dojo.soy/wear2-arduino-ide). Once installed, open the application. There a few extra things needed to make it work for this project.

4. Open the **Preferences** from the **Arduino** menu. In the **Additional Board Manager URLs** box, paste the following and click OK.
   ```
      https://adafruit.github.io/arduino-board-index/package_adafruit_index.json
   ```

5. In the **Tools** menu, go to **Board** and select **Boards Manager...**. Choose **Contributed** from the dropdown. Install **Adafruit AVR Boards by Adafruit**. Click Close.

6. Quit and restart Arduino IDE. You should see the **Adafruit Flora** and the **Adafruit Gemma** listed in the **Boards** menu now as well as the **LilyPad Arduino** and **LilyPad Arduino USB**. Select the board you will be using.

7. In the **Sketch** menu, go to **Include Library** and select **Manage Libraries...**. Type `neopixel` into the search box. Install **Adafruit NeoPixel by Adafruit**. Click Close.

8. You will need the following hardware for this project
   * Adafruit Flora or Gemma and a USB cable
   * Around eight NeoPixels
   * Conductive thread
   * Three pairs of crocodile clips \(you can also use pieces of conductive thread instead, but crocodile clips are easier to test with\)
   * Optional: a battery pack will allow you to wear your finished project without being attached to the computer!
9. Other materials you will need are
   * An embroidery needle and scissors
   * A t-shirt
   * Clear nail polish
   * Optional: an embroidery hoop is recommended to make stitching up your circuit easier



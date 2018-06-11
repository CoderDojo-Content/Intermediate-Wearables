1. In Arduino IDE, click **File** &gt **New**. You will get a blank **sketch** that looks like this 
    ```
        void setup() {
            // put your setup code here, to run once:

        }

        void loop() {
            // put your main code here, to run repeatedly:

        }
    ```
    Any line that starts with `// ` is a **comment**. Comments are ignored by the computer. They're useful for making notes for yourself or other people reading the code.
2. Go to **Sketch** &gt **Include Library** and select **Adafruit NeoPixel**. Do you see this line of code added to the top of your sketch? `#include <Adafruit_NeoPixel.h>` Click at the end of this line and hit Return a few times to add some blank lines underneath.

3. Underneath the new line of code, type the following: `#define PIXELS_PIN 6` You are setting which pin of the Flora to use for **data** \(instructions\). That's the pin you connect the **data** pins of the pixels to, pin number 6.

4. Underneath that, type `#define NUM_PIXELS 8`. This is the number of NeoPixels you have. If you have a different number than 8, change it to the correct number.

5. Finally, underneath that, type 
    ``` 
        Adafruit_NeoPixel strip = Adafruit_NeoPixel(NUM_PIXELS, PIXELS_PIN, NEO_GRB + NEO_KHZ800);
    ```

6. Inside the _setup_ function, add the following two lines
    ``` 
        void setup() {
            // put your setup code here, to run once:
            strip.begin();
            strip.show();
        }
    ```
    * the code in the _setup_ function runs when the Flora starts

7. All the code in a **function** goes in between a pair of **curly braces** `{ }`. You're going to write your own **function** now. At the bottom of the sketch, click _after_ the `}` \(so, outside the _loop_ function\) and press Return a couple of times. Then type the following code:
    ``` 
        void lightPixel(uint16_t i, uint32_t c) {
            strip.setPixelColor(i, c);
            strip.show();
        }
    ```

8. Click **Verify** to compile your code and check for errors. If there are any mistakes you will need to fix the code and check again. Usually the errors tell you which line of code needs fixing. Check that you typed it exactly as shown!

9. Click inside the _loop_ function, in between the curly braces, and on a new line, type `lightPixel(0, strip.Color(0, 0, 255));`. Click **Verify** to compile again and make sure it's all correct.
 * this code **calls** the function you made. That means it tells the function to run. The bits inside the brackets are **parameters**: the information the function needs to run.

10. Let's plug in the Flora and run your code! Press the **reset** button on the Flora and then click the **Upload** button. When it's done, what happens?

11. Hopefully, you should see the first pixel light up blue. Let's do another! Inside the _loop_ function, type two more lines:
    ```
        lightPixel(1, strip.Color(0, 0, 255));
        lightPixel(2, strip.Color(0, 0, 255));
    ``` 

12. Verify and upload your code once more. This time you should see the first three pixels light up blue.

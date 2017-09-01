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

3. Underneath the new line of code, type the following: `#define PIXELS_PIN = 6` You are setting which pin of the Flora to use for **data** \(instructions\). That's the pin you connect the **data** pins of the pixels to, pin number 6.

4. Underneath that, type `#define NUM_PIXELS = 8`. This is the number of NeoPixels you have. If you have a different number than 8, change it to the correct number.

5. Finally, underneath that, type 
    ``` 
        Adafruit_NeoPixel strip = Adafruit_NeoPixel(NUM_PIXELS, PIXELS_PIN, NEO_GRB + NEO_KHZ800);
    ```
    to set up your chain of pixels, ready for coding!
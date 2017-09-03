1. Add the following new function to the end of your sketch. Don't worry, you don't have to understand it just now! It's borrowed from the example sketch you ran earlier. 
    ```
        uint32_t Wheel(byte WheelPos) {
            WheelPos = 255 - WheelPos;
            if(WheelPos < 85) {
                return strip.Color(255 - WheelPos * 3, 0, WheelPos * 3);
            }
            if(WheelPos < 170) {
                WheelPos -= 85;
                return strip.Color(0, WheelPos * 3, 255 - WheelPos * 3);
            }
            WheelPos -= 170;
            return strip.Color(WheelPos * 3, 255 - WheelPos * 3, 0);
        }
    ```
    * This function lets you choose any numer from 0 to 255 and it mixes a colour for you.

2. Now add another new function. See if you can spot the **loop** in it!
    ```
        void lightAllRainbow() {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, Wheel(((i * 256 / strip.numPixels())) & 255));
            }
            strip.show();
        }
    ```
    * There's a bit of math in here too! It's there to pick a nice selection of colours evenly from across the whole rainbow.

3. All that's left is to _call_ the function. Change the`loop` function so that it has just this line of code in it. Then verify and upload your sketch to see a lovely rainbow of colours
    ```
        void loop() {
            lightAllRainbow();
        }
    ``` 
    * Notice how you don't pass any **parameters** this time. That's because the new function figures out the colours for you!

    <!-- PICTURE HERE!! -->

4. How about adding a delay? Let's write a new function, that's similar to the one above but with a delay added to the loop so it animates:
    ```
        void animateRainbow(, uint8_t wait) {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, Wheel(((i * 256 / strip.numPixels())) & 255));
            strip.show();
            delay(wait);
            }
        }
    ```
    * Notice how the `strip.show()` has been moved inside the loop as well

5. Change the function call in the `loop` function:
    ```
        void loop() {
            animateRainbow(100);
        }
    ``` 

6. Have a go at putting together a sequence using a few function calls in the `loop` function. Experiment with different colours and `delay` lengths!  
    ```
        void loop() {
            lightAllOneColour(strip.Color(0, 0, 255));
            delay(100);
            turnAllOff();
            delay(100);
            lightAllOneColour(strip.Color(255, 0, 255));
            delay(100);
            turnAllOff();
            delay(100);
            lightAllOneColour(strip.Color(0, 255, 255));
            delay(100);
            turnAllOff();
            delay(100);
            lightAllOneColour(strip.Color(255, 255, 0));
            delay(100);
            turnAllOff();
            delay(100);
            animateRainbow(100);
            animateRainbow(100);
            animateRainbow(100);
        }
    ``` 
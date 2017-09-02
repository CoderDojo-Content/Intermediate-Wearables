1. Create the following new function after your first one:
    ``` 
        void lightAll(uint32_t c) {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, c);
                strip.show();
            }
        }
    ```

2. Delete the other lines in code in your _loop_ function, or **comment them out** \(so you can put them back in later if you want\). Your loop() code should look like this now:
    ```
        void loop() {
            // put your main code here, to run repeatedly:
            // lightPixel(0, strip.Color(0, 0, 255));
            // lightPixel(1, strip.Color(255, 0, 0));
            // lightPixel(2, strip.Color(0, 0, 255));

            lightAll(strip.Color(0, 0, 255));
        }
    ``` 
    * Remember the computer ignores comments! So the above code is the same as: 
        ```
            void loop() {
                lightAll(strip.Color(0, 0, 255));
            }
        ``` 

3. Verify and upload your code. What do you notice? This time you only needed to write _one line_ of code to call a function, and all of the pixels turned on. Take a look at your two functions, _lightPixel_ and _lightAll_. Can you spot the difference between them?

4. They both contain these two lines:
    ```
        strip.setPixelColor(i, c);
        strip.show();
    ```
    The first line tells Flora to set the colour of a particular pixel. `c` is the colour and `i` is which pixel. The second line sends the instructions out through Flora's pin and onto your pixels.

5. In your new function, can you see that those two lines of code are inside another pair of **curly braces**? This pair belongs to something called a **loop** \(but not the _loop_ function!\), rather than a function. It looks like this:
    ``` 
        for(uint16_t i=0; i<strip.numPixels(); i++) {
            
        }
    ```
The above code checks how many pixels are in your chain and then runs the code inside the curly braces that many times. 
 * _Here's the clever bit:_ The value of `i` starts off as zero and changes by one each time, so every time the line `strip.setPixelColor(i, c);` runs, it's setting the colour of the _next_ pixel!

6. Add the following new function to the end of your sketch. Don't worry, you don't have to understand it just now! It's borrowed from the example sketch you ran earlier. 
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

7. Now add another new function. See if you can spot the **loop** in it!
    ```
        void lightAllRainbow() {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, Wheel(((i * 256 / strip.numPixels())) & 255));
            }
            strip.show();
        }
    ```
    * There's a bit of math in here too! It's there to pick a nice selection of colours evenly from across the whole rainbow.

8. All that's left is to _call_ the function. Change the _loop_ function so that it has just this line of code in it:
    ```
        void loop() {
            lightAllRainbow();
        }
    ``` 
    * Notice how you don't pass any **parameters** this time. That's because the new function figures out the colours for you!


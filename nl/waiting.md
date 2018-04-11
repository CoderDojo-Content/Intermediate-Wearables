1. Let's write another function! It will be similar to the _lightAll_ function you wrote earlier, but with one extra line, and another **parameter** added.
    ```
        void animateAll(uint32_t c, uint8_t wait) {
        for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, c);
                strip.show();
                delay(wait);
            }
        }
    ```   

2. To call the function, change the line of code in _loop_: 
    ```
        void loop() {
             animateAll(strip.Color(0,0,255), 200);
        }
    ``` 

3. Verify and upload your code. Watch the pixels carefully! 

4. Yay, animation! However, once the lights are all on, you don't see the pattern repeat anymore because they never turn off. Add in the following new function:
    ```
        void turnOffAll(uint8_t wait) {
        for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, strip.Color(0,0,0));
                strip.show();
                delay(wait);
            }
        }
    ```
Then call the function by adding this new line inside the _loop_ function, underneath the line that's already there





Introduce delays, or turning off earlier and bring them back in here to animate?

"off and on"
can then also explain the actual function of the loop function (because it hasn't been mentioned at all and it should be!)
Also versus the setup function.
On second card, before bringing in colours

With just one extra line of code you can animate that rainbow! Add in a new line of code after `strip.show();` in the _lightAllRainbow_ function: `delay(500);`. Your function should now look like this:
    ```
        void lightAllRainbow() {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, Wheel(((i * 256 / strip.numPixels())) & 255));
                strip.show();
                delay(500);
            }
        }
    ```

2. Verify and upload the code again and watch

You've added in a **delay**
 * Whole card on delays?
 * also probably Animate. So call this card Animate instead of "what are you waiting for"


* yes and tie in with the animated wipe then
 * set all the pixels on to some colour ... animate with colorWipe? no, do animate on another card, loops can be one concept, delays another
 * choose different colours
 * set brightness as a final tweak

 * how does it behave with pixel index out of range? Two possible scenarios... index bigger than the length in code, index bigger than length in real life.
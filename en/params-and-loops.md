1. Create the following new function after your first one:
    ``` 
        void lightAllOneColour(uint32_t c) {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, c);
                strip.show();
            }
        }
    ```
    * This function takes a **parameter**: that's the bit inside the round brackets. It's some extra information that you give the function when you call it.

2. Delete the code in the `loop` function and add the following two calls to your new function:
    ```
        void loop() {
            lightAllOneColour(strip.Color(0, 0, 255));
            lightAllOneColour(strip.Color(0, 0, 0));
        }
    ``` 
    See how you're passing in a colour as a **parameter** to your function? This is the colour that gets used in place of `c` in the line `strip.setPixelColor(i, c);`. It means you can use the same function to make the pixels any colour, even to turn them all off!

3. Verify and upload your code. What do you notice? This time you only needed to write _one line_ of code that calls `strip.setPixelColor`, and all of the pixels turned on. 

4. Inside your new function, can you see that there is another pair of **curly braces** with some code in between? This pair belongs to something called a **for loop** \(but not the `loop` function!\), rather than a function. It looks like this:
    ``` 
        for(uint16_t i=0; i<strip.numPixels(); i++) {
            
        }
    ```
The above code checks how many pixels are in your chain and then runs the code inside the curly braces that many times. _Here's the clever bit:_ The value of `i` starts off as zero and changes by one each time, so every time the line `strip.setPixelColor(i, c);` runs, it's setting the colour of the _next_ pixel!

5. In your new `lightAllOneColour` function, add the following line after `strip.show();`
    ```
        delay(200);
    ```
    Make sure the new line is _before_ the `}`, so it's inside the loop. Your function should look like this now:
    ``` 
        void lightAllOneColour(uint32_t c) {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, c);
                strip.show();
                delay(150);
            }
        }
    ```

6. Verify your code again and upload the sketch to the Flora! Now you have a cool animated light sequence!

7. Let's add another **parameter** to this function, so you can choose different values for the `delay` when you call the function: 
    ``` 
        void lightAllOneColour(uint32_t c, uint8_t wait) {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, c);
                strip.show();
                delay(wait);
            }
        }
    ```

8. Change your `loop` function to look like this:
    ```
        void loop() {
            lightAllOneColour(strip.Color(0, 0, 255), 200);
            lightAllOneColour(strip.Color(255, 0, 255), 100);
            lightAllOneColour(strip.Color(255, 0, 0), 50);
        }
    ``` 
    Notice how you're passing in two **parameters** in the brackets now? The second one is the value for the `delay`.

9. Try as many colours as you like! Can you see how smaller or bigger numbers for the `delay` affect the speed of the animation?
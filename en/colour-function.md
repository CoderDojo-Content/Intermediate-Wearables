1. You're going to write your own **function** now. **Functions** keep your code tidy. At the bottom of the sketch, click _after_ the `}` \(so, outside the `loop` function\) and press Return a couple of times. Then type the following code:
    ``` 
        void lightAll() {
            strip.setPixelColor(0, strip.Color(0, 0, 255));
            strip.setPixelColor(1, strip.Color(0, 0, 255));
            strip.setPixelColor(2, strip.Color(0, 0, 255));
            strip.setPixelColor(3, strip.Color(0, 0, 255));
            strip.setPixelColor(4, strip.Color(0, 0, 255));
            strip.setPixelColor(5, strip.Color(0, 0, 255));
            strip.setPixelColor(6, strip.Color(0, 0, 255));
            strip.setPixelColor(7, strip.Color(0, 0, 255));
            strip.show();
        }
    ```
    All the code in a **function** goes in between a pair of **curly braces** `{ }`

2. Now change your _setup_ code so that it looks like this:
    ``` 
        void setup() {
            // put your setup code here, to run once:
            strip.begin();
            strip.show();
            lightAll();
        }
    ```
    The last line **calls** the function you made. That means it tells the function to run.

3. Verify and upload your sketch to the Flora. Did all the pixels light up blue?
 * You might have figured out that the first number in the line `strip.setPixelColor(0, strip.Color(0, 0, 255));` decides which pixel to light up. Have you noticed that the first pixel is zero instead of one? So if you have eight pixels the last one is number `7`.

4. Change the second line of the `lightAll` function from
    ```
        strip.setPixelColor(1, strip.Color(0, 0, 255));
    ``` 
    to
    ```
        strip.setPixelColor(1, strip.Color(255, 0, 0));
    ``` 
    Verify and upload the code to the Flora. Can you spot the difference?

5. On a computer, colours are made by mixing the three **primary colours of light**, _red_, _green_, and _blue_. You use numbers from `0` to `255` to say how much of each colour to mix. So the code `strip.Color(0, 0, 255)` makes _blue_ because the value for red and green are both zero. 
 * What colour do you think `strip.Color(0, 255, 0)` will give you? Try it out!

6. Here are a few more colours that are good to know
    ```
        void lightAll() {
            strip.setPixelColor(0, strip.Color(0, 0, 255)); // blue
            strip.setPixelColor(1, strip.Color(255, 0, 0)); // red
            strip.setPixelColor(2, strip.Color(0, 255, 0)); // green
            strip.setPixelColor(3, strip.Color(255, 0, 255)); // magenta
            strip.setPixelColor(4, strip.Color(255, 255, 255)); // white
            strip.setPixelColor(5, strip.Color(255, 255, 0)); // yellow
            strip.setPixelColor(6, strip.Color(0, 255, 255)); // cyan
            strip.setPixelColor(7, strip.Color(255, 127, 0)); // orange
            strip.show();
        }
    ``` 
    
7. Try experimenting with the numbers to get different shades. What do you think you will get if you set a value of `0` for all three colours, `strip.Color(0, 0, 0)`? 

8. Are you seeing stars yet?! Those NeoPixels sure are BRIGHT, aren't they! Luckily, if you want to, you can change the brightness of them with this code: `strip.setBrightness(10);` Add it to the _setup_ function, in between the lines `strip.begin();` and `strip.show();`. Just like with colours, the number can be anything from `0` to `255`.

9. You may find that the colours are not showing up properly towards the end of the chain. This is because the circuit is losing power due to **resistance** in the thread. You can add more power by stitching an extra thread along both the **negative** and the **positive** tracks in your circuit.


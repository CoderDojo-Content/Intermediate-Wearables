1. Change the second line of the `lightAll` function from
    ```
        strip.setPixelColor(1, strip.Color(0, 0, 255));
    ``` 
    to
    ```
        strip.setPixelColor(1, strip.Color(255, 0, 0));
    ``` 
    Verify and upload the code to the Flora. Can you spot the difference?

2. On a computer, colours are made by mixing the three primary colours of light, _red_, _green_, and _blue_. You use numbers from `0` to `255` to say how much of each colour to mix. So the code `strip.Color(0, 0, 255)` makes _blue_ because the value for red and green are both zero! 
 * What colour do you think `strip.Color(0, 255, 0)` will give you? Try it out!

3. Here are a few more colours to get you started
    ```
        void lightAll() {
            strip.setPixelColor(0, strip.Color(0, 0, 255));
            strip.setPixelColor(1, strip.Color(255, 0, 0));
            strip.setPixelColor(2, strip.Color(0, 0, 255));
            strip.setPixelColor(3, strip.Color(255, 0, 255));
            strip.setPixelColor(4, strip.Color(255, 255, 0));
            strip.setPixelColor(5, strip.Color(0, 255, 255));
            strip.setPixelColor(6, strip.Color(255, 127, 0));
            strip.setPixelColor(7, strip.Color(255, 127, 0)); ** TODO pick another colour with 3 **
            strip.show();
        }
    ``` 
    
4. Try experimenting with the numbers to get different shades. What do you think you will get if you mix the maximum value of all three colours, `strip.Color(255, 255, 255)`? 

5. Are you seeing stars yet?! Those NeoPixels sure are BRIGHT, aren't they! Luckily, if you want to, you can change the brightness of them with this code: `strip.setBrightness(10);` Add it to the _setup_ function, like this:
    ``` 
        void setup() {
            // put your setup code here, to run once:
            strip.begin();
            strip.show();
            strip.setBrightness(10);
        }
    ```
    * Just like with the colours, the number can be anything from `0` to `255`. I've used `10` which is very dim, almost off!



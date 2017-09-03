1. Change the second line of the _loop_ function from
    ```
        lightPixel(1, strip.Color(0, 0, 255));
    ``` 
    to
    ```
        lightPixel(1, strip.Color(255, 0, 0));
    ``` 

2. It should look like this now:
    ```
        void loop() {
            // put your main code here, to run repeatedly:
            lightPixel(0, strip.Color(0, 0, 255));
            lightPixel(1, strip.Color(255, 0, 0));
            lightPixel(2, strip.Color(0, 0, 255));
        }
    ``` 
    Verify and upload the code to the Flora. Can you work out what this code is doing?

3. Let's take a look at those **parameters** you're passing into your function \(remember, they're the bits of information inside the round brackets\).
    ```
        lightPixel(0, strip.Color(0, 0, 255));
    ```
    The first is a simple number. You might have figured out that it decides which pixel to light up! Have you noticed that the first pixel is zero instead of one?

3. The second **parameter** looks a bit more complicated, right? On a computer, colours are made by mixing the three primary colours of light, _red_, _green_, and _blue_. You use numbers from `0` to `255` to say how much of each colour to mix. So the code `strip.Color(0, 0, 255)` makes _blue_ because the value for red and green are both zero!

4. Here are a few basic colours to get you started
    ```
        void loop() {
            // put your main code here, to run repeatedly:
            lightPixel(0, strip.Color(0, 0, 255));
            lightPixel(1, strip.Color(255, 0, 0));
            lightPixel(2, strip.Color(0, 0, 255));
            lightPixel(3, strip.Color(255, 0, 255));
            lightPixel(4, strip.Color(255, 255, 0));
            lightPixel(5, strip.Color(0, 255, 255));
            lightPixel(6, strip.Color(255, 127, 0));
            lightPixel(7, strip.Color(255, 127, 0)); ** TODO pick another colour with 3 **
        }
    ``` 
    
4. Try experimenting with the numbers to get different shades. What do you think you will get if you mix the maximum value of all three colours, `strip.Color(255, 255, 255)`? How about a value of zero for all of them, `strip.Color(0, 0, 0)`?
 * Play around with the order of the colours by changing the value of the first **parameter**, the number that sets which pixel to light up. Remember, the pixels are numbered from `0`. So if you have eight pixels the last one is number `7`.

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





<!-- 1. Let's take a closer look at this code: `strip.setPixelColor(1, strip.Color(0, 0, 255));`. Change `strip.Color(0, 0, 255)` to `strip.Color(255, 0, 0)`.  -->

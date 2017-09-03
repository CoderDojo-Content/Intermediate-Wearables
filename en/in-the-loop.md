
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
    * All the code in a **function** goes in between a pair of **curly braces** `{ }`

2. Now change your _setup_ code so that it looks like this:
    ``` 
        void setup() {
            // put your setup code here, to run once:
            strip.begin();
            strip.show();
            lightAll();
        }
    ```
    * the last line **calls** the function you made. That means it tells the function to run.

3. Verify and upload your sketch to the Flora. Did all the pixels light up blue?
 * You might have figured out that the first number in the line `strip.setPixelColor(0, strip.Color(0, 0, 255));` decides which pixel to light up. Have you noticed that the first pixel is zero instead of one? So if you have eight pixels the last one is number `7`.

4. Let's write another function to turn all the pixels off! At the end of the sketch, type the following code. Make sure it's outside the `lightAll` function, so on a new line after the `}`.
     ``` 
        void turnAllOff() {
            strip.setPixelColor(0, strip.Color(0, 0, 0));
            strip.setPixelColor(1, strip.Color(0, 0, 0));
            strip.setPixelColor(2, strip.Color(0, 0, 0));
            strip.setPixelColor(3, strip.Color(0, 0, 0));
            strip.setPixelColor(4, strip.Color(0, 0, 0));
            strip.setPixelColor(5, strip.Color(0, 0, 0));
            strip.setPixelColor(6, strip.Color(0, 0, 0));
            strip.setPixelColor(7, strip.Color(0, 0, 0));
            strip.show();
        }
    ```

5. This time you will write code to call your functions in `loop` instead of in `setup`. Click inside the `loop` function, in between the curly braces, and type the following code:
    ```
        lightAll();
        delay(200);
        turnAllOff();
        delay(200);
    ```
    * What do you think `delay` does?

6. Delete the line `lightAll();` from inside the `setup` function. Verify and upload the code.
 * After the Flora has run all the code in the `setup` function, it then runs the `loop` function over and over again forever!

 7. Try putting in different values for the `delay`. For example, `delay(50);` or `delay(1000);`. Don't forget to verify and upload the code to test out your changes!

1. Create the following new function after your first one:
    ``` 
        void lightAllOneColour(uint32_t c) {
            strip.setPixelColor(0, c);
            strip.setPixelColor(1, c);
            strip.setPixelColor(2, c);
            strip.setPixelColor(3, c);
            strip.setPixelColor(4, c);
            strip.setPixelColor(5, c);
            strip.setPixelColor(6, c);
            strip.setPixelColor(7, c);
            strip.show();
        }
    ```
    * This function takes a **parameter**: that's the bit inside the round brackets. It's some extra information that you give the function when you call it.

2. This time you will write your function calls in **loop** instead of in **setup**. Click inside the **loop** function and add code so that it looks like this:
    ```
        void loop() {
            lightAllOneColour(strip.Color(0, 0, 255));
            delay(200);
            lightAllOneColour(strip.Color(0, 0, 0));
            delay(200);
        }
    ```
    See how you're passing in a colour as a **parameter** to your function? This is the colour that gets used in place of `c` in the line `strip.setPixelColor(i, c);`. It means you can use the same function to make the pixels any colour, even to turn them all off!

3. Delete the line `lightAll();` from inside the **setup** function. Verify and upload the code.
 * After the Flora has run all the code in the **setup** function, it then runs the **loop** function over and over again forever!

4. What do you think the **delay** function does? Try putting in different values for it's **parameter**. For example, `delay(50);` or `delay(1000);`. Don't forget to verify and upload the code to test out your changes!

5. Have you noticed that the colour `(0, 0, 0)` turns the pixels off? Try running the following code on the Flora:
    ```
        void loop() {
            lightAllOneColour(strip.Color(255, 0, 255));
            delay(500);
            lightAllOneColour(strip.Color(0, 0, 0));
            delay(500);
            lightAllOneColour(strip.Color(255, 127, 0));
            delay(500);
            lightAllOneColour(strip.Color(0, 0, 0));
            delay(500);
        }
    ```
    Now run the same code with the "off" colour:
    ```
        void loop() {
            lightAllOneColour(strip.Color(255, 0, 255));
            delay(500);
            lightAllOneColour(strip.Color(255, 127, 0));
            delay(500);
        }
    ```
    See the difference?

6. Try designing your own sequence by changing the code in the **loop** function! You can add as many delays and as many calls to your **lightAllOneColour** function as you like. Experiment with different values for the colour parameter.
 * Remember, the whole sequence will keep repeating over and over. 
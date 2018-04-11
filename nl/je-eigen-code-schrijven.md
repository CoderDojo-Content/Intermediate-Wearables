1. In Arduino IDE, klik op **Bestand** &gt; **Nieuw**. Je ziet een nieuwe **sketch** die er zo uit moet zien:

   ```
        void setup() {
            // put your setup code here, to run once:

        }
        void loop() {
            // put your main code here, to run repeatedly:

        }
   ```

   Elke regel die start met `//` is een **comment** \(= commentaar\). Comments worden door de computer genegeerd. Ze zijn handig om notities te maken voor jezelf of anderen.

2. Ga naar **Schets** &gt; **Bibliotheek gebruiken** en selecteer **Adafruit NeoPixel**. Je zou nu deze coderegel boven in je schets moeten zien: `#include <Adafruit_NeoPixel.h>`. Klik aan het eind van die regel en klik een paar keer op Enter om een paar blanco regels in te voegen.

3. Onder deze nieuwe coderegel typ je `#define PIXELS_PIN 6`. Je vertelt nu welke pin van de Flora gebruikt gaat worden voor **data** \(instructies\). Dit is de pin die de **data** pinnen van de pixels verbindt: pin nummer 6. 

4. Daaronder typ je `#define NUM_PIXELS 8`. Dit is het aantal NeoPixels dat je gebruikt. Als je een ander aantal dan 8 gebruikt, typ dan dat getal.

5. Tenslotte typ je deze regel:

   ```
        Adafruit_NeoPixel strip = Adafruit_NeoPixel(NUM_PIXELS, PIXELS_PIN, NEO_GRB + NEO_KHZ800);
   ```

6. Binnen de _setup_ functie voeg je de volgende twee coderegels toe:

   ```
        void setup() {
            // put your setup code here, to run once:
            strip.begin();
            strip.show();
        }
   ```

   * de code in de _setup_ functie wordt uitgevoerd als de Flora opstart.

7. Na `strip.show();` klik je op Enter en typ je vervolgens deze twee regels:

   ```
        strip.setPixelColor(0, strip.Color(0, 0, 255));
        strip.show();
   ```

8. Klik op **Verifiëren** om je code te compileren en op fouten na te kijken. Als er fouten zijn, verbeter ze dan. Meestal zie je staan in welke regel de fout zit. Zorg dat je precies typt wat er in deze kaarten staat!

9. Koppel Flora aan je computer en voer je code uit. Klik op de **reset** knop op de Flora en dan op de **Upload **knop. Wat gebeurt er als het uploaden klaar is?

10. Hopelijk licht de eerste pixel blauw op. Nu gaan we de volgende doen! Boven de tweede `strip.show();` typ je de volgende twee regels:

    ```
        strip.setPixelColor(1, strip.Color(0, 0, 255));
        strip.setPixelColor(2, strip.Color(0, 0, 255));
    ```

11. De _setup_ functie zou er nu zo uit moeten zien:

    ```
        void setup() {
            // put your setup code here, to run once:
            strip.begin();
            strip.show();
            strip.setPixelColor(0, strip.Color(0, 0, 255));
            strip.setPixelColor(1, strip.Color(0, 0, 255));
            strip.setPixelColor(2, strip.Color(0, 0, 255));
            strip.show();
        }
    ```

    Snap je wat deze code doet?

12. Verifieer en upload je code. Nu zouden de eerste drie pixels blauw moeten oplichten. Schrijf zelf de coderegels voor de andere pixels!![](assets/threeBlue_150_800.png)




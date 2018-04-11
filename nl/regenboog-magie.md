1. Voeg de volgende nieuwe functie toe aan het eind van je schets. Geen zorgen, je hoeft het niet meteen te begrijpen! het komt uit de voorbeeldschets die je eerder hebt gebruikt.

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

   Deze functie laat je elk getal tussen 0 en 255 kiezen en mengt een kleur voor je.

2. Voeg nu deze nieuwe functie toe. Zie je de **for loop** daarin?

   ```
        void lightAllRainbow() {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, Wheel(((i * 256 / strip.numPixels())) & 255));
                strip.show();
            }
        }
   ```

   Hier zit ook wat wiskunde in! Het kiest een fraaie selectie van kleuren uit de hele regenboog.

3. Nu hoef je de functie alleen nog maar _aan te roepen_. Verander de `loop` functie zodat deze coderegel erin zit. Verifieer en upload dan de schets om een prachtige regenboog aan kleuren te zien.

   ```
        void loop() {
            lightAllRainbow();
        }
   ```

   Je hoeft geen **parameters** in te voeren omdat de nieuwe functie de kleuren voor je uitzoekt!

4. En nog een delay toevoegen? Schrijf een nieuwe functie die lijkt op die hierboven maar met een delay toegevoegd in de loop zodat het animeert:

   ```
        void animateRainbow(uint8_t wait) {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, Wheel(((i * 256 / strip.numPixels())) & 255));
                strip.show();
                delay(wait);
            }
        }
   ```

5. Verander de functieaanroep in de `loop `functie en voeg een tweede regel toe om je andere animatiefunctie aan te roepen:

   ```
        void loop() {
            animateRainbow(100);
            animateOneColour(strip.Color(0, 0, 0), 100);
        }
   ```

   Probeer het uit op de Flora!

6. Combineer verschillende aanroepen in de `animateRainbow` functie en je andere functies. Jouw fantasie is eindeloos! Je kunt heel veel gave dingen doen met de trucjes die je geleerd hebt met kleuren, loops en delays. Als je meer voorbeelden wilt, kijk je in de **strandtest** schets die je gebruikt hebt om de NeoPixels te testen.  
   ![](assets/rainbowSmile_200_800.png)

7. Als je van plan bent om je project te dragen, kun je een batterijhouder gebruiken. Een houder met 3xAA, 3xAAA of een knoopbatterij werkt goed op de Flora. Kijk op [dojo.soy/wear2-flora-power](http://dojo.soy/wear2-flora-power) voor meer informatie. Gebruik je niet de Flora maar een ander board kijk dan na wat die nodig hebben.




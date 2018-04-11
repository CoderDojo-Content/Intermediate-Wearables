1. Maak de volgende nieuwe functie aan het eind van je schets:

   ```
        void animateOneColour(uint32_t c, uint8_t wait) {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, c);
                strip.show();
            }
        }
   ```

   * Zie je dat deze functie _twee _**parameters** heeft? Je gebruikt de tweede pas later.

2. Verwijder \(of **comment out**!\) de code in de `loop` functie en schrijf een nieuwe aanroep voor je nieuwe functie:

   ```
        void loop() {
            animateOneColour(strip.Color(0, 0, 255), 100);
        }
   ```

   Zie je hoe je twee **parameters** binnen de haakjes zet? De tweede wordt nu nog niet gebruikt, maar de code zal niet compileren als je geen waarde voor alle **parameters **invult als je de functie aanroept.

3. Verifieer en upload je code. Wat zie je? Nu hoefde je maar _één regel_ te schrijven die `strip.setPixelColor` aanriep en alle pixels aanzette.

4. Binnen je nieuwe functie, zie je dat er nog een paar **accolades** staan met wat code? Dit paar behoort toe aan een **for loop** \(= voor lus; maar niet de `loop` functie!\), en niet aan een functie. Het ziet er zo uit:

   ```
        for(uint16_t i=0; i<strip.numPixels(); i++) {

        }
   ```

   De code hierboven kijkt na hoeveel pixels er in je keten zitten en voert dan de code binnen de accolades dat aantal keer uit. _Dit is er nou zo handig aan: _de waarde van` i `begint bij nul en verandert elke keer met één, dus elke keer dat de regel `strip.setPixelColour (i, c);` uitgevoerd wordt, bepaalt het de kleur van de _volgende_ pixel!

5. Nu gaan we wat met de tweede **parameter **doen! In je nieuwe `animateOneColour` functie voeg je de volgende regel toe na `strip.show();`

   ```
        delay(wait);
   ```

   Zorg ervoor dat de nieuwe regel _vóór_ de` }` staat, dus binnen de loop. Je code zou er nu zo uit moeten zien:

   ```
        void animateOneColour(uint32_t c, uint8_t wait) {
            for(uint16_t i=0; i<strip.numPixels(); i++) {
                strip.setPixelColor(i, c);
                strip.show();
                delay(wait);
            }
        }
   ```

   Je gebruikt nu geen getal voor de delay, maar de tweede **parameter** van je functie. Dit betekent dat je verschillende waarden voor de `delay` kunt kiezen als je de functie aanroept.

6. Voeg nog een aanroep toe aan je functie binnen `loop`, om de lichtjes uit en aan te zetten:

   ```
        void loop() {
            animateOneColour(strip.Color(0, 0, 255), 100);
            animateOneColour(strip.Color(0, 0, 0), 100);
        }
   ```

7. Verifieer je code weer en upload de schets naar je Flora. Nu heb je een gave geanimeerde reeks!

8. Je hoeft de pixels natuurlijk niet uit te zetten. Waarom niet een reeks kleuren achter elkaar animeren?

   ```
        void loop() {
            animateOneColour(strip.Color(255, 127, 0), 100);
            animateOneColour(strip.Color(255, 0, 255), 100);
            animateOneColour(strip.Color(0, 255, 255), 100);
        }
   ```

   Voeg zoveel kleuren toe als je wilt. Verander ook de waarden van de tweede **parameter** van `100` naar iets anders en zie hoe je animatie sneller of langzamer gaat!




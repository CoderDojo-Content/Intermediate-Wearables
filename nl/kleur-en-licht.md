1. Je gaat nu je eigen **function** \(= functie\) schrijven. **Functions** houden je code netjes. Onderaan de schets, klik _na_ de } \(dus buiten de `loop` functie\) en klik een paar keer op Enter. typ nu de volgende code:

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

   Alle code binnen een **function **wordt binnen **accolades** { } gezet.

2. Verander nu je _setup_ code zodat het er zo uit ziet:

   ```
        void setup() {
            // put your setup code here, to run once:
            strip.begin();
            strip.show();
            lightAll();
        }
   ```

   De laatste regel **roept** de function die je gemaakt hebt **aan**. Het vertelt de functie om te beginnen.

3. Verifieer en upload je schets naar Flora. Lichten alle pixels blauw op?

   * Je zult vast gezien hebben dat het eerste getal in de regel `strip.setPixelColor(0, strip.Color(0, 0, 255)); `bepaalt welke pixel oplicht. Zie je dat de eerste pixel nul is in plaats van één? Dus als je acht pixels hebt is je laatste getal `7`.

4. Verander de tweede regel van `lightAll `functie van

   ```
        strip.setPixelColor(1, strip.Color(0, 0, 255));
   ```

   naar

   ```
        strip.setPixelColor(1, strip.Color(255, 0, 0));
   ```

   Verifieer en upload je code naar Flora. Zie je het verschil?

5. Op een computer worden kleuren gemaakt door de drie **primaire kleuren van licht**, _rood_, _groen_ en _blauw_ te mengen. Je gebruikt getallen van `0` tot `255` om te vertellen hoeveel van elke kleur gemengd moet worden. Dus de code `strip.Color(0, 0, 255)` maakt _blauw_ omdat de waarden van rood en groen beide nul zijn.

   * Welke kleur geeft `strip.Color(0, 255, 0)` denk je? Probeer het uit!

6. Hier zijn nog wat kleuren die handig zijn om te weten:

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

7. Experimenteer met de getallen voor verschillende kleuren. Wat denk je dat er gebeurt als je de waarde op `0` zet voor alle kleuren `strip.Color(0, 0, 0)`?

8. Zie je al sterretjes?! NeoPixels zijn echt FEL, niet waar! Gelukkig kun je de felheid van de pixels veranderen met deze code: `strip.setBrightness(10);`. Voeg het toe aan de _setup_ functie, tussen de regels `strip.begin();` en `strip.show();`. Net als met kleuren kun je getallen tussen `0` en `255` gebruiken.

9. Het kan zijn dat de kleuren er aan het eind van de keten niet zo goed uitzien. Dat komt omdat het circuit aan kracht verliest door **weerstand** in de draad. Je kunt meer kracht toevoegen door een extra draad te naaien langs zowel de **negatieve **als **positieve **lijnen in je circuit.




1. Schrijf deze nieuwe functie na je eerste:

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

   * Deze functie neemt een **parameter**: dat is het stukje binnen de ronde haakjes \( \). Het is wat extra informatie die je aan de functie geeft als je het aanroept.

2. Nu ga je een functie schrijven die **loop** \(= lus\) heet in plaats van **setup**. Klik binnen de **loop** functie en voeg code toe zodat het er zo uit ziet:

   ```
        void loop() {
            lightAllOneColour(strip.Color(0, 0, 255));
            delay(200);
            lightAllOneColour(strip.Color(0, 0, 0));
            delay(200);
        }
   ```

   Zie je hoe je een kleur als **parameter** in je functie zet? Dit is de kleur die gebruikt wordt in plaats van `c` op elke regel van je functie` lightAllOneColour`. Dit betekent dat je dezelfde functie kunt gebruiken om pixels elke kleur te laten zijn, zelfs om ze allemaal uit te zetten!

3. Verwijder de regel `lightAll();` in de **setup** functie. Verifieer en upload de code.

   * Als Flora start, loopt het alle code binnen de **setup** functie eerst door en blijft dan de **loop** functie eeuwig herhalen!

4. Wat denk je dat de **delay **\(= uitstel\) functie doet? Zet daar eens verschillende waarden in de **parameter**, bijvoorbeeld `delay(50);` or `delay(1000);`. Vergeet niet om je code te verifiëren en uploaden om je aanpassingen te testen!

5. Is het je opgevallen dat de kleur `(0, 0, 0)` alle pixels uitzet? Probeer de volgende code uit op je Flora:

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

   Voer nu dezelfde code uit zonder de "uit" kleur:

   ```
        void loop() {
            lightAllOneColour(strip.Color(255, 0, 255));
            delay(500);
            lightAllOneColour(strip.Color(255, 127, 0));
            delay(500);
        }
   ```

   Zie je het verschil?

6. Probeer je eigen regels te schrijven door de code in de **loop** functie te veranderen! Je kunt zoveel delays en calls aan je **lightAllOneColour** toevoegen als je zelf wilt. Experimenteer met langere en kortere delays en verschillende waarden voor de kleurparameters.

   * onthoud: de hele reeks wordt continu herhaald. 




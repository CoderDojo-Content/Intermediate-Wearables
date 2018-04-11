1. Voordat je begint is het handig om je NeoPixels te testen. Open Arduino IDE. Kijk nog even na welk board je gebruikt. In de voorbeelden gebruiken we _Adafruit Flora_.

2. Ga naar **Bestand**, selecteer **Voorbeelden** en zoek **Adafruit NeoPixel** \(let op: deze kan helemaal onderaan staan!\) en kies **strandtest**.

3. Een nieuw scherm wordt geopend. Het codebestand heet een **schets** in Arduino IDE. Zoek deze coderegel:

   ```
      Adafruit_NeoPixel strip = Adafruit_NeoPixel(60, PIN, NEO_GRB + NEO_KHZ800);
   ```

4. Verander het eerste getal naar `1`. Nu moet de code er zo uitzien:

   ```
      Adafruit_NeoPixel strip = Adafruit_NeoPixel(1, PIN, NEO_GRB + NEO_KHZ800);
   ```

5. Klik op **Bestand** &gt; **Opslaan als**. Typ een naam voor jouw schets en sla het op.

6. Boven in je **schets** klik je op **Verifiëren**. Onderin je scherm moet komen te staan "Compileren voltooid" wat betekent dat de code juist is **gecompileerd** \(zo niet, dan zie je hier de foutmeldingen. Je moet de fouten dan gaan verbeteren\).  
    ![](assets/verifyIcon.png)

7. Nu gaan we uploaden! Koppel je Flora aan de computer. Druk op de **reset** knop op de Flora en dan _meteen_, terwijl het rode lichtje knippert, klik je op het pijlicoon om de code naar je Flora te uploaden. Het rode lichtje moet knipperen, gevolgd door twee oranje lichtjes op de Flora. Als het klaar is, zou de tekst "Upload voltooid" te zien moeten zijn onderin je schets.  
   ![](assets/upload3_120_800.png)

   * Soms lukt het uploaden niet meteen. Zorg dat het juiste board geselecteerd is, dat je USB kabel werkt en goed gekoppeld zit. Dan gaat het alleen nog om timing! Je krijgt het vanzelf voor elkaar.

8. Koppel Flora los van je computer \(de aan/uit knop op een Flora kan gebruikt worden als deze is aangesloten op een batterijhouder, maar werkt niet als de Flora via USB aan een computer gekoppeld is\).

   * Koppel Flora los of zet het uit voordat je andere onderdelen vast- of loskoppelt zodat er niets beschadigt!

9. Klem drie krokodillenklemmen aan de **GND**, **\#6** en **VBATT** pinnen.  
   ![](assets/crocsFlora_169_800.png)

10. Pak een NeoPixel en verbind de **GND** draad aan de **-** pin. Verbind de **\#6** aan de **data in** pin: dit is de pin met de pijl die naar binnen wijst op de NeoPixel. Verbind tenslotte de **VBATT** aan de **+** pin.  
    ![](assets/crocsPixel_169_800.png)

11. Klaar? Zet Flora weer aan en zie hoe je NeoPixel oplicht en in meerdere kleuren knippert!

12. Test al je NeoPixels door ze aan te sluiten zoals beschreven bij stap 10. Onthoud dat je Flora** uitzet** voor de de draden vast- of loskoppelt!

13. Als je de NeoPixels getest hebt, verander je de code naar het aantal pixels dat je gaat gebruiken. Ik gebruik er acht:

    ```
      Adafruit_NeoPixel strip = Adafruit_NeoPixel(8, PIN, NEO_GRB + NEO_KHZ800);
    ```

14. Klik op **Verifieer** en **upload** de nieuwe code naar je Flora. Nu gaan we een NeoPixel circuit maken!




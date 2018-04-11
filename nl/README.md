{% callout %}<b>Waarschuwing:</b> In dit project wordt gewerkt met knipperende lichten wat gevolgen zou kunnen hebben voor mensen met lichtgevoelige epilepsie.
{% endcallout %}

1. In dit project naai je LED lampjes op een t-shirt en programmeer je ze om te knipperen en van kleur te veranderen! 

2. De LEDs worden aangestuurd door de Adafruit Flora. Je kunt ook de Adafruit Gemma, LilyPad Arduino of LilyPad Arduino USB gebruiken. Het kan dan wel voorkomen dat de code dan aangepast moet worden (bijv. de output pin en de configuratie van het board in Arduino IDE).
 * _NB:_ De Gemma werkt niet met Linux, en ook niet op een USB 3.0 poort. Zorg dan voor een USB 2.0 poort of connectie.

3. Donwload en installeer Arduino IDE via [dojo.soy/wear2-arduino-ide](http://dojo.soy/wear2-arduino-ide). Open het programma als het geïnstalleerd is. Er volgen nog wat extra zaken die nodig zijn voor dit project.

4. Open in het menu **Bestand** de **Voorkeuren**. Zet bij **Additionele Bordenbeheer URLS** het volgende neer en klik dan op OK.
   ```
      https://adafruit.github.io/arduino-board-index/package_adafruit_index.json
   ```

5. Ga naar het **Hulpmiddelen** menu, dan naar **Board "Adafruit Flora"** en dan naar **Bordenbeheer**. Bij **Type** klik je op **Bijgedragen**. Installeer **Adafruit AVR boards by Adafruit**. Klik daarna op "Sluiten".

6. Sluit Arduino IDE af en start het opnieuw. Bij Boards zou je nu moeten zien: **Adafruit Flora**, **Adafruit Gemma**, **LilyPad Arduino** en **LilyPad Arduino USB**. Selecteer het board dat je gaat gebruiken.

7. Ga naar het **Schets** menu, dan naar **Bibliotheek gebruiken**. Klik op **Bibliotheken beheren** en in het zoekvenster typ je `neopixel`. Installeer **Adafruit NeoPixel by Adafruit**. Klik daarna op "Sluiten".

8. Je hebt de volgende materialen nodig voor dit project
   * Adafruit Flora of Gemma en een USB kabel
   * Acht NeoPixels
   * Geleidend draad
   * Drie krokodillenklemmen \(je kunt ook stukjes geleidend draad gebruiken, maar krokodillenklemmen werken makkelijk voor het testen\)
   * Optioneel: een batterijhouder en knoopbatterij zodat je je project kunt dragen zonder aan de computer vast te zitten!
   * Naald en schaar
   * Een t-shirt
   * Blanco nagellak
   * Optioneel: een borduurring om het naaien van je circuit makkelijker te maken



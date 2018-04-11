1. Verzamel je NeoPixels en pak textielkrijt of een viltstift. Leg een t-shirt \(of een ander stuk stof dat je voor je project gebruikt\) op een vlakke ondergrond. Leg de pixels in de vorm die jij wilt. Ik ga een lachend gezichtje maken! Andere ideeën zijn:

   * Een rechte lijn
   * Een hart \(daar kun je 8 NeoPixels goed voor gebruiken\)
   * Nep "knopen" aan de voorkant van een t-shirt

2. Bepaal waar je Flora moet komen en kies een NeoPixel waar je Flora aan wilt koppelen: deze ga je er als eerste opnaaien. De rest wordt door een keten aan elkaar gekoppeld. Je zou een ononderbroken lijn moeten kunnen volgen met je vinger: zodanig dat de lijn zich nergens kruist \(kortsluiting!\).

3. Teken de buiten- en binnenkant met textielkrijt en markeer waar elke NeoPixel komt.  
   ![](assets/drawAroundShape_178_800.png)

4. Klaar om te gaan naaien? Als je alles gemarkeerd hebt, leg de spullen dan aan de kant en pak naald en geleidedraad. Als je pixels dicht bij elkaar liggen dan zou 20 cm draad genoeg moeten zijn. Als je een borduurring hebt dan kan dat het naaien een stuk makkelijker maken.

5. Eerst ga je de **data** lijn naaien. Leg de eerste pixel op zijn plek met de pijltjes in de richting van waar de tweede pixel moet komen. Zet de eerste pixel vast met de pin met de pijl die **weg **wijst van de LED in het midden. Dit is de **output **pin.

   * Zet drie of vier steken door de pin om hem goed aan de stof vast te zetten.

6. Gebruik een rijgsteek tot je bij de plek komt waar je tweede pixel komt. Pak dan die tweede pixel en leg het op de juiste plek, met de pijltjes wijzend naar de plek van de derde pixel.

7. Naai de tweede pixel vast via de **input** pin \(onthoud: dit is de pin waar de pijl **naar** de LED in het midden wijst\). Zet de draad vast met een paar steken aan de achterkant van de stof en knip het restant af.

   * Tip: gebruik blanco nagellak om de draadeinden vast te zetten; zo zal het niet gaan rafelen en kunnen losse draadjes geen kortsluiting veroorzaken.

8. Gebruik een _nieuw stuk geleidedraad_, verbind de **output** pin van de tweede pixel aan de **input **pin van de derde pixel. Ga zo door tot alle pixels aan elkaar zitten via hun **data** pins. Gebruik steeds een nieuwe draad tussen de pixels.

   * De keten stopt bij de laatste pixel; je zet niets vast aan diens **output** pin.
     ![](assets/pixelSewing3_136_800.png)

9. Nu ga je alle **negatieve** pins in de keten verbinden, gebruik hiervoor een stuk draad van 50-100 cm. Naai een paar strakke steken door elke - pin van elke pixel. Begin bij de eerste en eindig bij de laatste. gebruik een rijgsteek tussen de pixels.

   * Zorg dat deze draad nergens de **data **draad raakt!

10. Gebruik een lang stuk draad om alle **+** pinnen van de pixels te verbinden, net zoals je de **-** pinnen in stap 9 verbonden hebt.

11. Tot slot leg je de Flora op je t-shirt \(zorg dat Flora _niet_ aanstaat!\). Gebruik drie verschillende stukken geleidedraad. Verbind de **\#6** pin aan de **input**, de **GND** pin aan de **-** en de **VBATT** pin aan de **+** pin van de eerste NeoPixel. Gebruik weer een rijgsteek. Zorg dat geen van de draden elkaar raken. Je kunt andere pins van de Flora met gewoon naaigaren vastzetten op de stof om het steviger op zijn plek te zetten.  
    ![](assets/stitchedCircuit_200_800.png)

12. Het moment van de waarheid: tijd om je Flora aan te zetten! Schrik niet als niet alle pixels oplichten. Dat kan veroorzaakt worden door: 
    * Kortsluiting: raken draden elkaar? Raakt iets van metaal de stof of het circuit? Is de stof nat?
    * Losse verbindingen: de steken aan elke pin moeten stevig vastzitten voor een goede verbinding.
    * Juiste code ge-upload: heeft je code het juiste aantal pixels? Is de code geverifieerd en ge-upload zonder foutmeldingen?




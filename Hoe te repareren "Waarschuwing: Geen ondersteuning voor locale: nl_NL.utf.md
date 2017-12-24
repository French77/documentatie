#### Linux Mint 17&18 bevatten enkele wijzigingen met betrekking tot de ondersteuning van de lokale taal en de manier waarop deze is ingesteld. Als gevolg hiervan ziet u de volgende waarschuwing, bijvoorbeeld bij het uitvoeren van `update-initramfs`
- Waarschuwing: No support for locale: nl_NL.utf8

Dit komt omdat `locale-gen` een archiefbestand gebruikt om alle landinstellingen in op te slaan, maar veel hulpprogramma's zijn nog steeds op zoek naar de locale bestanden
Kijk eens naar > ``ls /usr/lib/locale/``. 
- Als je uitvoer er uitziet zoals hieronder is weergegeven, lees dan verder:

 `ls /usr/lib/locale/
C.UTF-8  locale-archive`

De waarschuwing is niet kritiek , maar als het je stoort of problemen veroorzaakt, geef dan in de terminalvenster onderstaand commando in:
> ``sudo locale-gen --purge --no-archive``

Met deze opdracht wordt het archiefbestand verwijderd en vervangen door de .utf8-bestanden,zie afbeelding hieronder

![Screenshot](https://i.imgur.com/5VyVxm4.png"Screenshot") 

 #### Opmerking: de onderstaande uitvoer laat de Engelse en Nederlandse locale bestanden zien, eigen uitvoer kan verschillen afhankelijk van de talen die er zijn geselecteerd.
 ![Screenshot](https://i.imgur.com/5vPsjzm.png"Screenshot") 
 
Daarna kan je e.v.t onderstaand commando ingeven in de terminal,ter controle 
> ``sudo update-initramfs -u``
 
![](https://img.shields.io/badge/Linux-CC0-brightgreen.svg?style=social&label=Afbeeldingen)

#### Probleem na activeren Radiotray is het 2e icon niet zichtbaar in het systeemvak Linux Mint Cinnamon.
Na ``sudo apt install radiotray python-xdg`` nog steeds geen 2e icon zichtbaar,probleem doet zich kennelijk voor in de configuratie i.c.m appindicator.
#### Oplossing is door appindicator in het config.xml bestand te vervangen door systray.
##### Open de terminal in geef onderstaande code in om het bestand config.xml te openen:
``gksudo xed ~/.local/share/radiotray/config.xml``

![Screenshot](https://i.imgur.com/kVtbn4D.png"Screenshot")

##### Verander bij `option name="gui_engine"` de waarde naar value="systray"
##### Vervolgens na aanpassing het config.xml bestand opslaan.

2e icon ![Screenshot](https://i.imgur.com/v6CrEm3.png"Screenshot") is nu zichtbaar en radiozenders kunnen worden geactiveerd en bewerkt.

###### Van belang is wel dat systeemvak onder hulptoepassingen toevoegen aan paneel (Rechter muisklik op paneel) wordt geactiveerd.

![](https://img.shields.io/badge/Linux-CC0-brightgreen.svg?style=social&label=Afbeeldingen)



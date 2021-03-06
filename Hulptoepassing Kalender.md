#### Ga naar:
- ``/home/gebruikers_naam/.cinnamon/configs/calendar@cinnamon.org folder``
- ``Open het .json bestand``
- ``Verander in de sectie custom-format de waarde ("value")  naar bv:``
- ``"%H:%M:%S\n%A %x Week %V" ``

`custom-format": {
        "type": "entry",
        "default": "%A %B %e, %H:%M",
        "description": "Date format",
        "indent": true,
        "dependency": "use-custom-format",
        "tooltip": "Set your custom format here.",
  "value": "%H:%M:%S\n%A %x Week %V"`
  
 #### Syntax datum/tijd opmaak 
 - %H:%M:%S%n%A %d-%m-%Y Week %V
 #### Na aanpassing zal kalender applet er als volgt zo uitzien in je werk/taakbalk.
![Screenshot](https://i.imgur.com/J4sai44.png"Screenshot")


**Is de uitlijning niet naar wens in de werk/taakbalk (kan aan het gebruikte thema liggen)**
- rechter muisklik op een leeg veld in de werk/taakbalk
- paneelinstellingen => kiezen voor aangepaste werk/taakbalk en Cinnamon toestaan om de uitlijning te laten instellen m.b.v schuifbalk.

**Wil je het nu geheel anders weergeven hieronder een lijst met karakters voor tijd en datum die je kunt toepassen** 
####  Combinatie van een van de volgende onderstaande karakters is mogelijk: ####
 

- %%    Een letterlijke %
- %a    Afkorting weekdag naam (bijvoorbeeld Zon)
- %A    Volledige weekdag naam (bijvoorbeeld zondag)
- %b    Afkorting maand naam (bijvoorbeeld Sept)
- %B    Volledige maand naam (bijvoorbeeld September)
- %c    Datum en tijd(b.v,Don Maart 3 23:05:25 2005)
- %C    Eeuw; zoals in %Y, behalve de laatste twee cijfers (bijvoorbeeld 21)
- %d    Dag vd maand(b.v, 01)
- %D    Datum; hetzelfde als %m/%d/%y
- %e    Dag van de maand, met tussenruimte; hetzelfde als %d maar zonder toonaangevende 0 
- %F    Volledige datum; hetzelfde als %Y-%m-%d
- %g    laatste twee cijfers van het jaar van het ISO weeknummer (zie% G)
- %G    jaar van het ISO weeknummer (zie %V); gewoonlijk alleen bruikbaar met %V
- %h    Hetzelfde als %b
- %H    Uur (00..23)
- %I    Uur (01..12)
- %j    Dag van het jaar (001..366)
- %k    Uur ( 0..23)
- %l    Uur ( 1..12)
- %m    Maand (01..12)
- %M    Minuten (00..59)
- %n    Een nieuwe lijn
- %N    Nanoseconden (000000000..999999999)
- %p    Equivalent van ofwel AM of PM; leeg indien niet bekend
- %P    Hetzelfde als %p, maar met kleine letters
- %r    12 uurs kloktijd (bijvoorbeeld 11:11:04)
- %R    24 uurs kloktijd (bijvoorbeeld 21:11:04)
- %s    Seconden sinds 1970-01-01 00:00:00 UTC
- %S    Seconden (00..60)
- %t    Een tab
- %T    Tijd; hetzelfde als %H:%M:%S
- %u    Dag vd week (1..7); 1 is Maandag
- %U    Weeknummer van het jaar, met zondag als eerste dag van de week (00..53)
- %V    ISO weeknummer, met maandag als eerste dag van de week (01..53)
- %w    Dag van de week (0..6); 0 is zondag 
- %W    Weeknummer van het jaar, met maandag als eerste dag van de week (00..53)
- %x    Datum representatie (bijvoorbeeld 12/31/99)
- %X    Tijd representatie (bijvoorbeeld 23:13:48)
- %y    Laatste twee cijfers van het jaar (00..99)
- %Y    Jaar

####       Mogelijkheden om numerieke tijdzone weer te geven ####
- %z    +hhmm numerieke tijdzone (bijvoorbeeld -0400)
- %:z    +hh:mm numerieke tijdzone (bijvoorbeeld -04:00)
- %::z    +hh:mm:ss numerieke tijdzone (bijvoorbeeld -04:00:00)  
- %:::z    Numerieke tijdzone (bijvoorbeeld -04, +05: 30)

- %Z     Alfabetische tijdzoneafkorting (bijvoorbeeld CEST)

<<<<<<< HEAD
# js.poll-calibrate-shp13-iobroker (Version 0.2)
Dieses Script ermöglicht es, unzählige Bewegungsmelder, Schaltaktoren (Steckdosen, Lampen, etc.) und Lichtsensoren im ioBroker miteinander zu verknüpfen

## Was sollte beachtet werden und was ist möglich?
Der timeout beginnt erst dann zu laufen, wenn der Datenpunkt "motion" des jeweiligen Bewegungsmelders den Wert "false" zurückgibt. Sollten mehrere Bewegungsmelder eine Lampe schalten, wird gewartet bis alle BWM "false" melden. <br>
*Hinweis*: Die Einschaltdauer sollte nicht nur wenige Sekunden betragen, da einige Bewegungsmelder einen cooldown haben, bevor sie wieder Bewegungen erkennen und melden. Da führt dazu, dass eventuell Lampen bei zu kurzer Einschaltdauer ausschalten, obwohl man noch im Raum ist! <br>
Wird ein Lichtsensor verwendet, kann man ihn pro Bewegungsmelder zuordnen. Auch kann man die Einschaltdauer pro Lampe einzeln festlegen. Das Script ist modular aufgebaut, d.h. es kann jeder Bewegungsmelder mit jeder Lampe (auch mehreren) gekoppelt werden. Das gleiche gilt für Lichtsensoren. <br>


## Script-Updates einspielen
- Das Script ist so aufgebaut, dass Updates keinen Einfluss auf eure Geräteliste haben. Ihr müsst eure Geräte nur einmal anlegen und das wars dann auch schon. Die folgende Zeile gibt euch einen Hinweis darauf, ab wo ihr das Script bei einem Update kopieren und wieder einfügen müsst. <br>
  ![update_Zeile.png](/admin/update_Zeile.png)
 <br>


# Anleitung
## Script erstellen
Ein neues JS Script in iobroker erstellen und das Script aus "script-bwm-script.js" kopieren und einfügen. <br>

![erstellung_1.png](/admin/erstellung_1.png) <br>
![erstellung_2.png](/admin/erstellung_2.png) <br>

## Einstellungen

![Einstellungen.png](/admin/Einstellungen.png)

**faktor**: Hier wird der Kalibrierfaktor in Dezimalform eingegeben <br>
**poll**: Zeit in Millisekunden, wie oft die Werte geholt werden sollen. Nicht weniger als 10000 eingeben, da sonst die Belastung für das System unnötig hoch wird<br>
**inst**: Zigbee Instanz, in der eure Geräte betrieben werden (Standard "zigbee.0")<br>
**arr**:
{/* wama */ id: '588e81fffed3904d', newPath: '0_userdata.0.Verbrauch.gerechnet.Wama' },<br>

/ *NAME EURES DEVICES* / (Ist nur ein Kommentar und hat keinen Einfluss auf das Skript)<br>
**id**: 'HIER DIE ID DES BLITZWOLF GERÄTES EINGEBEN',
**newPath**: 'HIER DEN PFAD ZUM NEUEN KALIBRIERTEN DP ANGEBEN' <- Wird dann automatisch neu erstellt!





**Falls euch meine Arbeit gefällt :** <br>

[![Paypal Donation](https://img.shields.io/badge/paypal-donate%20%7C%20spenden-blue.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=3EYML5A4EMJCW&source=url)




## Changelog

### 0.2 (2020-12-11)
* (xenon-s) Änderung des Triggernamens

### 0.1 (2020-12-11)
* (xenon-s) initial commit


# License
MIT License

Copyright (c) 2020 xenon-s<br>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:<br>

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.<br>

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.<br>

=======
einfach das Script aus script.txt in ein neues ioBroker JS importieren

const arr = [
    // id: -> Name aus dem zigbee adapter
    // newPath: -> neuer Pfad mit kalibrierten werten
    
    {/* wama */ id: '588e81fffed3904d', newPath: '0_userdata.0.Verbrauch.gerechnet.Wama' },
    {/*trockner*/ id: '842e14fffe3a4bb3', newPath: '0_userdata.0.Verbrauch.gerechnet.Trockner' },
];
>>>>>>> main

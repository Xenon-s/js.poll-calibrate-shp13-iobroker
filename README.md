# js.poll-calibrate-shp13-iobroker (Version 0.2)
Dieses Skript ermöglicht es, die Daten von Blitzwolf SHP13 zu pollen und zu kalibrieren (im ioBroker)

# Anleitung
## Script erstellen
Ein neues JS Script in iobroker erstellen und das [Script V 0.2](https://raw.githubusercontent.com/Xenon-s/js.poll-calibrate-shp13-iobroker/main/script.txt) kopieren und einfügen. <br>

![erstellung_1.png](/admin/erstellung_1.png) <br>
![erstellung_2.png](/admin/erstellung_2.png) <br>

## Einstellungen

![einstellungen.png](/admin/einstellungen.png)

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




Karten
Allgemeine Informationen
Eine Karte, wie sie in einem Pudu Kettybot gespeichert ist, ist eine digitale Repräsentation der Umgebung, die der Roboter für Navigation nutzt. Karten enthalten Wegpunkte und andere Knoten.

| Bild einer Karte im PuduInstaller oder im MapingTool |

Wegpunkte
Wegpunkte sind für den Roboter Ziele, zu denen er fahren kann. Diese werden im
»Serviermenü« des Roboters angezeigt und lassen sich als eine Reihe von Zielen auswählen, zu denen der Roboter nacheinander hinfahren wird, bevor er wieder zur Ursprungsposition zurückfährt. Für Pudu Kettybots können bis zu »3« Wegpunkte für eine Tour ausgewählt werden.

| Bild von Serviermenü mit möglichen Wegpunkten |

Karten erstellen
Voraussetzungen
Damit ein Kettybot eine Karte erstellen bzw. einscannen kann, ist zwingend eine Installation eines Markers nötig.

| Bild eines Markers an der Decke oder als Sticker |

Der Marker markiert den Startpunkt bzw. Rastplatz der bzw. des Kettybots.

Erstellung mithilfe des »MappingTools«
Um eine Karte zu erstellen wird das »MappingTool« auf den Kettybots verwendet.

Das »MappingTool« kann durch folgenden Pfad gestartet werden:
Einstellungen → Debug-Menü (Standardpasswort: pudupw) → »MappingTool«

| Bild des Mapping Tools |

Durch einen Klick auf »‚Neue Karte erstellen‘« kann nun eine neue Karte gescannt werden.

Führe den Roboter zur Startposition und folge den Anweisungen des Kettybots.
|| Bild von roboter, über ihm ist der marker

Der Roboter kann nun langsam vom Benutzer geschoben werden, wobei der gesamte Bereich der Karte abgefahren werden sollte, die der Roboter später befahren soll. Wichtig ist hier, dass der abgefahrene Weg im Kettybot als potentielle Route gespeichert wird. Deshalb muss sichergestellt werden, dass die abgefahrene Routen immer zugänglich sind. Falls zu einem späteren Zeitpunkt Gegenstände wie zum Beispiel Stühle die abgefahrenen Routen blockieren, kann dies zu Problemen führen. Zum Beispiel kann der Kettybot beim Befahren einer blockierten Route sich so verhalten, dass er nicht zum Ziel findet und auch keine anderen Routen in Betracht zieht.

Während dem Abfahren der Route kann der Benutzer Wegpunkte hinzufügen, die später als Ziele zur Verfügung stehen. Dazu positioniert der Benutzer den Kettybot an den gewünschten Wegpunkt und fügt diesen über die Benutzerfläche des »MappingTools« dem Roboter hinzu.

| Bild, wie man einen Wegpunkt hinzufügen kann |

Falls alle Bereiche der Karte abgefahren wurde, muss der Roboter wieder an die Startposition zurückgeschoben werden. Daraufhin kann der Benutzer den Kartenerstellungsvorgang abschließen und bestätigen.

Nach dem Bestätigen der Karte und einem Neustart des Kettybots ist die soeben eingescannte Karte ausgewählt. Allerdings sind die Wegpunkte der Karte nicht als Ziele für den Roboter auswählbar. Dies liegt daran, da kein Pickup Location-Knoten auf der Karte existiert.

Bearbeiten von Karten mithilfe des »PuduInstallers«
Um einen Pickup Location-Knoten der Karte hinzuzufügen und weitere Modifikationen vornehmen zu können, wie zum Beispiel das nachträgliche Hinzufügen von Wegpunkten, wird die PuduInstaller Software verwendet.

| Bild des PuduInstallers |

Um auf dem Kettybot erstellte Karten mit der Software bearbeiten zu können, müssen diese erst von dem Roboter auf den Rechner übertragen werden. Dazu müssen sich der Rechner und der Kettybot im selben Netzwerk befinden. Außerdem muss die Funktion »xyz« auf dem Kettybot aktiviert sein. Dies kann über folgenden Pfad aktiviert werden:

Einstellungen → Debug-Menü → »xyz« anschalten

|Bild vom Switch|

Im PuduInstaller kann nun sich nun über
»ADB → ???«
mit dem Kettybot verbunden werden.
|Bild von Kettybot verbindung|

»mögl. Hier weitere beschreibung«

Anschließend kann über Pull and load map Button die gewünschte Karte des Kettybots auf den Rechner übertragen und bearbeitet werden.

| Bild der Karte im PuduInstaller |

Auf der geöffneten Karte sind nun einige Elemente zu erkennen:
• Routen (blau)
• Wegpunkte (orange)

Um die Karte verwenden zu können, muss ein Pickup Location-Knoten aus dem linken Menü ausgewählt werden, und zur Karte hinzugefügt werden. Idealerweise wird dieser direkt bei der Startposition der Karte platziert.

| Bild der Karte im PuduInstaller mit Pickup Location |

Über das linke Menü können außerdem neue Wegpunkte bzw. Ziele der Karte hinzugefügt werden.

Wenn die Karte wie gewünscht angepasst wurde, kann diese über den Button Send map an den Kettybot geschickt werden. Stelle hierbei sicher, dass PuduInstaller immer noch mit dem Kettybot verbunden ist. Wähle dann »PuduBot« aus, um die Karte zu übertragen.

| Bild von PuduInstaller mit SendMap und der übersicht mit blauen buttons |

Nach einem Neustart des Kettybots ist die aktualisierte Karte einsatzbereit.

Über diesen Weg können auch Karten, die auf einem Kettybot erstellt wurden an andere Kettybots übertragen werden. Dies ist wichtig, wenn man mehrere Kettybots zusammen auf der selben Karte betreiben möchte.


Vorgang bei Kartenerstellung
Zunächst wurde eine Karte für das »Nao-Labor« (A333) erstellt. Hier waren bereits Marker angebracht.
| Bild marker in A333 |

Dazu wurde der Roboter durch den Raum geschoben, um diesen vollständig einzuscannen. Jedoch wurden hier auch Wege abgefahren, die in der normalen Konfiguration des Raums durch Stühle blockiert waren. Dies führte zu den oben genannten Problemen.
Außerdem wurde mithilfe der PuduInstaller Software ein neuer Wegpunkt hinzugefügt und die Karte an die anderen Kettybots übertragen.

Um eine weitere Umgebung (Mensa) als Karte zu erstellen, waren einige Workarouds notwendig. Zunächst ist der Kettybot an dem Marker der ausgewählten Karte gebunden. Als der Roboter zur Mensa geschoben wurde und daraufhin gestartet wurde, war der Marker der alten Karte nicht mehr für den Kettybot sichtbar, was zur Folge hatte, dass sämtliche Einstellungen inklusive der Funktion der Kartenerstellung nicht zur Verfügung standen. Den Roboter auf Werkseinstellungen zurückzusetzen war nicht ohne weiteres möglich.
Dieses Problem wurde gelöst, in dem der Roboter unter dem Marker der alten Karte gestartet wurde und dann zur neuen Umgebung transportiert wurde. Dadurch blieb die Funktion, neue Karten und somit einen neuen Marker einzuscannen, erhalten.
Nach dem Einscannen der Mensaumgebung konnte der Kettybot normal auf der neuen Karte eingesetzt werden.

| Bild der Mensakarte |




• Karten allgemein
    ◦ Was sind Karten?
        ▪ Allgemein
        ▪ Enthalten Wegpunkte zu dem ein Kettybot fahren kann
        ▪ Enthalten Routen
        ▪ || Bild von Karte im PuduInstaller oder KettybotTool
    ◦ Wo werden Karten gespeichert?
        ▪ Auf Kettybots
            • || Bild von Kartenübersicht eines der Kettybots
        ▪ Werden auch in die Cloud geladen
        ▪ Können auch auf den PC gezogen werden
            • Welches Format haben Karten?
• Karten erstellen
    ◦ Voraussetzungen
        ▪ Marker an der Decke
            • || Bild von Marker an der Decke oder auf Sticker
        ▪ » Abstand?
        ▪ » …
    ◦ Karte mit Pudu Kettybot erstellen
        ▪ Kartentool starten
            • || Bild → debug menü → kartentool → neu?
        ▪ Roboter an Start bringen (wo der Marker hängt)
            • || Bild von roboter, über ihm ist der marker
        ▪ Roboter alle Bereiche der Karte abfahren, die der Roboter später befahren kann
            • Wichtig: Der abgefahrene Weg wird im Kettybot als potentielle Route gespeichert und muss immer zugänglich sein.
                ◦ Falls später Stühle oder ähnliche Gegenstände die Route blockieren führt dies zu Problemen (Kettybot blockiert)
        ▪ Wegpunkte hinzufügen
            • || Bild von interface, wo man wegpunkte hinzufügen kann
        ▪ Roboter wieder an Start führen
    ◦ Karte mit PuduInstaller auf Rechner übertragen
        ▪ Pudu Kettybot muss im selben Netzwerk sein wie rechner
        ▪ Der eine Switch muss aktiviert sein
            • || Bild vom Switch
        ▪ in PuduInstaller mit Kettybot verbinden
            • ||  Bild anleitung
        ▪ Karte ziehen
            • || Bild
    ◦ Karte im PuduInstaller Map-Editor bearbeiten
        ▪ Karte öffnen
            • || Bild
        ▪ Wegpunkte hinzufügen
            • || Bild
        ▪ » Entrypoint setzen
            • || Bild
    ◦ Karte hochladen
        ▪ Karte auf Kettybot laden
            • || Bild
        ▪ Karten zwischen Pudu Kettybots übertragen
• Vorgang bei Kartenerstellung
    ◦ Zuerst Nao-Labor als Karte erstellt
        ▪ || Bild von Karte
        ▪ Marker war schon installiert
            • || Bild von Marker
        ▪ Wie oben beschrieben
        ▪ Dann im Karteneditor
            • Neuer Wegpunkt
            • Startpunkt
            • || Bild von Editor
        ▪ »? Versucht neue routen hinzuzufügen, hat nicht geklappt
    ◦ Karte in der Mensa
        ▪ Marker installieren
            • || Bild maker
        ▪ pudu karte abfahren
        ▪ wegpunkte hinzufügen
        ▪ » …
        ▪ || Bild von Karte in Puduinstaller

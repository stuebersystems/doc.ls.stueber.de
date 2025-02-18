# ASDPC-Schnittstelle

Hier finden Sie die jeweils aktuellste Version zur ASDPC-Schnittstelle **inklusiver aller kurzfristig veröffentlichten Korrekturen während einer Statistikphase**.

## Download der aktuellen Schnittstelle

Sollte die aktuelle Schnittstelle bereits in einem Serviceupdate veröffentlicht sein, dann zeigt der Link des Schnittstellenpakets auf unsere Downloadseite.

### Änderung 2024-11-19

* CHANGE: Ab Magellan 11.0.11 => Für Bildungsgänge, die mit `A12` beginnen, werden die nachfolgenden Felder nicht automatisch von uns vorbesetzt, sondern mit dem Wert, der im Feld `Laufbahn > Versetzungsart` gewählt wurde, gefüllt.
  * Neuzugang
  * Neuzugang an gleicher Schule


### Schnittstellenpaket - 08.09.2022

[Downloadlink](https://my.hidrive.com/share/neqlm8tqnv)

!!! info "Hinweis"

    Eine Anleitung zum Austausch der einzelnen Dateien finden Sie im Abschnitt ["Wie Dateien ausgetauscht werden"](#wie-dateien-ausgetauscht-werden)!

#### Aktuelle Änderungen

* FIX: NRW => SIM.TXT ist ein Schüler zugleich Nebenschüler und Stammschüler wird er in der SIM.txt mit zwei Datensätzen mit den unterschiedlichen Klassen ausgegeben
* FIX: NRW => SIM.TXT Herkunftschule bei Schülerstatus Neuzugang
* FIX: NRW => SIM.TXT Schüler wird als Abgänger erkann, wenn Schüler > Laufbahn > Abschluss > Abschluss 1 ein Wert eingetragen ist und nicht mehr nur wenn der Wert auf 0A gesetzt ist

---

#### Letztes Serviceupdate - 9.0.7 (23.08.2022)

* FIX: NRW => Ausspielen der Grundschulempfehlung für GE und GY korrigiert
* NEW: NRW ABS => Neuer Katalog: AS_Bewerbungsempfehlungen.keys

---

## Wie Dateien ausgetauscht werden

!!! warning "Wichtig"

    Vorausgesetzt wird immer die zuletzt veröffentlichte Programmversion. Liegt das letzte Änderungsdatum vor dem Veröffentlichungsdatum unserer Standardausgabe, sind die Änderungen für die Schnittstelle alle im Standardupdate mit enthalten! Das Ausgabedatum der letzten Magellan-Version sehen Sie in unserer [Changelog-Datei](https://doc.magellan.stueber.de/changelog/changelog/).

Was soll getauscht werden | Anmerkungen
------------------------- | -----------
**Pfade in Magellan**     | Die entsprechenden Pfade zu Ihren Dokumenten, Skripten und Importdateien können Sie im Magellan-Administrator unter `Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner` einsehen.
**Schlüssel**             | Dateien mit der Endung **\*.keys** sind Ihre Schlüsseldateien für den Import der aktuellen Statistikschlüssel. Diese gehören auf den Serverrechner in den dortigen Unterordner Importe\Nordrhein-Westfalen.<br><br>Fügen Sie diese Dateien dort ein und überschreiben Sie ggf. bereits existierende Schlüsseldateien. Anschließend lesen Sie die Schlüssel über den Magellan-Administrator unter `Datenimporte > Schlüsselverzeichnisse importieren > Nordrhein-Westfalen > Ihre Schulart` ein. Sie können alle Schlüsseldateien importieren oder auch nur eine Datei, dazu ändern Sie "alle Kataloge" ab und wählen gezielt die gewünschte Importdatei.
**Skripte**               | **\*.dws oder \*.int**  Dateien mit der Endung **\*.dws oder \*.int** gehören auf den Serverrechner in den dortigen Unterordner Skripte \(**Achtung**: Nicht in den Bundesland-Unterordner, sondern direkt in den Skripteordner\).<br/><br/>**\*.xml** Dateien mit der Endung **\*.xml** gehören auf den Serverrechner in den dortigen Unterordner Skripte\Nordrhein-Westfalen. Bitte beachten Sie, dass die Dateien mit diesem Schritt lediglich hinterlegt sind und erst noch in Ihren Datenbank importiert werden müssen. Eine Anleitung zum Schlüsselimport finden Sie [hier](https://doc.ls.stueber.de/schluesselverzeichnisse/).
**Magellan.exe**          | Das Nutzen einer neuen Magellan.exe setzt mindestens die aktuellste Version voraus. Das letzte und aktuelle Serviceupdate finden Sie in unseren [Downloads](http://magellan.stueber.de/download.php).<b/r><br/>Nehmen Sie die Arbeiten mit der Schnittstelle in der Schule an der aktuellen Datenbank vor oder in einer zweiten Umgebung, also zum Beispiel auf einem Extrarechner, auf den die Datenbank übertragen wird? Wenn Sie es im Schulnetzwerk machen, dann müssten bitte die Rechner alle \(erst der Server, dann die Arbeitsplätze\) auf die aktuelle Version aktualisiert werden, anschließend fügen Sie diese Magellan.exe auf dem Rechner ins Programmverzeichnis ein, auf dem Sie die Schnittstelle ausführen möchten. Nutzen Sie ein Zweitsystem aktualisieren Sie diesen Rechner und ersetzen dann bitte die Magellan.exe mit der neuen Datei.<br/><br/>Die Magellan.exe finden Sie bei 64-Bit Betriebssystemen unter `C:\Program Files \(x86\)\Stueber Systems\Magellan 8`, bei 32 Bit Betriebssystemen unter `C:\Programme\Stueber Systems\Magellan 8`.

---

## Archiv

---

### Schnittstellenpaket ABS/BBS 2019 - 19-09-2019

* FIX: ABI.TXT - Ausgabe der Abiturnote im Format n.n (Punkt)
* FIX: ABI.TXT - Zeugnis wird jetzt korrekt, entsprechend der Dokumentation ausgespielt.

---

### Serviceupdate - 17.09.2019

* FIX: SIM.TXT - LSSchulform wurde nicht korrekt ausgelesen. Das führte zu Leereinträgen in der Spalte.
* FIX: SIM.TXT - LSKlassenart wurde nicht ausgespielt, sondern nur ausgelesen. Das führte bei den Datensatzsarten: "Neuzugang" und "Neuzugang an gleicher Schule" dazu, dass eine Spalte in der Zeile fehlte.
* FIX: SIM.TXT - Adressmerkmal wird zwar nicht benötigt wurde aber auch nicht als Leerfeld (Nur Trennzeichen) ausgespielt.
* FIX: SIM.TXT - Die Kopfzeilen für Adressmerkmal und Internat am Ende der SIM.TXT haben gefehlt
* CHANGE: SIM.TXT - Die beiden Spalten `Produktname` und `Produktversion` dienen lediglich Supportzwecken. Beide Informationen wurden in die Spalte Produktname verschoben. In der Spalte `Produktversion` geben wir jetzt die Datensatzart aus, dies hilft dem Support bei der Suche nach Problemlösungen.
* CHANGE: Kein Fehler aber eine Eingabehilfe. Einige Kunden geben keine Versetzungart ein, sondern setzen lediglich das Merkmal Versetzt. Wir tragen dem Folge und berechnen entsprechend die Versetzung anders als zuvor. Nachzulesen in der Dokumentation unter [SIM.TXT - Dateneingabe - Feld "Versetzung"](https://doc.ls.stueber.de/nordrhein-westfalen/schuelerdaten/#dateneingabe).

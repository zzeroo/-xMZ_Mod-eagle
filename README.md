# xMZ-Mod-Touch Eagle Files

Eagle files for the 'xMZ-Mod-Touch' project.

# Material Listen (BOM)

Die Material Listen werden aus den Eagle Zeichnungen gewonnen. Hierzu werden in
Eagle zunächst über den "design link" alle Bauteile in der Farnell Datenbank
gesucht.
Anschließend wird diese Liste gespeichert.

* Datei: "Deckelplatine $VERSION-order.txt"

Danach wird das bom.ulp in Eagle ausgeführt. Folgende Einstellungen sind zu
wählen:

	Listen-Typ: Werte (Häckchen unter "Attribute auflisten" setzen)
	Ausgabeformat: CSV

Diese Datei wird ebenfalls gespeichert.

* Datei: "Deckelplatine $VERSION BOM.csv"

### Farnell BOM Import

Farnell bietet die Möglichkeit über eine Web GUI die BOM Daten in eine
Bestellung umzuwandeln.

Format der CSV Datei für den Import:
- 3 Spalten
"Anzahl	Ordercode	Beschreibung"
- Dateiformat .xls


#Produktionsdaten
## Boardlayout Dateien

Einige der wichtigsten Ebenen (Drill, Solder, Paste) wurden einzeln mit der
Document (Layer 48) Ebene als PDF gedruckt

gs -dBATCH -dNOPAUSE -q -sDEVICE=pdfwrite -sOutputFile=Bodenplatine.pdf \
"Bodenplatine Dimensions.pdf" \
"Bodenplatine Placement TOP.pdf" \
"Bodenplatine PCB: TOP Layer.pdf" \
"Bodenplatine PCB: BOTTOM Layer.pdf" \
"Bodenplatine TOP Paste.pdf" \
"Bodenplatine TOP Solder Mask.pdf" \
"Bodenplatine Drill Drawing.pdf"


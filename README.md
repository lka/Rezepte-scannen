# Rezepte-scannen
Lasten-/Pflichtenheft um Rezepte zu scannen und mit KI zu verarbeiten

# Lastenheft
## Ziel
Die Erweiterung einer Sammlung von Kochrezepten, die in Zeitschriften vorliegen, die ich aber in meiner App "My Recipe Box" (ehemals "recette-tec") haben möchte.

## Voraussetzungen
- Ein DIN A4 Flachbett-Scanner, eingestellt auf 300 dpi und jpeg mit hoher Auflösung (keine Kompression). Das Scan Ziel ist ein Eingangs Verzeichnis unterhalb von Rezepte im Dokumenten Ordner, das Format ist PDF. Das gescannte Dokument ist also unter [User]\Dokumente\Rezepte\Eingang\scan_yyyymmddMMss.pdf zu finden.
- Ein Windows 11 PC für die Verarbeitung und als HTML-Server für die erstellten Kochrezepte.
- Ein Tablet mit der App "My Recipe Box".

## Arbeitsweise
- Scannen des Dokumentes mit dem gewünschten Kochrezept.
- Starten der KI und Ausführung des vorgegebenen Prompts "Rezept scannen".
- Starten des HTTP Servers.
- Importieren des Rezeptes mit dem Tablet und der Importfunktion von "My Recipe Box".

# Pflichtenheft
## KI Funktionen
### Verwendung einer KI
Hier kommt Claude Desktop in der kostenlosen Version zur Verwendung.

### Lesen / Schreiben von Dokumenten
Dafür wird ein MCP-Server ["mcp-server-filesystem"](https://github.com/MarcusJellinghaus/mcp_server_filesystem.git) verwendet, der nur das entsprechende Arbeitsverzeichnis unter [User]\Dokumente\Rezepte frei gibt und nicht das ganze Filesystem.

### Texterkennung
Das Eingangs-PDF enthält ein Bild des Rezeptes, das mit Hilfe von "tesseract" in Text umgewandelt wird. Den Zugriff für die KI erlaubt wiederum ein MCP-Server ["mcp-server-tesseract"](https://github.com/lka/mcp_server_tesseract.git).



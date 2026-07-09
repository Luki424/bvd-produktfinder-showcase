# BVD Produktfinder – Showcase

Interaktiver Produktfinder über das Sortiment der [BVD GmbH, Sinsheim](https://www.bvd-batterien.de)
(„The Battery Company"): 60 Produktlinien mit 430 Varianten – Starter-, Motorrad-,
Versorgungs-, Backup- und Industriebatterien, Portable Power und Zubehör von
FLYBAT, VARTA, BOSCH, OPTIMA, HOPPECKE, motoVolt, MAWEK, S.P.E. und Victron Energy.

**Inoffizieller Demo-Showcase.** Produktdaten (Typenprogramme, Maße, Gewichte,
Kaltstartströme, Artikelnummern), Bilder und Datenblatt-Links stammen von den
öffentlichen Produktseiten auf bvd-batterien.de (Stand Juli 2026). Keine Preise –
Anfragen direkt an die BVD GmbH.

Single-File-App (React + Vite, alles in einer `index.html`), gebaut mit Claude Code.
Als PWA installierbar und offline nutzbar (Service Worker); die Suche versteht auch
Vergleichstypen wie `LN3`, `BCI 48` oder `YTX14-BS` – inklusive Kurzschreibweisen
(`bci48`, `YTX14BS`) – sowie EAN- und ETN-Typnummern. Je Variante zeigt eine Verfügbarkeits-Ampel
(auf Lager / knapp / auf Anfrage) den BVD-Lagerbestand (Stichtag im Tooltip) –
ohne interne Stückzahlen; dazu Katalog-Filter „Sofort ab Lager" und
Verfügbarkeits-Hinweise in Produktkarten und Anfrageliste; Sortierung „Sofort ab Lager zuerst" und ein Verfügbarkeits-Zähler im Katalog. Ein Sortiment-Dashboard
zeigt Kategorien, Technologien, Kapazitätsklassen und Lagerabdeckung als klickbare
Charts; der Ersatzbatterie-Finder visualisiert das Einbaumaß maßstabsgetreu.
Eine Vergleichs-Ansicht stellt mehrere Produktlinien nebeneinander (Verfügbarkeit,
Technologie, Spannung, Kapazität, Kaltstart, Maße L×B×H, Gewicht, Varianten) –
mit Unterschieds-Hervorhebung, Filter „Nur Unterschiede", teilbarem Link und
direkter Übernahme in die Anfrageliste.
Ein Ladegeräte-Berater empfiehlt Ladestrom und passende Ladegeräte zur Batterie;
ein Upgrade-Berater zeigt zulässige Wechsel (SLI → EFB → AGM); ein
Batteriebank-Rechner legt Reihen-/Parallelschaltungen für 12/24/48-V-Systeme aus;
ein Bordnetz-Assistent für Marine & Caravan empfiehlt anhand von Fahrzeugtyp, Nutzung,
Landstrom und Solar die passende Versorgungstechnologie (Blei/LiFePO4), Ladequellen
(Landstrom-Ladegerät, Ladebooster, Solar/MPPT) und Kernprinzipien – inklusive
Verbraucher-Baukasten, der typische Bordverbraucher (Kühlbox, Licht, Wasserpumpe …)
auswählbar macht und direkt in den Energiebedarf-Rechner übernimmt; dessen Ergebnis
wiederum belegt den Batteriebank-Rechner mit der Ziel-Kapazität (Blei/LiFePO4) vor;
ein Technik-Glossar erklärt die Fachbegriffe; ein Info-Bereich erläutert Altbatterie-Rücknahme,
Pfand (Batteriegesetz) und Batterie-Pflege/Lagerung. ETN-Typnummer und Pollage (Pluspol rechts/links) je
Variante stammen aus der offiziellen BVD-Preisliste (ohne Preise).
Fürs Tagesgeschäft: Barcode-Scanner in der Suche (nativer BarcodeDetector,
plus eigener EAN-13-Decoder als Fallback – funktioniert damit auch auf iPhone
und Desktop), QR-Code beim Teilen, druckfertige Anfrageliste sowie Direktkontakt
(Anrufen per tel:-Link und vorbereitete E-Mail) aus der Anfrageliste. QR-Codes via
[qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) (MIT).
Die Oberfläche ist zweisprachig (DE/EN) und bietet einen Hell-/Dunkelmodus
(Umschalter im Header, folgt sonst der Systemeinstellung); Produktdaten bleiben
in Originalsprache.

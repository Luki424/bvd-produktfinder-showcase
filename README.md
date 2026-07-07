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
(`bci48`, `YTX14BS`) – sowie EAN-Codes vom Barcode. Je Variante zeigt eine Verfügbarkeits-Ampel
(auf Lager / knapp / auf Anfrage) den BVD-Lagerbestand (Stichtag im Tooltip) –
ohne interne Stückzahlen; dazu Katalog-Filter „Sofort ab Lager" und
Verfügbarkeits-Hinweise in Produktkarten und Anfrageliste. Ein Sortiment-Dashboard
zeigt Kategorien, Technologien, Kapazitätsklassen und Lagerabdeckung als klickbare
Charts; der Ersatzbatterie-Finder visualisiert das Einbaumaß maßstabsgetreu.

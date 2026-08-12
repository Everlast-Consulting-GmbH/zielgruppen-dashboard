# Zielgruppen-Dashboard — ARCHIVIERTER STAND

> [!WARNING]
> **Dieser Repository-Stand ist veraltet und wird nicht mehr gepflegt.**
>
> Die aktuelle Variante liegt im **Resource Hub der Everlast-App**:
> <https://app.everlastintern.de/resource-hub> (Eintrag „Zielgruppen-Dashboard").
> Zugriff über Cloudflare Access mit `@everlastconsulting.de` /
> `@kiberatung.de` und der Berechtigung `resource-hub.read`.
>
> **Änderungen an der HTML bitte dort** über „Datei ersetzen" einspielen — das
> hält die Resource-ID und damit bestehende Permalinks stabil. Änderungen in
> diesem Repo landen nirgends.

## Was hier noch liegt

| Datei | Zweck |
|---|---|
| `index.html` | Der archivierte Dashboard-Stand (self-contained, keine Build-Schritte) |
| `Keywords-Branchen.csv` | Quelldatei der Keyword-Zuordnung. Wird zur Laufzeit **nicht** geladen |

## Die Daten liegen nicht in diesem Repo

Das Dashboard zieht seine Inhalte per JSONP live aus Google Sheets — die
HTML ist nur die Hülle. **Inhaltliche Pflege passiert im Sheet, nicht hier
und nicht im Resource Hub.**

- Sheet: `1a9_4DEy9K8vaehLUujwHDnvFDCM5d1Dakm9c40bTKPg`
- Tab `275775392` — Zielgruppen-Daten (NACE-Code, Bewertung, Use-Cases)
- Tab `1767725536` — Keywords je NACE-Code

Lädt das Sheet nicht, rendert die Seite still aus dem eingebauten
`FALLBACK_DATA` weiter — die Anzeige sieht dann korrekt aus, zeigt aber alte
Zahlen. Ein Ausfall ist nur in der Browser-Konsole sichtbar.

## Altlast: die öffentliche Vercel-Instanz

<https://zielgruppen-dashboard.aiagentur.de/> läuft weiterhin, ist **ohne
Login erreichbar** und zeigt dieselben Live-Daten — obwohl sich das Dokument
im Footer selbst als „Vertrauliche Ressource" bezeichnet. Der zugehörige
Vercel-Account war Stand 08/2026 nicht auffindbar, deshalb konnte die
Instanz nicht abgeschaltet werden. Bis das passiert, ersetzt der Resource-Hub-
Eintrag sie nicht, sondern steht daneben.

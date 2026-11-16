# Draf

Hardloopschema als web-app (PWA) met Strava-koppeling. Alles staat lokaal op het toestel: geen account, geen server.

- **Vandaag**: weekoverzicht, de training van vandaag als blokjes (breedte = tijd, hoogte = zwaarte), voortgang van de week en de volgende training.
- **Schema**: alle weken, met per training de stappen, zones, uitleg en aandachtspunten.
- **Activiteiten**: loopjes en ritten uit Strava, vergeleken met wat er gepland stond.
- **Profiel**: schema importeren, Strava koppelen, back-up.

## Schema

Een schema is een JSON-bestand in hetzelfde formaat als Tempo in Kern (`kern: "tempo-plan"`): weken met een startdatum (maandag) en per dag een lijst trainingen met stappen (`l`, `t`, `z` voor loopzone, `bz` voor fietszone, `tgt` voor een doel). Er zit een voorbeeldschema in de app.

## Strava

Gebruikt een eigen Strava API-app. Client ID en secret vul je zelf in op het toestel; ze staan nergens in de code. Een nieuwe Strava-app laat standaard één sporter toe; in de API-instellingen van Strava kun je dat verhogen naar tien. De callback-domeinnaam moet het domein zijn waar deze pagina staat.

## Lokaal draaien

```sh
python3 -m http.server 8000
```

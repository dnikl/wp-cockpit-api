# wp-cockpit-api

## Authentifizierung

Authentifizieren Sie sich mittels Basic Auth.
Der Username und das Passwort werden von der Netlive AG zur Verfügung gestellt.

```
**PUT** http://127.0.0.1:8500/Demandit20180307/System204F/AjaxProxy/sso/interface.cfm
```

## JSON Fields

| Key  | Value | Required | Description |
| ------------- | ------------- | ------------- |
| email  | "max@muster.ch" | yes | |



{
    "email": "max@muster.ch",
    "ext_geb_id": "id_634",
    "kwh_el": 2000,
    "kwh_wrm": 3000,
    "stand_datum": "2012-04-23T18:25:43.511Z",
    "anrede_id": 1,
    "vorname": "Max",
    "name": "Muster",
    "bezeichnung": "geb api",
    "strasse": "api strasse",
    "plz": 9204,
    "ort": "api ort",
    "meter_ueber_meer": 800,
    "egid_nr": 554324,
    "baujahr": 1950,
    "energiebezugsflaeche": 160,
    "waermepumpentyp_id": 2,
    "brauchwarmwasserproduktion": 1,
    "heizungstyp_id": 2,
    "einschaltungen": 4,
    "betriebsdauer": 120,
    "installateur": "Max Müller"
}
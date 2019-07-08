# wp-cockpit-api

## Authentifizierung

Authentifizieren Sie sich mittels Basic Auth.
Der Username und das Passwort werden von der Netlive AG zur Verfügung gestellt.

```
**PUT** http://127.0.0.1:8500/Demandit20180307/System204F/AjaxProxy/sso/interface.cfm
```

## JSON Fields

| Key  | Value | Required | Description
| ------------- | ------------- | ------------- |
| email  | "max@muster.ch" | yes
| ext_geb_id  | "12BCD" | yes |
| kwh_el  | 2000 | yes |
| kwh_wrm  | 3000 | yes |
| stand_datum  | "2012-04-23T18:25:43.511Z" | yes |
| anrede_id | 1 = "Frau"  OR 3 = "Herr" | when email not found  |
| vorname | "Max" | when email is not found  |
| name | "Muster" | when email is not found  |
| bezeichnung | "MFH Max Muster" | when ext_geb_id not found  |
| strasse | "Hauptstrasse 17" | when ext_geb_id not found  |
| plz | 9200 | when ext_geb_id not found |
| ort | "Gossau" | when ext_geb_id not found |
| meter_ueber_meer | 800 | when ext_geb_id not found |
| egid_nr | 554324 | |
| baujahr | 1990 | |
| energiebezugsflaeche | 1990 | |
| waermepumpentyp_id | | |
| brauchwarmwasserproduktion | | |
| heizungstyp_id | | |
| einschaltungen | | |
| betriebsdauer | | |
| installateur | | |


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
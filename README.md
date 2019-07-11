# wp-cockpit-api

## Authentifizierung

Authentifizieren Sie sich mittels Basic Auth.
Der Username und das Passwort werden von der Netlive AG zur Verfügung gestellt.
Die Werte müssen als JSON gesendet werden.

## Request Headers

Make sure you set the following request header.
```
Content-Type: application/json; charset=utf-8
```


```
PUT https://mypage.netlive.ch/System204F/AjaxProxy/sso/interface.cfm
```

## JSON Fields

| Key | Example value | Required | Description |
|:-----------|:-----------|:-----------|:-----------|  
| email  | "max@muster.ch" | yes | |
| ext_geb_id  | "12BCD" | yes | |
| kwh_el  | 2000 | yes | |
| kwh_wrm  | 3000 | yes | |
| stand_datum  | "2012-04-23T18:25:43.511Z" | yes | |
| anrede_id | 1 | when email not found  | Siehe Tabelle |
| vorname | "Max" | when email is not found  | |
| name | "Muster" | when email is not found  | |
| bezeichnung | "MFH Max Muster" | when ext_geb_id not found  | |
| strasse | "Hauptstrasse 17" | when ext_geb_id not found  | |
| plz | 9200 | when ext_geb_id not found | |
| ort | "Gossau" | when ext_geb_id not found | |
| meter_ueber_meer | 800 | when ext_geb_id not found | |
| egid_nr | 554324 | | |
| baujahr | 1990 | | |
| energiebezugsflaeche | 160 | | |
| waermepumpentyp_id | 1 | | Siehe Tabelle| |
| brauchwarmwasserproduktion | 1 | | Siehe Tabelle |
| heizungstyp_id | 2 | | Siehe Tabelle |
| einschaltungen | 4 | |
| betriebsdauer | 100 | |
| installateur | "Peter Müller" | |


## Example JSON
```
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
    "betriebsdauer": 100,
    "installateur": "Peter Müller"
}
```

## Tables

### Anrede
| ID | Value | 
|:-----------|:-----------|
1 | Frau
2 | Herr

### Wärmepumpentyp
| ID | Value | 
|:-----------|:-----------|
2 | Luft/ Wasser-Wärmepumpe
3 | Sole/ Wasser-Wärmepumpe
4 | Split-Luft/Wasser-Wärmepumpe
7 | Inverter-Luft/Wasser-Wärmepumpe
8 | Inverter-Sole/Wasser-Wärmepumpe

### Brauchwarmwasserproduktion
| ID | Value | 
|:-----------|:-----------|
1 | Ja
2 | Nein

### Heizungstyp
| ID | Value | 
|:-----------|:-----------|
2 | Bodenheizung (35°C / 30°C)
3 | Radiatorenheizung (45°C / 40°C)
4 | Bodenheizungen und Heizkörper kombiniert

## Responses

### Success
```
{
    "SUCCESS":"updated",
    "MESSWERT_ID":365
} 
```

### Missing Field
```
{
    "ERROR": "Missing field ext_geb_id in request body"
} 
```
# Datenbanken

-> **Organisierte Sammlung an Daten**, welche ein Management dieser (lesen, schreiben) ermöglicht.

Ein Mailclient könnte Daten eines Kontaktbuchs über dreierlei Wege erreichen:

* **Programmierinterface** -> Kontakt stellt Endpoint bereit, über welche der Server besagte Daten erhält.
* **File exchange** -> Kontaktbuch schreibt Daten in ein File, welches der Server dann ließt.
* **Datenbanken** -> Kontakten speichern Daten organisiert mittels eines DB-Tools, Mailserver ließt diese dann wieder.


Neben den [[_Relationale Datenbanken|Relationalen Datenbanken]] existieren auch noch die [[Nicht-Relationalen Datenbanken]].


## Ansprüche

- Daten müssen **schnell** erreichbar sein
- Verwante Daten müssen verlinked werden können
- Daten müssen änderbar sein
- Mehrere Nutzer:innen müssen Daten **gleichzeitig** verwenden können
- Daten müssen **konsistent** sein und
- dürfen nicht verloren gehen
- Nur jene mit Berechtigung sollen Zugang erhalten.

Nach dem [[CAP-Theorem]] sind **nicht alle** dieser Ansprüche zeitgleich implementierbar!
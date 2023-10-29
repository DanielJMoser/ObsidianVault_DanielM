# Aufbau
#embeddedsystems

***Zwei grobe Unterteilungen:***

## Plattformsoftware

* Hardware-Abstraktionsschicht
* Beinhaltet **Schnittstellen** und **Treibersoftware**
* Kapselung von low-level Aufgaben und Bereitstellung entsprechender Services


## Applikationssoftware

* Aufbauend auf [[Aufbau ES#Plattformsoftware|Plattformsoftware]]
* Möglichst Hardware-unabhängig
* Implementiert **eigentliche Funktionalität**

-------------------------------------------------------

-> Oftmals bestehend aus **mehreren Teilsystemen!**

Diese werden **Steuergeräte** oder **Electronic Control Unit** (ECU) genannt und sind durch ein **Kommunikationsnetzwerk** (i.d.R. [[Bus-Systeme]]) verbunden.

Zwischen den, oftmals von **unterschiedlichen Entwicklerteams** ins Leben gerufenen, Teilsystemen existieren **eindeutig definierte Schnittstellen** nach dem *Teile-und-Herrsche*-Prinzip.

--------------------------------------------------


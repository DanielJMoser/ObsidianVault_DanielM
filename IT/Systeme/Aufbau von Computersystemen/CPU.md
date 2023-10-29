# CPU
## Aufbau
### Steuerwerk
-> Ablauf der **Befehlsverarbeitung**!
-> **Senden u. Empfangen** von Steuersignalen zwischen allen Funktionseinheiten.
-> [[CPU#Programmzähler|Programmzähler]], [[CPU#Befehlsregister|Befehlsregister]], Befehlsdecoder, Steuerleitungen


#### Programmzähler
-> enthält Speicheraddresse des nächsten auszuführenden Befehls.

#### Befehlsregister
-> Hier wird obiger Befehl hingeschrieben. **Register**: Speicherstellen, die besonders schnellen Zugriff ermöglichen.

#### Befehlsdecoder
-> Befehle sind **Bitfolgen**, welche den auszuführenden Befehl und ihre Operanden (d.i. die Speicheraddresse im [[CPU#Befehlsregister|Befehlsregister]]) kodieren.

------------------------

## ISA Architekturen

### Register Memory Architektur

- Operanden von Befehlen können sowohl im *Hauptspeicher* als auch in *Registern* sein.


### Load-Store Architektur

- Operanden nur im *Register*
- Müssen erst in den *Hauptspeicher* geladen werden
- Werden danach wieder zurückgeschrieben.


### Stack Architektur

- Operanden können nur in als **Stacks** organisierten Registern sein.

------------------

## Befehlsausführung

### Fetch
- Ladet Befehl aus Speicher

### Decode
- Steuerleitungen werden gesetzt
- Andere Komponenten wissen was zu tun ist.

### Load
- Operanden werden geladen.

### Execute
- Befehle werden ausgeführt.

### Store
- Ergebnis wird zurückgespeichert.


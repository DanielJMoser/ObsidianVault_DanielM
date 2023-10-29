
-> [[Prozessbasierte Systeme]]

In dem Kontext von **Betriebssystemen**, sind Prozesse eine **Abstraktion**, die verwendet wird, um die **Ausführung von Anwendungen und Programmen** zu verwalten. 
Ein Prozess ist die _Grundeinheit_ der **Ressourcenverwaltung** und der **Verarbeitung**, die von einem Betriebssystem verwaltet wird.

___

## Bestandteile eines Prozesses

Jeder Prozess hat seinen **eigenen Satz von Ressourcen**, einschließlich _Arbeitsspeicher, Register und Dateihandles_. 
Jeder Prozess hat auch seinen eigenen _Prozesszustand_ und seine eigene _Ausführungssteuerung_.

Ein Prozess kann aus **einem oder mehreren [[Threads]]** bestehen, die **parallel** ausgeführt werden können, um die Leistung zu verbessern. Jeder Thread hat seinen eigenen Satz von Registerwerten und Arbeitsspeicher-Adressen, aber teilt sich die gleiche Prozessumgebung.

___

## Verwaltung von und mit Prozessen

Prozesse werden von einem **Betriebssystem verwaltet** und können von **anderen Prozessen gestartet, gestoppt, angehalten und fortgesetzt** werden. Sie können auch Ressourcen wie Arbeitsspeicher, CPU-Zeit und Dateien teilen und verwalten.

Prozesse sind die **Grundeinheit für die Ressourcenverwaltung und die Verarbeitung**, die von einem Betriebssystem verwaltet wird. Sie ermöglichen es Anwendungen und Programmen, **unabhängig voneinander** ausgeführt zu werden und sicherzustellen, dass jeder Prozess die ihm zugewiesenen Ressourcen **nicht überschreitet** und dadurch andere Prozesse beeinträchtigt.

___

## Prozesse und Sicherheit

Prozesse können auch als **Sicherheitsmechanismus** verwendet werden, da sie es ermöglichen, dass ein fehlerhafter Prozess **abgeschlossen** wird, ohne dass dies Auswirkungen auf andere Prozesse hat.

___

## Zusammenfassung

Prozesse sind auch die **Grundlage für die Multitasking-Fähigkeit eines Betriebssystems**, da sie es ermöglichen, dass mehrere Anwendungen gleichzeitig ausgeführt werden, ohne dass eine Anwendung die andere beeinträchtigt.

Zusammenfassend,

**_Prozesse sind eine Abstraktion, die verwendet wird, um die Ausführung von Anwendungen und Programmen zu verwalten und Ressourcen sicher und effizient zu teilen._** 

Sie ermöglichen es, dass **mehrere Anwendungen gleichzeitig** ausgeführt werden und erhöhen die **Sicherheit** und **Stabilität** des Systems.
Ein Shared-Memory-Computer (auch als **Symmetric Multiprocessing-System oder SMP-System** bezeichnet) ist ein Computersystem, das m**ehrere Prozessoren oder Prozessorkerne auf einer gemeinsamen physikalischen Speicherarchitektur** nutzt. 

Im Gegensatz zu [[Distributed-Memory-Systemen]], teilen sich alle Prozessoren in einem Shared-Memory-Computer denselben Speicher.

In einem Shared-Memory-Computer kann **jeder Prozessor auf jeden Speicherbereich** zugreifen, was die Programmierung von Anwendungen erleichtert. 
Dies ermöglicht eine **effektive Zusammenarbeit** zwischen den Prozessoren, da sie einfach Daten miteinander teilen können, ohne sie über das Netzwerk übertragen zu müssen. Dadurch wird die **Latenz reduziert** und die Geschwindigkeit der Datenverarbeitung erhöht.

Ein Shared-Memory-Computer wird typischerweise in Anwendungen eingesetzt, die eine **hohe Leistung** erfordern, wie z.B. 

- wissenschaftliche Simulationen, 
- Datenbankanwendungen, 
- parallele Verarbeitung von Grafiken oder Multimedia-Anwendungen. 

In der Regel bieten Shared-Memory-Computer auch eine höhere Skalierbarkeit als Einzelprozessor-Systeme, da sie mehrere Prozessoren oder Prozessorkerne aufnehmen können und somit eine höhere Verarbeitungsleistung bieten.

Allerdings haben Shared-Memory-Computer auch einige Nachteile. Ein Problem ist, dass sie anfällig für Engpässe bei der Speicherbandbreite sind, wenn zu viele Prozessoren gleichzeitig auf denselben Speicherbereich zugreifen. Dies kann zu Verzögerungen in der Datenverarbeitung und einer reduzierten Leistung führen. Ein weiteres Problem besteht darin, dass die Kosten für Shared-Memory-Systeme höher sind als für Einzelprozessor-Systeme, da sie spezielle Hardwarekomponenten wie spezielle Speicherkontroller und Interconnects benötigen, um den gemeinsamen Speicher zu verwalten.
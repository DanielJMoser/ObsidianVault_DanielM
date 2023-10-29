
-> Kommen ohne Speicherabstraktion aus.

Bei solchen Systemen kann ein einziges Programm den **gesamten Speicher** für sich allein beanspruchen. Code kann so platziert werden, dass die **Sprungadressen** stimmen und **Globale Variablen** dort, wo das Programm sie erwartet.

Etwa [[_Mikrocontroller]] fallen in diese Kategorie. Obwohl diese **nicht über ein Betriebssystem verfügen**, ist Single Tasking möglich. Speicherabstraktion würde wenig Nutzen, aber **viele Kosten** verursachen.

Verfügt ein Single-Tasking System über ein Betriebssystem, so muss sowohl **Kernel** als auch **Verwaltungsstrukturen** im Speicher gehalten werden. Ein Programm hat damit Zugriff auf den **gesamten** Speicher (also auch auf den Speicher des Betriebssystems), welcher damit auch leicht durch **Malware** veränderbar wird. Zum Schutz verwendet man Mechanismen wie [[Segmentierung]].

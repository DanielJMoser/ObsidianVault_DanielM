-> die Ausführung von [[_SQL|SQL]]-Abfragen in **Java-Anwendungen**. 

JDBC stellt **verschiedene Arten** von Statements bereit, um SQL-Abfragen an eine Datenbank zu senden und Ergebnisse abzurufen. Die drei wichtigsten Arten von Statements in JDBC sind:

### 1.  Statement
Dies ist das **einfachste Statement**, das verwendet wird, um eine **beliebige** SQL-Abfrage auszuführen. Es wird normalerweise für **statische** SQL-Abfragen verwendet, die **keine Parameter** enthalten.


### 2. [[JDBC PreparedStatement|PreparedStatement]]
Dieses Statement ist ähnlich wie das einfache Statement, jedoch können hier **Platzhalter** verwendet werden, um Parameter in der SQL-Abfrage zu **ersetzen**. Es wird normalerweise für SQL-Abfragen verwendet, die Parameter enthalten, um **SQL-Injektionsangriffe** zu vermeiden und die **Performance** der Anwendung zu verbessern.

### 3.  CallableStatement
Dieses Statement wird verwendet, um **gespeicherte Prozeduren** aufzurufen und ist für Datenbanken geeignet, die gespeicherte Prozeduren unterstützen.

Nachdem ein Statement erstellt wurde, wird es an die Datenbank **gesendet** und **ausgeführt**, und das Ergebnis wird von der Datenbank zurückgegeben. 
Die Ergebnisse können dann von der Anwendung abgerufen werden, um weitere Verarbeitungen durchzuführen.


## Beispiel

```SQL
try (var con = DriverManager.getConnection(...);
	 var stm = con.createStatement()) {
	
	 // TODO
	 
}
```


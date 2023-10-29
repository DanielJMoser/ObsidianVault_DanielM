
# executeUpdate()

`executeUpdate()` ist eine Methode in [[_JDBC|JDBC]], die verwendet wird, um SQL-Anweisungen auszuführen, die Daten in der Datenbank ändern. 
Die Methode gibt die **Anzahl der betroffenen Zeilen** als Integer zurück, die durch die Ausführung der SQL-Anweisung geändert wurden.

`executeUpdate()` wird normalerweise verwendet, um SQL-Anweisungen auszuführen, die **INSERT**-, **UPDATE**- oder **DELETE**-Operationen ausführen. Diese Arten von SQL-Anweisungen ändern Daten in der Datenbank und haben **keinen Rückgabewert.**
Anstatt ein Ergebnis zurückzugeben, gibt `executeUpdate()` die **Anzahl der geänderten Zeilen** zurück, damit die Anwendung überprüfen kann, ob die Änderungen erfolgreich waren.

```SQL
var query = " DELETE FROM x;";

try (var con = DriverManager.getConnection (...);
	 var stm = con.createStatement()) {
		 con.setAutoCommit(false); /* optional ! */
		 stm.executeUpdate(query);
		 con.commit(); /* optional ! */
		 
} catch (Exception e) { 
	 con.abort(); /* optional ! */
}
```

___

# executeQuery()

`executeQuery()` ist eine Methode in [[_JDBC|JDBC]], die verwendet wird, um SQL-Abfragen auszuführen, die **Daten aus der Datenbank zurückgeben**. Die Methode gibt ein **ResultSet-Objekt** zurück, das die Ergebnisse der SQL-Abfrage enthält.

`executeQuery()` wird normalerweise verwendet, um **SELECT-Abfragen** auszuführen, die Daten aus der Datenbank zurückgeben. Diese Art von SQL-Abfragen geben keine Anzahl von geänderten Zeilen zurück, sondern eine **Ergebnismenge** mit Datensätzen, die aus der Datenbank abgerufen wurden.

```SQL
var query = " SELECT * FROM X;";
try (var con = DriverManager.getConnection (...);
	 var s = con.createStatement();
	 var r = s.executeQuery(query)) { 
	 while (r.next()) {
	 var x = r.getInt(1); // index based
	 var y = r.getString ("y") ; // name based
	  ...
	}
}
```



-> ermöglicht es, [[_SQL|SQL]]-Anweisungen mit **Parametern** auszuführen. 
Im Gegensatz zu einem normalen Statement werden bei einem PreparedStatement die Parameter als **Platzhalter** in der SQL-Anweisung verwendet und können dann bei Bedarf durch **konkrete Werte** ersetzt werden.

## Vorteile

1.  Bessere Leistung: Da PreparedStatements vorab kompiliert werden, können sie schneller ausgeführt werden als normale Statements.
    
2.  Sicherheit: PreparedStatements verhindern SQL-Injektionsangriffe, da sie Parameterwerte automatisch escapen.
    
3.  Flexibilität: PreparedStatements sind flexibler als normale Statements, da sie zur Laufzeit verschiedene Parameterwerte akzeptieren können.

```SQL
var query = " DELETE FROM x WHERE id = ?
			and y like ?;";

try (var con = DriverManager.getConnection(...);
	var stm = con.prepareStatement ( query )) { 
	stm.setInt(1,42);
	stm.setString(2,"% test");
	stm.executeUpdate();
	con.commit();
}
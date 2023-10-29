
Um **neue Informationen** zu unserer Datenbank hinzuzufügen, können wir in SQL folgende Operatoren verwenden:

- Insert
- Update
- Delete

Wird einer der Operatoren verwendet, sucht das System nach **widersprüchlichkeiten**. Werden diese gefunden -> Abbruch


## Update

```sql
UPDATE Professor
SET Salary = Salary * 1.1
WHERE Salary < 1000;
```

**SET** erlaubt uns, ein oder mehrere Attribute gegen einen neuen Ausdruck auszutauschen (hier: e[] gegen a)

**WHERE** muss nicht zwingend verwendet werden. Falls nicht: Jedes Tupel im System wird upgedated.


## Delete

```sql
DELETE
FROM Professor
WHERE Salary < 1000;
```

-> Löscht **jedes Tupel**, falls WHERE-Condition nicht bereitgestellt!

Könnte zu Problemen in der Abhängigkeit führen.


## Insert

```sql
INSERT
INTO Professors
VALUES (2142, 'Aristoteles', 'Philosophy', 3600)
```

Kann mit oder ohne Liste an attributen verwendet werden. Wir können auch **mehrere** Professoren gleichzeitig einfügen, in dem wir sie "bulken".


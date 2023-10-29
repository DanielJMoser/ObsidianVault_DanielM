-> Konzept in der Softwareentwicklung, das sich auf ein Design-Muster bezieht, bei dem die [[Entity|Entities]] im Domain Model zwar über Eigenschaften verfügen, aber nur **sehr wenig** oder **gar keine Geschäftslogik** in sich tragen. 
Die Geschäftslogik wird stattdessen in **separaten** Dienst- oder Serviceklassen implementiert.

Im Gegensatz zum [[Rich Domain Model]], bei dem die Geschäftslogik direkt in den Entitäten des Domain Models implementiert wird, ist das **Anemic Domain Model** insofern "**anämisch**", als es die Entitäten als **einfache Datenstrukturen** behandelt, ohne dass sie in der Lage sind, komplexe Aufgaben auszuführen. 

## Beispiel

```SQL
public class Person {
	private int id;
	private String firstName;
	private String lastName;
	public Person() {}
	public Person (int id , String fn , String ln ) {
		setId(id);
		setFirstName(fn); 
		setLastName(ln);
	}
	
	public int getId () {
		return id;
	}
	public void setId (int id ) {
		this.id = id;
	}
	public String getFirstName () {
		return firstName;
	}
	...
}
```

## Nachteile

Der Nachteil des Anemic Domain Models ist, dass es zu einer übermäßigen Abhängigkeit von Serviceklassen führen kann, was zu einem höheren Codevolumen, geringerer Kohäsion und schlechter Lesbarkeit führt. Es kann auch zu Verwirrung führen, da die Geschäftslogik nicht direkt in den Entitäten enthalten ist und stattdessen in verschiedenen Teilen des Codes verteilt ist.

Insgesamt wird das Anemic Domain Model von vielen Experten kritisiert, da es zu einer **schlechteren Lesbarkeit, Wartbarkeit und Erweiterbarkeit** des Codes führen kann. 
Das [[Rich Domain Model]] ist oft die bevorzugte Design-Strategie, da es dazu beiträgt, dass die Geschäftslogik auf eine **strukturierte und leicht verständliche** Weise implementiert wird.
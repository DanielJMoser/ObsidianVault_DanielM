# Daten-Container

-> Abstrakte Objekte, die andere Objekte speichern (vgl. z.B. Arrays)

Theoretisch ein **"Unendlicher Speicher"** von Objekten. (praktisch: limitiert durch Arbeitsspeicher)


Jedes Mal solche Container eigens zu implementieren, ist äußerst aufwendig. Daher: **Vorgefertigte Container in Standard-Bibliothek**.

Da C++ eine **statisch typisierte** Programmiersprache ist, müsste diese für jeden möglichen Datentypen einen eigenen Container beinhalten, was in der Praxis eine Unmöglichkeit darstellt, weshalb die dortigen Daten-Container in Form von [[Class Templates]] vorliegen.
Solche generischen Container werden auch **Collections** genannt.

Diese Container teilen sich in **_zwei Obergruppen_** auf:
- [[Sequentielle Container]]
- [[Assoziative Container]]





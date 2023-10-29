# Kritische Regionen
#prozesssynchronisation 
#synchronisationsprimitiven 

-> Auch: Critical Regions, Critical Sections, kritische Abschnitte!
Dabei handelt es sich um **Code-Abschnitte, die nur von einem Prozess bzw. Thread gleichzeitig betreten werden dürfen**.

Sie bestehen meist aus **mehreren Einzelanweiseungen**, deren Zwischenergebnisse **inkonsistente Zustände** darstellen.

Auf diese sollen andrer Prozesse bzw. [[Threads|Threads]] natürlich keinen Zugriff erlangen! Konsistenz kann nur sichergestellt werden, wenn **alle** Einzelanweisungen in **einem Stück** abgearbeitet werden können.

Dieses Konzept wird auch ***Mutual Exclution*** genannt.

___

## Anschauungsbeispiel

```c
#include <pthread.h>
#include <stdio.h>

/**
 * Variable, welche den Mutex reprÃ¤sentiert.
 *
 * Von dieser Variable sollte nie eine Kopie angefertigt werden!
 */
pthread_mutex_t mutex;


void* thread_func(void* arg) {
	int* mydata = (int*)arg;
	// Wir addieren zur Ã¼bergebenen Zahl 10000-mal die 1
	for (int i = 0; i < 10000; i++) {
		// Sperre den Mutex
		pthread_mutex_lock(&mutex);

		// Begin der kritischen Region
		*mydata += 1;
		// Ende der kritischen Region

		// Entsperre den Mutex
		pthread_mutex_unlock(&mutex);
	}
	return NULL;
}

int main() {
	// Reserviere Speicher fÃ¼r die Thread-Handles
	pthread_t myThreads[10];
	// Reserviere Speicher fÃ¼r die benutzerdefinierten Daten
	// Zu dieser Zahl werden 10 Threads 10000-mal die 1 dazuaddieren
	int mydata = 0;

	// Initialisiere den Mutex
	// 1. Argument: Zeiger auf die Mutex Variable
	// 2. Argument: Zeiger auf die Attribut-Variable (NULL bedeutet Default Attribute)
	pthread_mutex_init(&mutex, NULL);

	// Erzeuge 10 Threads
	for (int i = 0; i < 10; i++) {
		printf("Erzeuge Thread %d\n", i);
		// Erzeuge den Thread
		pthread_create(&myThreads[i], NULL, &thread_func, &mydata);
	}

	// Warte auf die Beendigung aller Threads
	for (int i = 0; i < 10; i++) {
		pthread_join(myThreads[i], NULL);
		printf("Thread %d wurde beendet\n", i);
	}

	// Gebe das Endergebnis aus
	printf("mydata = %d\n", mydata);

	// Gebe den Mutex wieder frei
	pthread_mutex_destroy(&mutex);

	return 0;
}```

Die Idee wäre hier, 10 000x eine 1 zu addieren. Tatsächlich sind die Ergebnisse beim Ausführen aber ziemlich **zufällig** -> fair bit of [[Race Conditions]]

____

## ***Aber warum?***

Die kritische Region besteht im Code nur aus einer Zeile (nämlich *"*mydata += 1;*"), tatsächlich aber aus drei Schritten:

1. Variable *s* wird vom Hauptspeicher ins Register *a* geladen. -> a = s
2. Dort wird die Eins addiert
3. Der neue Wert wird in den Hauptspeicher zurückgespeichert. (vgl. [[CPU#Load-Store Architektur|Load-Store Architektur bei CPUs]])


Paralell dazu wird 
1. die Variable *s* ins Register *b* geladen. -> b = s
2. Dort wird die Eins addiert
3. Der neue Wert wird in den Hauptspeicher zurückgespeichert.


### Korrekte Routine
Richtiger Weise sollte dies **nacheinander** passieren, *s* also erst ins Register *b* geladen werden, nachdem die Variable aus dem Register *a* wieder in den Hauptspeicher rückgespeichert wurde.
Gilt ursprünglich **s = 0**, so gilt nun **s = 2**.


### Inkorrekte Routine
Der erste Thread wird **nach Schritt 2** unterbrochen, Thread Zwei ladet *s* aus dem Hauptspeicher und fährt normal fort. Erst zum Schluss werden beide Werte zurückgespeichert.
Gilt ursprünglich **s = 0**, so gilt nun fälschlicher Weise **s = 1**.


### Grafik

![[Drawing_CritRegion.png]]
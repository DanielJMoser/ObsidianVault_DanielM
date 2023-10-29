# Relational Model

-> Bestehend aus:

[[Relationship|Relation]]
[[Attribute]]
[[Tuple_DB|Tuple]]


## Regeln

* Jedes [[Tuple_DB|Tuple]] ist **eindeutig** und beschreibt eine [[Entity]].
* Die Reihenfolge von Zeilen und Spalten hat keine semantische Aussagekraft
* Jede Zelle (-> **Wert des Attributs**) beinhaltet einen **Atomaren Wert**. Dieser kann auch NULL sein, falls nicht existent oder unbekannt
* Jede [[Relationship|Relation]] hat einen **Primärkey**


## Primärkey

-> Identifiziert Tuple eindeutig. siehe: [[Primärschlüssel]]

Mehrere Attribute können zu einem Primärkey **zusammengefasst** werden. Sein Wert darf nicht NULL sein -> **Entity Integrity**. 

Notation: **durchgehend unterstrichen**


## Foreign Keys

-> Identifiziert ein Tupel einer **anderen Tabelle**. Kann ein Primärkey in dieser anderen Tabelle sein! Siehe: [[Fremdschlüssel]]

Ein Foreign Key beschreibt ein **Verhältnis** zur referenzierten Entität.

Notation: **gestrichelt unterstrichen** oder **doppelt unterstrichen**, falls auch Teil des Primärkeys.




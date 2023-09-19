# Latex-Arbeitsblaetter
Hallo, zu Beginn meines Referendariats habe ich mir gedacht, dass es doch schön wäre einheitliche Arbeitsblätter zu haben. Was eignet sich dazu besser als Latex? Da ich jedoch keine besonderen spezialpakete manuell installieren wollte, um auch möglichst unabhängig zu bleiben, habe ich angefangen mir eine eigene Vorlage zu basteln. Die Vorlage besteht im groben aus 3 Teilen: Commands.tex, Erwartungsbild.tex und Vorlage_AB.tex.

## Vorlage_AB.tex
Diese Datei ist das Herzstück des Arbeitsblattes. Hier werden die Aufgaben reingeschrieben und auch die Variablen (unter anderem für die Kopfzeile) definiert.

### Variablen
Ein Großteil der Variable sollte eindeutig sein (Fach, Lehrer, Datum, Einheit, ...). Da einige Variablen jedoch das Verhalten des Dokumentes verändern soll auf diese noch einmal gesondert eingegangen werden.
#### \Typ
Über die Angabe des Typs kann zwischen einem Arbeitsblatt, einer Leistungskontrolle und einer Klassenarbeit unterschieden werden. Das Arbeitsblatt unterscheidet sich von den beiden letztgenannten dahingehen, dass es keine Punktzahl und kein Erwartungsbild enthält. Die Leistungskontrolle und die Klassenarbeit beinhalten beide sowohl eine Punktzahl, als auch ein Erwartungsbild für die Aufgaben. Da es an unserer Schule für Leistungskontrollen und Klassenarbeiten leicht andere Notengrenzen gibt, habe ich mich dazu entschlossen zwischen diesen beiden Arten bereits als Variable zu unterscheiden. Unter dem Erwartungsbild erscheinen dann auch entsprechend des Typs die Notengrenzen.

#### \Losung
Die Variable Losung soll es perspektivisch ermöglichen bei Lückentexten ein Dokumente mit ausgefüllten Lücken zu erstellen.

## Commands.tex
Die Commands.tex beinhaltet das Layout der Kopfzeile und von mir eigene Commands, welche zum erstellen von Aufgaben genutzt werden können.

### Die Commands
#### \aufgabe{#1}{#2}{#3}
Der Befehl zum erzeugen einer Aufgabe verhält sich je nach Typ des Arbeitsblattes unterschiedlich. Für ein Gewöhnliches Arbeitsblatt nimmt dieser Befehl eine Variable entgegen, welche die Aufgabenstellung beinhaltet. Für die Typen Leistungskontrolle und Klassenarbeit werden als zweite Variable die Punktzahl für die Aufgabe, sowie das Erwartungsbild der Aufgabe als dritte Variable übergeben. Dieses erscheint dann auch auf der letzten Seiten.

#### \kariert{}{}

## Erwartungsbild.tex
Die Erwartungsbild.tex erzeugt basierend auf den Aufgaben ein einheitliches Erwartungsbild, welches als seperate Seite ausgegeben wird. Sie ermöglicht es eine transparente Bewertung vorzunehmen und beinhaltet auch die Notenspiegel, sowie die Notengrenzen.

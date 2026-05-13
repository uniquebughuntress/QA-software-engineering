# Anforderungsanalyse – Grocery Mate Applikation

## Die Webanwendung https://grocerymate.masterschool.com/ bietet folgende Basis-Funktionalitäten:

- Registrierung und Login
- Produktsuche mit Sortierfunktion (z. B. nach Preis), Kategorisierung von Produkten
- Produkte zu Favoriten hinzufügen
- Produkte in den Warenkorb legen
- Bestellabschluss: Eingabe von Rechnungs- und Versandinformationen, Auswahl der Zahlungsmethode, Preisberechnung (Gesamtsumme)

## **Neue Funktionen (Features)**

---

### **1. Bewertungssystem für Produkte**

**Ursprünglich vage formulierte Anforderung:**

Nutzer sollen Produkte mit einem 5-Sterne-System bewerten und zusätzlich schriftliches Feedback hinterlassen können.

**Fragen**:

1. Sollen Bewertungen erst nach erfolgreichem Kauf des Produkts durch den Nutzer abgegeben werden dürfen oder bereits ohne Kauf? (Testrelevanz: Berechtigungs- und Validierungslogik)
2. Darf ein Nutzer ein Produkt mehrmals bewerten (pro Nutzer und Kauf) oder ist eine Bewertung pro Nutzer und Produkt möglich? (Testrelevanz: Testen von Mehrfachbewertungen)
3. Wo sind die bereits gekauften Artikel aufgelistet?
4. Können Bewertungen nach der Abgabe bearbeitet oder gelöscht werden? (Testrelevanz: CRUD-Operationen prüfen)
5. Sollen neue Bewertungen sofort sichtbar sein oder erst nach Freigabe? (Testrelevanz: Datenkonsistenz und Admin-Workflow)
6. Gibt es eine Mindest- oder Maximallänge für den schriftlichen Feedback-Text? (Testrelevanz: Feldvalidierung und Grenzwerttests)
7. Gibt es einen Hinweis auf erlaubte Zeichenanzahl im Feedback-Feld (und somit eine clientseitige Begrenzung/ serverseitige Validierung)?

**Detaillierte Anforderung**:
- Eingeloggte Nutzer können pro Produkt genau eine Bewertung abgeben
- Das Bewertungssystem besteht aus einer 5-Sterne-Auswahl (1-5 Sterne) und einem optionalen Textfeld
- Der schriftliche Kommentar ist optional und auf 500 Zeichen begrenzt
- Bewertungen können nach der Abgabe nicht mehr bearbeitet, aber gelöscht werden
- Nutzer können nur Produkte bewerten, die sie tatsächlich gekauft haben
- Der Durchschnitt aller Bewertungen wird auf der Produktdetailseite als Sterne-Wert und dezimaler Wert (z. B. 4.2/5) angezeigt
- Neue Bewertungen sind sofort sichtbar (keine Freigabe durch Admin erforderlich)

---

### **2. Altersverifikation für alkoholische Produkte**

**Ursprünglich vage formulierte Anforderung:**

Alkoholische Produkte erfordern eine Altersverifikation. Beim Aufrufen der Kategorie soll ein Fenster erscheinen, in dem Nutzer ihr Alter angeben müssen (18+), bevor sie Zugriff erhalten.

**Fragen**:

1. Wie soll die Altersverifikation umgesetzt werden? (z. B. Eingabe des Geburtsdatums für eingeloggte Kunden)
2. In welchem Format soll das Geburtsdatum angegeben werden? (z. B. TT/MM/JJJJ, TT-MM-JJJJ etc)
3. Welche Meldung soll angezeigt werden, wenn der Benutzer unter 18 ist?
4. Sind bestimmte rechtliche Hinweise oder Datenschutzhinweise für die Altersverifikation erforderlich?
5. Kann man das angegebene Geburtsdatum ändern (z.B. wenn man sich vertippt hat)?


**Detaillierte Anforderung**:

- 

---

### **3. Änderungen bei den Versandkosten**

**Ursprünglich vage formulierte Anforderung:**

Versandkosten entfallen ab einem bestimmten Bestellwert. Darunter fallen Versandkosten an.

## Bewertungsgrundlage

- Mindestens 3 Fragen pro neuem Feature
- Fragen müssen für das Verständnis des Testings relevant sein

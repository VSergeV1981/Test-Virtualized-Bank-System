![C#](https://img.shields.io/badge/C%23-.NET-blue)
![Windows Forms](https://img.shields.io/badge/Windows-Forms-success)
![Repository Pattern](https://img.shields.io/badge/Pattern-Repository-orange)
![MVP](https://img.shields.io/badge/Architecture-MVP-informational)
![License](https://img.shields.io/badge/License-MIT-green)
# Bank Software

Eine Desktop-Anwendung zur Verwaltung von Kunden, Konten und Buchungen, entwickelt mit **C#**, **.NET** und **Windows Forms**.

---

## Projektbeschreibung

Dieses Projekt entstand im Rahmen einer Testaufgabe.

Ziel war die Entwicklung einer übersichtlichen und wartbaren Desktop-Anwendung zur Verwaltung von Bankstammdaten sowie zur Durchführung einfacher Bankbuchungen.

Der Schwerpunkt lag auf einer sauberen Code-Struktur, einer klaren Trennung der Verantwortlichkeiten sowie einer intuitiven Benutzeroberfläche – nicht auf der Umsetzung einer vollständigen Clean Architecture oder Domain Driven Design.

---

# Funktionen

Die Anwendung besteht aus fünf Modulen:

## Länder

- Anlegen neuer Länder
- Bearbeiten vorhandener Datensätze
- Soft Delete
- Validierung aller Eingaben

---

## Orte

- Verwaltung von Städten und Ortschaften
- Zuordnung zu einem Land
- Validierung der Eingabedaten

---

## Kunden und Konten

Verwaltung von:

- Kunden
- Bankkonten

Funktionen:

- Kunde anlegen, bearbeiten und löschen
- Mehrere Konten pro Kunde
- Standardkonto
- IBAN-Verwaltung
- Kontostand
- Automatische Vergabe von Kundennummern und Kontonummern

---

## Buchungen

Unterstützte Buchungsarten:

- Einzahlung
- Auszahlung
- Überweisung
- Eingang

Funktionen:

- Neue Buchungen erfassen
- Automatische Berechnung des Kontostands
- Validierung aller Eingaben
- Automatische Vergabe der Buchungsnummer

---

## Buchungsvorschau

Anzeige sämtlicher Buchungen.

Enthält ebenfalls bereits gelöschte Datensätze (Soft Delete).

---

# Benutzeroberfläche

Die Anwendung verwendet eine klassische Windows-Desktopoberfläche.

Nach dem Start erscheint das Hauptfenster mit:

- TreeView zur Navigation
- TabControl für die geöffneten Module
- DataGridView zur Anzeige der Daten
- Dialogfenster für Auswahllisten

---

# Eingabefelder

Es werden drei unterschiedliche Eingabetypen verwendet.

### Standard-Textfeld

Direkte Texteingabe.

Navigation über die Tab-Taste.

---

### Lookup-Feld

Datensätze können ausgewählt werden

- über eine Schaltfläche,
- über **F2**
- oder durch Eingabe eines bekannten Schlüssels und Bestätigung mit **Enter**.

---

### ComboBox

Auswahl eines Wertes aus einer vorbereiteten Liste.

---

# Validierung

Für nahezu alle Eingabefelder wurden eigene Validatoren implementiert.

Unter anderem:

- IBAN
- E-Mail
- Ländercode
- Postleitzahl
- Pflichtfelder
- Buchungsbetrag
- Buchungsdatum
- Buchungstyp
- Verwendungszweck

---

# Technische Umsetzung

- C#
- .NET
- Windows Forms
- MVP-orientierte Struktur
- Repository Pattern
- DataSet / DataTable
- LINQ
- Eigene Validierungsbibliothek
- Enum-Extensions mit DescriptionAttribute
- Soft Delete
- In-Memory-Datenhaltung
- SHA-256 Hash für Kontostände

---

# Projektstruktur

```
Presenters/
Views/
Repositories/
Models/
Services/
Validation/
Extensions/
Enums/
Storage/
```

---

# Architektur

Die Anwendung orientiert sich an einer MVP-ähnlichen Struktur.

- Presenter übernehmen die Anwendungslogik.
- Views enthalten ausschließlich die Benutzeroberfläche.
- Repositories kapseln den Datenzugriff.
- Services enthalten fachliche Berechnungen.
- Validatoren prüfen sämtliche Benutzereingaben.

---

# Besondere Merkmale

- übersichtliche Projektstruktur
- konsequente Trennung der Verantwortlichkeiten
- wiederverwendbare Validatoren
- automatische Nummerngenerierung
- Berechnung und Prüfung des Kontostands
- Soft Delete
- übersichtliche Windows-Desktopoberfläche

---

# Screenshots

## Begrüßungsfenster

<img width="1284" height="746" alt="image" src="./README Images/000 splash window.png" />



---

## Hauptfenster

<img width="1284" height="746" alt="image" src="./README Images/001 main window.png" />



---

## Kunden und Konten

<img width="1291" height="809" alt="image" src="./README Images/002 customer and accounts page.png" />


---

## Buchungen

<img width="1552" height="1032" alt="image" src="./README Images/003 booking page.png" />


---

# Hinweis

Dieses Projekt dient ausschließlich Demonstrations- und Lernzwecken und wurde im Rahmen einer Testaufgabe entwickelt.

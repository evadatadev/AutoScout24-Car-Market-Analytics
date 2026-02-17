# 📘 Analyse, Machine Learning & Dashboard – Projektstruktur

## **Phase 1 — Daten (Aufgabe 1.1)**

### 🎯 Ziel: Daten laden, verstehen, bereinigen.

### **1.1 Daten laden & Überblick**

* `autoscout24.csv` einlesen
* Anzahl Zeilen & Spalten bestimmen
* Datentypen prüfen
* Erste Stichprobe anzeigen (`head()`)

### **1.2 Datenqualität prüfen**

* Fehlende Werte analysieren
* Ausreißer erkennen (Preis, km, PS, Erstzulassung)
* Duplikate entfernen
* Inkonsistente Einträge (z. B. Schreibweisen von Marken)

---

## **Phase 2 — Analyse (Aufgabe 1.2)**

### 🎯 Ziel: Geforderte Analysen + sinnvolle Erweiterungen.

### **2.1 Wie viele Autos wurden verkauft? Über welchen Zeitraum?**

* Anzahl Zeilen
* Min/Max Jahr der Erstzulassung oder Verkaufsdatum

### **2.2 Welche Marken sind erfasst?**

* Herstellerliste
* Häufigkeiten pro Marke

### **2.3 Korrelationen zwischen numerischen Features**

* Numerische Features identifizieren
* Scatterplots (Preis vs. km, Preis vs. PS, PS vs. km, …)
* Korrelationsmatrix berechnen
* Interpretation der Zusammenhänge

### **2.4 Veränderungen über die Jahre**

* Preisentwicklung
* Kilometerstand über Zeit
* PS-Entwicklung
* Herstellertrends

### **2.5 Weitere interessante Fragestellungen**

Beispiele:

* Welche Marken sind besonders preisstabil?
* Welche Autos haben die höchste Laufleistung?
* Saisonale Effekte?
* Unterschiede zwischen Privatverkäufern und Händlern
* Welche Faktoren beeinflussen den Preis am stärksten?

---

## **Phase 3 — Vorbereitung für Machine Learning**

### 🎯 Ziel: Feature-Set bauen, Zielvariable verstehen.

### **3.1 Zielvariable (Preis) untersuchen**

* Verteilung prüfen
* Log-Transformation erwägen
* Outlier-Handling

### **3.2 Feature Engineering**

* Alter aus Erstzulassung berechnen
* Kategorische Features encoden
* Relevante Features auswählen
* Redundante Features entfernen

### **3.3 Skalierung**

* Numerische Features skalieren (StandardScaler / MinMaxScaler)

---

## **Phase 4 — Machine Learning (Aufgabe 1.3)**

### 🎯 Ziel: Preisvorhersage für die Top‑5‑Hersteller.

### **4.1 Top‑5‑Hersteller**

* Hersteller zählen
* Top 5 auswählen
* Datensatz filtern

### **4.2 Durchschnittspreise pro Hersteller**

* Mittelwert
* Median
* Vergleich zwischen Herstellern

### **4.3 Modelltraining**

* Train/Test-Split
* Baseline-Modell (Durchschnittspreis)
* Lineare Regression
* Features: PS, km, Alter, Kraftstoff, Getriebe

### **4.4 Kategorie des ML-Problems**

* Supervised Learning
* Regression

### **4.5 Modellgüte**

* MAE
* RMSE
* R²

### **4.6 Weitere Modelle**

* CatBoost (Auswahl aufgrund von Datensatz mit vielen Kategorien)
* LightGBM (Auswahl aufgrund von vielen Zeilen (30k+)
* XGBoost (Auswahl aufgrund der Erwartung, dass es gut als Benchmark und für Präsentation ist)

### **4.7 Modellvergleich**

* Tabelle aller Modelle + Metriken
* Bestes Modell auswählen
* Feature Importance analysieren

---

## **Phase 5 — Validierung & Interpretation**

### 🎯 Ziel: Modell verstehen und Fehler analysieren.

### **5.1 Residuenanalyse**

* Residuenplots
* Fehlerverteilung

### **5.2 Feature Importance**

* Permutation Importance
* SHAP-Werte (optional)

### **5.3 Fehleranalyse**

* Welche Autos werden schlecht vorhergesagt?
* Muster in Fehlvorhersagen erkennen

---

## **Phase 6 — Dashboard (Aufgabe 1.4)**

### 🎯 Ziel: Ergebnisse visuell ansprechend präsentieren.

### **6.1 Dashboard-Framework**

* Tableau

### **6.2 Inhalte des Dashboards**

* Anzahl verkaufter Autos
* Markenübersicht
* Scatterplots (Korrelationen)
* Zeitliche Trends
* Preisvergleiche der Top‑5‑Hersteller
* Modellvergleich (MAE, RMSE, R²)
* Feature Importance

### **6.3 Design-Hinweise**

* Klare Achsenbeschriftungen
* Einheitliche Farbpalette
* Interaktive Filter (Hersteller, Jahr, PS‑Range)
* Übersichtliche Layoutstruktur

---

## **Phase 7 — Veröffentlichung**

### 🎯 **Ziel:** Ergebnisse professionell aufbereiten und öffentlich zugänglich machen.

## **7.1 Projekt auf GitHub veröffentlichen**

* Repository anlegen (inkl. klarer Ordnerstruktur: `data/`, `notebooks/`, `src/`, `models/`, `dashboard/`)
* README erstellen mit Projektbeschreibung, Vorgehen, Ergebnissen und Screenshots
* Jupyter Notebooks bereinigen (Outputs, Reihenfolge, Kommentare)
* Code dokumentieren und Requirements‑Datei hinzufügen
* Modellartefakte referenzieren
* Lizenz und Kontaktinformationen ergänzen

---

## **7.2 Dashboard über Tableau Public bereitstellen**

* Dashboard final prüfen (Filterlogik, Layout, Farben, Beschriftungen)
* Datenquelle als Extrakt einbetten
* Über Tableau Desktop auf Tableau Public veröffentlichen
* Titel, Kurzbeschreibung und Tags hinzufügen
* Öffentlichen Link generieren und testen
* Link in GitHub‑README einbinden

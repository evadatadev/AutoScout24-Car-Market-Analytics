# 📝 ENTWURF

# 🚗 AutoScout24 – Analyse, Visualisierung & Preisvorhersage

Dieses Projekt untersucht einen Datensatz von AutoScout24 mit Informationen über verkaufte Fahrzeuge.
Ziel ist es, die Daten explorativ zu analysieren, visuell aufzubereiten und ein Machine‑Learning‑Modell zur Vorhersage von Verkaufspreisen zu entwickeln.
Abschließend werden die wichtigsten Erkenntnisse in einem Dashboard dargestellt.

---

## 📁 Projektübersicht

Das Projekt umfasst vier zentrale Bereiche:

1. **Explorative Datenanalyse (EDA)**
2. **Visualisierung & statistische Zusammenhänge**
3. **Machine Learning – Preisvorhersage**
4. **Dashboard – visuelle Aufbereitung der Ergebnisse**

Die Arbeit wurde in mehreren Jupyter Notebooks durchgeführt und durch zusätzliche Dokumente ergänzt.

---

## 📊 Datensatz

**Datei:** `autoscout24.csv`Der Datensatz enthält Informationen über verkaufte Fahrzeuge, u. a.:

- Hersteller
- Modell
- Zulassungsjahr
- Meilenstand
- Kraftstoffart
- Leistung (PS)
- Getriebe
- Preis
- Zustand

**Zentrale Fragen:**

- Wie viele Autos wurden verkauft und über welchen Zeitraum?
- Welche Marken sind vertreten?
- Welche numerischen Features korrelieren miteinander?
- Gibt es Trends über die Jahre hinweg?
- Welche zusätzlichen Muster lassen sich entdecken?

---

## 🔍 Explorative Analyse

Die explorative Analyse (Notebook: `analyse.ipynb`) umfasst:

### ✔ Anzahl der Verkäufe & Zeitraum

Ermittlung des gesamten Beobachtungszeitraums und der Anzahl der Datensätze.

### ✔ Markenübersicht

Welche Hersteller sind am häufigsten vertreten?

### ✔ Korrelationen

Analyse numerischer Merkmale mittels:

- Korrelationsmatrix
- Scatterplots
- Heatmaps

### ✔ Zeitliche Entwicklungen

Untersuchung von Preis‑ und Angebotsveränderungen über die Jahre.

### ✔ Weitere Insights

Zusätzliche Fragestellungen, z. B.:

- Preisverteilung nach Kraftstoffart
- Einfluss von Kilometerstand und Erstzulassung
- Unterschiede zwischen Herstellern

---

## 🤖 Machine Learning

Die Modellierung erfolgt im Notebook `machine_learning.ipynb`.

### ✔ Häufigste Hersteller

Identifikation der **Top‑5‑Hersteller** nach Anzahl der Verkäufe.
Alle weiteren Analysen beziehen sich ausschließlich auf diese Teilmenge.

### ✔ Durchschnittspreise

Berechnung des durchschnittlichen Verkaufspreises pro Hersteller.

### ✔ Modelltraining

Ein Modell (z. B. **Lineare Regression**) wird trainiert, um den Verkaufspreis vorherzusagen.Verwendete Features können u. a. sein:

- Meilenstand
- Zulassung
- Leistung
- Kraftstoffart
- Hersteller

### ✔ Kategorie des Machine Learning

→ **Supervised Learning**, Regressionsproblem.

### ✔ Evaluation

Typische Fehlermetriken:

- **MAE** (Mean Absolute Error)
- **RMSE** (Root Mean Squared Error)
- **R²‑Score**

### ✔ Weitere Modelle

Erprobung alternativer Algorithmen, z. B.:

- Random Forest Regressor
- Gradient Boosting
- Ridge/Lasso Regression

---

## 📊 Dashboard

Ein Dashboard (z. B. Tableau) fasst die wichtigsten Erkenntnisse zusammen:

- Verteilung der Preise
- Trends über die Jahre
- Vergleich der Top‑5‑Hersteller
- Einfluss zentraler Features
- Modellperformance

Ziel ist eine intuitive, visuell ansprechende Darstellung für Betrachter ohne technischen Hintergrund.

---

## 📁 Projektstruktur

autoscout24-analysis/
│
├── data/
│   └── autoscout24.csv
│
├── notebooks/
│   ├── analyse.ipynb
│   └── machine_learning.ipynb
│
├── docs/
│   ├── Arbeitsplan.docx
│   └── Projekt_interview.pdf
│
├── README.md
└── requirements.txt

---

## ⚙️ Installation & Nutzung

```bash
# Repository klonen
git clone <REPO-URL>
cd autoscout24-analysis

# Abhängigkeiten installieren
pip install -r requirements.txt

# Notebooks starten
jupyter notebook
---
```

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
4. **Dashboard – visuelle Aufbereitung der Ergebnisse in Tableau**

Die Arbeit wurde in mehreren Jupyter Notebooks durchgeführt und durch zusätzliche Dokumente ergänzt.

---

## 📊 Datensatz

**Datei:** `autoscout24.csv`

Der Datensatz enthält Informationen über verkaufte Fahrzeuge, u. a.:

- Hersteller
- Modell
- Zulassungsjahr
- Kilometerstand
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

### ✔ Zeitliche Entwicklungen

Untersuchung von Preis‑ und Angebotsveränderungen über die Jahre.

### ✔ Weitere Insights

Zusätzliche Fragestellungen, z. B.:

- Preisverteilung nach Kraftstoffart
- Einfluss von Kilometerstand und Erstzulassung
- Unterschiede zwischen Herstellern

Die explorative Analyse bildet die Grundlage für das spätere Machine‑Learning‑Modell und hilft, Muster, Ausreißer und Zusammenhänge im Datensatz zu verstehen.

---

## 🤖 Machine Learning

Die Modellierung erfolgt im Notebook `machine_learning.ipynb`.

Ziel ist es, den Verkaufspreis eines Autos auf Basis ausgewählter Merkmale vorherzusagen.

## ✔ Häufigste Hersteller

Zunächst werden die **Top‑5‑Hersteller** nach Anzahl der Verkäufe identifiziert.

Alle weiteren Analysen und Modelle beziehen sich ausschließlich auf diese Teilmenge, um die Datenmenge zu fokussieren und Verzerrungen durch seltene Marken zu vermeiden.

## ✔ Durchschnittspreise

Für die Top‑5‑Hersteller werden die **durchschnittlichen Verkaufspreise** berechnet (Mittelwert, Median, Anzahl der Verkäufe).

Dies liefert eine erste Einschätzung über Preisniveaus und Unterschiede zwischen den Herstellern.

## ✔ Modelltraining

Zur Vorhersage des Verkaufspreises wird ein Regressionsmodell trainiert.

Verwendete Features (Phase‑4‑Feature‑Set):

* **hp** (Leistung in PS)
* **mileage** (Kilometerstand)
* **car_age** (Fahrzeugalter)
* **fuel** (Kraftstoffart)
* **gear** (Getriebe)

Die Zielvariable ist der logarithmierte Preis (`price_log`), um Ausreißer zu reduzieren und die Verteilung zu glätten.

Es werden mehrere Modelle getestet:

* **Lineare Regression**
* **CatBoost Regressor**
* **LightGBM Regressor**
* **XGBoost Regressor**

Alle Modelle laufen über eine einheitliche **Preprocessing‑Pipeline** (Imputation, Skalierung, One‑Hot‑Encoding).

## ✔ Kategorie des Machine Learning

→  **Supervised Learning** , genauer: **Regression**

Das Modell sagt einen kontinuierlichen Wert (Preis) vorher.

## ✔ Evaluation

Zur Bewertung der Modellgüte werden folgende Fehlermetriken verwendet:

* **MAE** (Mean Absolute Error)
* **RMSE** (Root Mean Squared Error)
* **R²‑Score** (Erklärte Varianz)

Zusätzlich wird eine **Baseline** berechnet, die immer nur den Durchschnittspreis des Trainingssets vorhersagt.

Alle Modelle übertreffen die Baseline deutlich.

## ✔ Modellvergleich

Die Boosting‑Modelle (CatBoost, LightGBM, XGBoost) erzielen die besten Ergebnisse.

Das beste Modell ist **CatBoost** mit:

* sehr niedrigem MAE
* geringstem RMSE
* höchstem R² (≈ 0.91)

## ✔ Feature Importance

Für das beste Modell wird die **Feature Importance** analysiert.

Die wichtigsten Einflussfaktoren auf den Preis sind:

1. **Leistung (hp)**
2. **Fahrzeugalter (car_age)**
3. **Kilometerstand (mileage)**
4. **Kraftstoffart**
5. **Getriebe**

Die Ergebnisse sind plausibel und spiegeln typische Marktmechanismen im Gebrauchtwagenhandel wider.

---

## 📊 Dashboard

Ein Dashboard (z. B. Tableau) fasst die wichtigsten Erkenntnisse zusammen:

- Verteilung der Preise
- Trends über die Jahre
- Vergleich der Top‑5‑Hersteller
- Einfluss zentraler Features
- Modellperformance

Ziel ist eine intuitive, visuell ansprechende Darstellung für Betrachter ohne technischen Hintergrund.

Dashboard live ansehen unter:

🔗 https://public.tableau.com/views/Dashboard_AutoScout24/Dashboard?:language=de-DE&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

---

## 📁 Projektstruktur

```
autoscout24-analysis/
│
├── data/ 		# autoscout24.csv, feature_importance.csv ...
├── notebooks/		# EDA-Analyse, Machine-Learning-Notebook
├── docs/		# Aufgabenstellung, Arbeitsplan
├── README.md
└── requirements.txt
```

---

## 🐍 Python‑Version

Dieses Projekt wurde mit **Python 3.13** entwickelt und getestet.

---

## ⚙️ Installation & Nutzung

```bash
# Repository klonen
git clone https://github.com/evadatadev/AutoScout24-Car-Market-Analytics.git
cd autoscout24-analysis

# Abhängigkeiten installieren
pip install -r requirements.txt

# Notebooks starten
jupyter notebook
---
```

---

## 📄 Lizenz

MIT License

---

## 🤝 Mitwirken

Pull Requests und Issues sind willkommen.

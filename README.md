<div align="center">

<img src="assets/banner.svg" alt="José Manuel Rojas — Reliability Engineer" width="100%" />

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Barlow&weight=500&size=24&pause=1200&color=6FA3BD&center=true&vCenter=true&width=640&lines=Turning+measured+signals+into+diagnostics;Condition+monitoring+for+mining+assets;From+the+sensor+to+the+maintenance+decision;Signal+processing+%C2%B7+ML+%C2%B7+Software" alt="Typing animation" />
</a>

<br/>

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

</div>

## 👋 About me

**Reliability engineer** with an electronics engineering background and almost five years turning measured signals into diagnostics, the most recent one in copper mining. At Salfa Mantenciones I lead initiatives to assess the health of mine and fixed-plant assets from vibration, thermography and electrical data, and I develop the models and the software to analyze them, so I move comfortably between field maintenance teams and the people who build predictive models. Before that I was a research engineer in voice laboratories at Universidad Técnica Federico Santa María and Boston University, measuring physiological signals and developing metrics to support clinical diagnosis.

I like problems where physics, data and software meet, and where "it works on my bench" is not good enough: validated against standards, covered by tests, and documented with the reasoning behind each decision.

## 🔭 What I'm working on

**Asset health in mining (Salfa Mantenciones, Oct 2025 – present)**

- Leading a condition-monitoring initiative for the ventilation fleet of a large underground copper mine, an operation-and-maintenance contract covering 273 assets, now in implementation with a staged plan to scale to the rest of the fleet.
- Detected fan imbalance from the vibration measurements of inspection rounds, tracked how it worsened over time, and built predictive models on that trend to schedule maintenance at the optimal moment. With vibration I also characterized blade damage, structural looseness, aerodynamic problems and impacts.
- Combine vibration with the operating variables of the variable-frequency drive (current, voltage, power) to assess motor heating, load and operating regime.
- Analyzed about 1,300 maintenance records and 69 failures to identify the fleet's chronic defects and which ones vibration and temperature can detect earlier (23% of failures). Prioritized critical equipment with the field reliability team using a GUT matrix (gravity, urgency, trend); the 250 HP injection fans, whose failure stops a sector of the mine, came first.
- Running a telemetry monitoring pilot on five pumps of a leaching plant; cavitation is the main finding in their vibration data so far.
- Leading the design of a thermographic inspection service for conveyor belts with a quadruped robot: defined when a measurement is valid, proposed temperature alert thresholds, and designed false-positive handling that combines visible and infrared imagery.
- From data to maintenance decisions: alert criteria, a severity scale (observation / alert / critical) and the flow to communicate findings to maintenance; Power BI management dashboards to estimate the return on predictive maintenance; sensor and gateway procurement managed in SAP.

**Software I build for it**

- **Reliability Dashboard** — a web platform that shows the health of each asset: status per equipment, trends, spectra and alarms with hysteresis, plus management screens (availability, savings estimator, ROI). Python (Flask + Jinja) with server-side rendering, TypeScript modules per page, PostgreSQL, an idempotent alarm engine inside the ingestion transaction, and blocking CI gates. On a 10-phase roadmap toward a Cloud Run deployment and a predictive-maintenance engine.
- **Diagnostics pipeline** — a Python toolkit that turns raw vibration signals into ranked fault hypotheses: it filters the signal, computes its spectrum, estimates rotating speed, and compares each measurement against a statistical baseline of the same mounting. Follows ISO 13373 and ISO 20816 as guides. Validated experimentally on a lab test rig.
- **ML study for fault diagnostics** — a comparison of machine-learning models for anomaly detection and fault classification from vibration signals (Isolation Forest, One-Class SVM, LOF, Autoencoder, Random Forest, XGBoost, SVM, MLP) on a public bearing-fault dataset, and a two-stage scheme (anomaly gate → fault classifier) with a multi-axis structure that adapts to different machines; ~99.8% accuracy on the classifier stage.
- **Robotic inspection platform** (private) — the platform-first demo behind the robotic inspection service: the robot is just one data source behind a port/adapter boundary, so the platform, its decision chain and its audit trail come first.

## 🎯 Side projects (built in my free time)

- **Data-acquisition firmware for microcontrollers** (C/C++, with Python host tooling) — multi-core firmware with a documented binary session format and integrity checks, and a version that sends the measurements to AWS over Wi-Fi at the maximum rate the hardware allows.
- **Flight Finder** — a personal flight-price monitor in Python: it queries fares on a schedule, stores the price history in SQLite, and alerts me when a price drops clearly below the norm for a route and date. Built with a pluggable provider design, YAML configuration, and linting/type checks (ruff, mypy, pytest).

## 💼 Experience & education

- **Salfa Mantenciones (SalfaCorp)** — Reliability Engineer · Santiago, Chile · Oct 2025 – present. Fixed-plant maintenance company with a presence in large-scale mining.
- **STEPP Lab for Sensorimotor Rehabilitation Engineering, Boston University** — Research Engineer · Boston, MA · Jul 2023 – Sep 2025. Measured and analyzed physiological signals from 200+ people (Parkinson's disease, dystonia and controls): neck vibration to detect vocal overuse, air pressure to estimate pulmonary performance, and tongue and mouth movements. Processed signals in Python and MATLAB (FFT, periodogram, Welch, wavelets; classical and adaptive filters), diagnosed faults in the measurement equipment, designed a respiration-sensor calibration procedure the lab still uses, and refined metrics for the diagnostic assessment of laryngeal dystonia. Co-author of two papers in preparation.
- **Voice Production Laboratory, Universidad Técnica Federico Santa María** — Research Engineer · Valparaíso, Chile · Dec 2021 – Jun 2023. Thesis: a deep neural network that replaces the finite-element model of the larynx inside LaDIVA, a neurocomputational model of speech; it outputs 20 temporal and spectral features and agrees 99% with the original model. Acquired data with human participants under experimental protocols and ethics regulations, recruiting 50+ people for EEG studies.
- **Universidad Técnica Federico Santa María** — Electronics Engineer (Ingeniero Civil Electrónico), 2016 – 2022. Teaching assistant for Digital Signal Processing and Applications (2021 – 2022): weekly review sessions on the Z transform, Fourier transform and digital filter design.
- **Pontificia Universidad Católica de Chile, Clase Ejecutiva UC** — Leadership and coaching skills for team training, 2026.

## 🧰 Skills & tools

<div align="center">

<img src="https://skillicons.dev/icons?i=py,matlab,r,ts,js,cpp,c,bash,powershell,html,css,react,flask,fastapi,postgres,sqlite,sklearn,pytorch,tensorflow,docker,githubactions,git,gcp,aws,azure,vscode,linux&perline=9" alt="Skills" />

</div>

<br/>

| Area | What I am currently working with |
|---|---|
| **Condition monitoring** | Vibration analysis (imbalance, structural looseness, blade faults, cavitation) · thermography · electrical variables from variable-frequency drives (current, voltage, power) · telemetry · wireless sensors for hazardous (Ex) areas |
| **Methods & standards** | GUT matrix to prioritize critical equipment · failure-mode analysis from maintenance history · ISO 13373, 13374, 17359 and 20816 |
| **Signal processing & models** | Spectral analysis (FFT, periodogram, Welch, wavelets) · classical and adaptive digital filters · feature extraction · anomaly detection and fault classification with machine learning · deep neural networks |
| **Programming & data** | **Python** (pandas, NumPy, SciPy, scikit-learn, XGBoost, PyTorch, TensorFlow) · **MATLAB** · R · SQL and PL/pgSQL · **TypeScript** · JavaScript · **C / C++** · Bash / PowerShell · Power BI |
| **Maintenance systems & software** | SAP · PostgreSQL · SQLite · Flask · FastAPI · React · REST APIs · Docker · Git / GitHub Actions |
| **Embedded & IoT** | Microcontroller firmware (C/C++, multi-core) · PlatformIO · SPI / I²C · MQTT · binary data formats with integrity checks |
| **Architecture & quality** | Hexagonal (ports & adapters) · canonical data contracts · ADRs · pytest / vitest · mypy · security-minded reviews (CSP, CORS allowlists, output escaping) |
| **Cloud** | Google Cloud (Cloud Run / Cloud SQL) · AWS · Azure |
| **Languages** | Spanish (native) · English (C1, IELTS 7.5) · Portuguese (basic) |

## 🧪 Selected highlights

- Built a condition-monitoring stack end to end — acquisition firmware, diagnostics pipeline, ML models and web platform — each piece tested and documented.
- Diagnostic engine with **robust speed estimation** that stays reliable when the dominant signal component is weak, a common failure mode of simple peak-picking in real installations.
- Learned the hard way that **test setup matters as much as algorithms**: identified when lab artifacts invalidate a diagnostic indicator, and documented the limitation instead of tuning around it.
- Treat architecture decisions as first-class artifacts: **50+ ADRs** for the platform, each with context, decision and consequences.
- Thesis: a **deep neural network** that replaces a finite-element laryngeal model with 99% agreement, inside a neurocomputational model of speech.

## 🔒 About my repositories

Most of my projects are in **private repositories** because they involve industrial data and business context that can't be made public. If you'd like more details about any of them (architecture, results, design decisions), **feel free to get in touch** and I'll be happy to walk you through them.

## 🌱 Currently learning / exploring

Predictive maintenance (remaining-useful-life forecasting with prediction intervals), event-driven architectures with NATS JetStream, Cloud Run deployments with automated migrations and rollback, and a native Android client.

## 💬 Ask me about

Condition monitoring · vibration analysis and thermography · electrical variables from VFDs · predictive maintenance · feature engineering for machine health · ML for anomaly detection · designing clean, testable backends.

## 📫 Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-JosemaRojas1-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/JosemaRojas1)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Jos%C3%A9%20Manuel%20Rojas-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jos%C3%A9-manuel-rojas-95b9a31bb)
[![Email](https://img.shields.io/badge/Email-jose.rojaso%40sansano.usm.cl-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jose.rojaso@sansano.usm.cl)

<img src="assets/footer.svg" alt="" width="100%" />

</div>

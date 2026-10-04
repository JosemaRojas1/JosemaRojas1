# Hi, I'm Josema Rojas 👋

**IoT & reliability engineer** building condition-based monitoring (CBM) systems end to end: from the sensor and firmware, through signal processing and machine learning, to the web platform that turns vibration data into maintenance decisions.

I like problems where physics, data and software meet, and where "it works on my bench" is not good enough: validated against standards, covered by tests, and documented with the reasoning behind each decision.

## 🔭 What I'm working on

- **Reliability Dashboard** — a web platform for condition monitoring of industrial fan fleets: per-asset health status, RMS/temperature trends, spectra and waveforms, an alarm inbox with hysteresis, and management screens (availability, savings estimator, ROI). Flask + Jinja with server-side rendering, TypeScript modules per page, PostgreSQL, an idempotent alarm engine inside the ingestion transaction, and blocking CI gates. Currently on a 10-phase roadmap toward a Cloud Run deployment and a predictive-maintenance engine.
- **Vibration analysis pipeline** — a Python toolkit that parses raw triaxial accelerometer sessions and produces diagnostics: Welch PSD, cepstrum-based RPM estimation, envelope analysis, harmonic/sideband profiles, z-score baselines per mounting, and fault hypotheses ranked against a healthy baseline (imbalance, blade damage, aerodynamic turbulence, looseness, impacts). Validated experimentally on a lab fan test rig.
- **ML study for vibration diagnostics** — a benchmark of eight architectures on the CWRU bearing dataset (Isolation Forest, One-Class SVM, LOF, Autoencoder, Random Forest, XGBoost, SVM, MLP) and a two-stage pipeline (anomaly gate → fault classifier) reaching ~99.8% accuracy on the classifier stage. A generic 3-axis industrial template is ready for a real-machine pilot.
- **Robotic inspection platform** (private) — a platform-first demo for autonomous inspection of conveyor idlers, where the robot is just one data source behind a port/adapter boundary.

## 🎯 Side projects (built in my free time)

- **V3 AWS Wi-Fi Vibration Monitoring** — the cloud-connected evolution of my local ESP32 + ADXL345 acquisition firmware (C/C++ with Python tooling), sending vibration data to AWS over Wi-Fi while keeping the maximum 3.2 kHz sampling rate imposed by the sensor.
- **Flight Finder** — a personal flight-price monitor in Python: it queries fares on a schedule, stores the price history in SQLite, and alerts me when a price drops clearly below the norm for a route and date. Built with a pluggable provider design, YAML configuration, and linting/type checks (ruff, mypy, pytest).

## 🧰 Skills & tools

| Area | What I use |
|---|---|
| **Languages** | **Python** (primary, incl. MicroPython and Jupyter) · **TypeScript** · JavaScript · **C / C++** · SQL and PL/pgSQL · HTML / CSS (Jinja templates) · Bash / PowerShell · Makefile · Dockerfile |
| **Embedded & IoT** | ESP32 (dual-core, FreeRTOS-style task split) · PlatformIO · SPI · ADXL345 / MPU6050 · LittleFS · MQTT · binary formats with CRC32 |
| **Signal processing** | Welch PSD · FFT · cepstrum · Hilbert envelope · kurtosis / crest factor · ISO 20816 velocity severity · SciPy · NumPy |
| **Machine learning** | scikit-learn · XGBoost · Autoencoders · Isolation Forest · feature engineering · anomaly detection · transfer-learning trade-offs |
| **Backend & data** | Flask · FastAPI · PostgreSQL · SQLite · Parquet · pandas · REST / SSE · NATS JetStream · OIDC (Auth0) |
| **Architecture** | Hexagonal (ports & adapters) · canonical data contracts · ADRs · multi-tenant access control · idempotent ingestion |
| **DevOps & quality** | Docker · GitHub Actions · pytest / vitest · mypy · Dependabot · security-minded reviews (CSP, CORS allowlists, output escaping) |
| **Cloud** | Google Cloud (Cloud Run / Cloud SQL, in progress) · AWS (Lambda / EC2 / SageMaker, explored for the ML module) |
| **Standards & domain** | ISO 13373 · ISO 17359 · ISO 20816 · vibration-based fault diagnosis · reliability / CBM |

## 🧪 Selected highlights

- Designed a **dual-core acquisition firmware** for the ESP32 + ADXL345 sampling at 3.2 kHz, with a documented binary session format, CRC32 integrity checks, and host tools for transfer and conversion.
- Built a diagnostic engine whose **cepstrum-based RPM estimation** stays reliable when the 1× component is weak, a common failure mode of peak-picking in real installations.
- Learned the hard way that **setup matters as much as algorithms**: identified when lab mounting artifacts (e.g. viscoelastic tape resonances) invalidate a diagnostic indicator, and documented the limitation instead of tuning around it.
- Treat architecture decisions as first-class artifacts: **50+ ADRs** for the platform, each with context, decision and consequences.

## 🔒 About my repositories

Most of my projects are in **private repositories** because they involve industrial data and business context that can't be made public. If you'd like more details about any of them (architecture, results, design decisions), **feel free to get in touch** and I'll be happy to walk you through them. See the contact section below.

## 🌱 Currently learning / exploring

Predictive maintenance (remaining-useful-life forecasting with prediction intervals), event-driven architectures with NATS JetStream, Cloud Run deployments with automated migrations and rollback, and a native Android client.

## 💬 Ask me about

Vibration analysis · condition monitoring · ESP32 data acquisition · feature engineering for machine health · ML for anomaly detection · designing clean, testable backends.

## 📫 Contact

- GitHub: [@JosemaRojas1](https://github.com/JosemaRojas1)
- Email: rojaso.josema@gmail.com


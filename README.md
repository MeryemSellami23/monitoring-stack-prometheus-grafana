# 📊 Infrastructure Monitoring Stack (Prometheus & Grafana)

## 📝 Description
Ce projet met en place une solution complète d'observabilité pour surveiller l'infrastructure, les containers Docker, et la disponibilité des services en temps réel.

## 🛠️ Stack Technique
- **Prometheus**: Collecte des métriques.
- **Grafana**: Visualisation des données et Alerting.
- **Loki & Promtail**: Centralisation des logs.
- **Exporters**: 
  - `Node Exporter` (Système)
  - `cAdvisor` (Containers)
  - `Blackbox Exporter` (Uptime/HTTP)

## 🏗️ Architecture
L'infrastructure est entièrement conteneurisée avec **Docker Compose**.

Lancez les services :

Bash
docker-compose up -d
Accédez à Grafana sur : http://localhost:3000

📊 Dashboards & Alerting
Infrastructure: Vue détaillée sur CPU/RAM/Disk.

Logs: Consultation des logs Docker via Loki.

Alertes: Notifications configurées pour le temps de réponse et l'état des services (Up/Down).


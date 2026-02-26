<img width="959" height="487" alt="node_exporter" src="https://github.com/user-attachments/assets/ed91da03-0f2c-417e-8296-fbf6702edfaa" /># 📊 Comprehensive Monitoring & Observability Stack

## 📝 Description du Projet
Ce projet met en place une infrastructure complète de supervision en utilisant la stack **Prometheus & Grafana**. L'objectif est de centraliser les métriques de performance, les logs et la disponibilité des services dans une interface unique, avec un système d'alerte proactif.

---

## 🖼️ Aperçu du Tableau de Bord (Screenshots)

### 1. 🖥️ Infrastructure Monitoring (Node Exporter)
Surveillance complète du serveur Linux : Utilisation du **CPU**, **Mémoire RAM**, et espace **Disque**.
<img width="959" height="487" alt="node_exporter" src="https://github.com/user-attachments/assets/0ace6385-6bf2-4a47-96de-700ee4c9e9fa" />

### 2. 🐳 Container Insights (cAdvisor)
Visualisation des ressources consommées par chaque container Docker (CPU/RAM par container).

<img width="959" height="453" alt="cadvisor" src="https://github.com/user-attachments/assets/ee817345-32d0-47dd-8d5c-c36b5df87fb6" />

### 3. 🌐 Disponibilité Web (Blackbox Exporter)
Vérification de l'état "Up/Down" et du temps de réponse (Latency) des sites web via sondes HTTP.


---<img width="926" height="371" alt="blackbox" src="https://github.com/user-attachments/assets/fa6c725f-3faf-4bb1-b2ea-20e22970c3ad" />


## 🚨 Alerting & Notifications (Proactive Response)

Le système est configuré pour détecter automatiquement les anomalies et envoyer des notifications immédiates.

### 📉 Alertes Configurées :
- **Website Down** : Alerte critique si le site web ne répond plus (Blackbox).
- **CPU High Usage** : Notification si la charge processeur dépasse 80%.
- **Container Down** : Alerte si un service Docker essentiel s'arrête.

<img width="955" height="331" alt="alert_websitedown" src="https://github.com/user-attachments/assets/d4a0b416-8fe9-4928-b086-b511834e2152" />
<img width="923" height="355" alt="alert_cpu" src="https://github.com/user-attachments/assets/22db7dc4-f166-44a5-b583-bfe3084ffce4" />

### 📧 Exemple de Notification Mail
Voici l'alerte reçue par email via **Grafana Alerting** :


---<img width="943" height="413" alt="mail" src="https://github.com/user-attachments/assets/64810561-5d73-4e51-b4ce-e520dfe4be4c" />


## 🛠️ Stack Technique
- **Prometheus** : Base de données temporelle (Metrics).
- **Grafana** : Visualisation et Alert Management.
- **Node Exporter** : Métriques Système.
- **cAdvisor** : Métriques Containers.
- **Blackbox Exporter** : Métriques de disponibilité (Probe).
- **Loki & Promtail** : Centralisation des Logs.
## 🚀 Comment lancer le projet ?

Pour déployer toute cette infrastructure sur votre machine, suivez ces étapes :

1. **Cloner le projet :**
   ```bash
   git clone [https://github.com/MeryemSellami23/monitoring-stack-prometheus-grafana.git](https://github.com/MeryemSellami23/monitoring-stack-prometheus-grafana.git)
   cd monitoring-stack-prometheus-grafana
Lancer les containers avec Docker Compose :

Bash
docker-compose up -d
Accéder aux interfaces :

Grafana : http://localhost:3000 (Login: admin / admin)

Prometheus : http://localhost:9090

Vérifier l'état :
Toutes les cibles (targets) doivent être en état UP dans Prometheus.

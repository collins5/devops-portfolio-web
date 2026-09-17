# 🚀 Web Portfolio

> Persönliches Web-Portfolio zur Präsentation meiner Projekte, technischen Fähigkeiten und meiner praktischen Entwicklung im Bereich Software Engineering und DevOps.

---

## 📑 Inhaltsverzeichnis

* [Über das Projekt](#-über-das-projekt)
* [Projektziele](#-projektziele)
* [Architektur](#-architektur)
* [Technologie-Stack](#-technologie-stack)
* [Projektstruktur](#-projektstruktur)
* [Voraussetzungen](#-voraussetzungen)
* [Installation](#-installation)
* [Konfiguration](#-konfiguration)
* [Lokaler Start](#-lokaler-start)
* [Docker](#-docker)
* [CI/CD](#-cicd)
* [Deployment](#-deployment)
* [Kubernetes](#-kubernetes)
* [Testing](#-testing)
* [Monitoring und Logging](#-monitoring-und-logging)
* [Security](#-security)
* [Troubleshooting](#-troubleshooting)
* [Lessons Learned](#-lessons-learned)
* [Roadmap](#-roadmap)
* [Autor](#-autor)

---

## 📖 Über das Projekt

### Was ist dieses Projekt?

[Kurze Beschreibung des Web-Portfolios.]

Dieses Projekt dient als persönliches Web-Portfolio und gleichzeitig als praktische Umgebung zur Anwendung moderner Entwicklungs- und DevOps-Methoden.

### Warum wurde das Projekt erstellt?

Mit diesem Web-Portfolio-Projekt verfolge ich zwei wesentliche Ziele. Einerseits nutze ich es als praxisnahes Lernprojekt, um den gesamten Lebenszyklus einer Anwendung - von der Konzeption über die Implementierung bis zum Deployment - eigenständig umzusetzen. 
Andererseits bietet es mir als angehendem DevOps-Engineer eine Plattform, um meine Lernfortschritte und meine fachliche Entwicklung kontinuierlich zu dokumentieren. 

Beispiel:

* Präsentation meiner technischen Projekte
* Dokumentation meiner praktischen DevOps-Erfahrungen
* Aufbau einer reproduzierbaren Deployment-Umgebung
* Anwendung von Linux, Docker, CI/CD und Kubernetes
* Automatisierung von Build-, Test- und Deployment-Prozessen

---

## 🎯 Projektziele

Die wichtigsten Ziele dieses Projekts sind:

* [ ] Professionelles Web-Portfolio erstellen
* [ ] Entwicklungsumgebung reproduzierbar aufbauen
* [ ] Git-basierte Versionsverwaltung verwenden
* [ ] Webserver mit Nginx bereitstellen
* [ ] Anwendung containerisieren
* [ ] CI/CD-Pipeline implementieren
* [ ] Test- und Produktionsumgebung trennen
* [ ] Deployment automatisieren
* [ ] Kubernetes-Deployment umsetzen
* [ ] Monitoring und Logging integrieren
* [ ] Technische Dokumentation pflegen

---

## 🏗️ Architektur

### Architekturübersicht

[Hier die Architektur des Projekts beschreiben.]

Beispiel:

```text
                    Internet
                       │
                       ▼
                  HTTPS / TLS
                       │
                       ▼
                  ┌─────────┐
                  │  Nginx  │
                  └────┬────┘
                       │
                       ▼
              ┌─────────────────┐
              │  Web Portfolio  │
              └─────────────────┘
```

Bei einer Kubernetes-Architektur könnte die Struktur beispielsweise erweitert werden:

```text
Internet
   │
   ▼
Ingress Controller
   │
   ▼
Kubernetes Service
   │
   ▼
Deployment
   │
   ├── Pod
   ├── Pod
   └── Pod
```

### Architekturentscheidungen

| Entscheidung | Begründung   |
| ------------ | ------------ |
| Nginx        | [Begründung] |
| Docker       | [Begründung] |
| GitLab CI/CD | [Begründung] |
| Kubernetes   | [Begründung] |
| Helm         | [Begründung] |

---

## 🛠️ Technologie-Stack

| Technologie             | Aufgabe                    | Version     |
| ----------------------- | -------------------------- | ----------- |
| Linux / Ubuntu          | Host-System                | `[Version]` |
| HTML / CSS / JavaScript | Frontend                   | `[Version]` |
| Nginx                   | Webserver / Reverse Proxy  | `[Version]` |
| Git                     | Versionsverwaltung         | `[Version]` |
| Docker                  | Containerisierung          | `[Version]` |
| Docker Compose          | Lokale Orchestrierung      | `[Version]` |
| GitLab CI/CD            | CI/CD-Automatisierung      | `-`         |
| Kubernetes              | Container-Orchestrierung   | `[Version]` |
| kubectl                 | Kubernetes CLI             | `[Version]` |
| Helm                    | Kubernetes Package Manager | `[Version]` |

> Die Tabelle sollte nur Technologien enthalten, die tatsächlich im Projekt verwendet werden.

---

## 📂 Projektstruktur

```text
web-portfolio/
│
├── src/
│   ├── index.html
│   ├── css/
│   ├── js/
│   └── assets/
│
├── nginx/
│   └── nginx.conf
│
├── docker/
│   └── ...
│
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
├── Dockerfile
├── docker-compose.yml
├── .gitlab-ci.yml
├── .gitignore
├── .env.example
└── README.md
```

### Wichtige Verzeichnisse

| Verzeichnis / Datei  | Beschreibung                    |
| -------------------- | ------------------------------- |
| `src/`               | Quellcode des Web-Portfolios    |
| `nginx/`             | Nginx-Konfiguration             |
| `docker/`            | Docker-spezifische Dateien      |
| `k8s/`               | Kubernetes-Manifeste            |
| `Dockerfile`         | Definition des Container-Images |
| `docker-compose.yml` | Lokale Container-Orchestrierung |
| `.gitlab-ci.yml`     | CI/CD-Pipeline                  |
| `.env.example`       | Beispiel für Umgebungsvariablen |

---

## ⚙️ Voraussetzungen

Für die lokale Ausführung werden folgende Werkzeuge benötigt:

```text
Git
Docker
Docker Compose
```

Für Kubernetes zusätzlich:

```text
kubectl
Minikube / k3d
Helm
```

### Installation überprüfen

```bash
git --version

docker --version

docker compose version

kubectl version --client

helm version
```

---

## 📥 Installation

### 1. Repository klonen

```bash
git clone <REPOSITORY-URL>
```

### 2. Projektverzeichnis öffnen

```bash
cd web-portfolio
```

### 3. Repository überprüfen

```bash
git status
```

---

## 🔧 Konfiguration

Falls Umgebungsvariablen benötigt werden:

```bash
cp .env.example .env
```

Beispiel:

```env
APP_ENV=development
APP_PORT=8080
```

### Umgang mit Secrets

Sensible Daten dürfen nicht im Git-Repository gespeichert werden.

Beispiele:

```text
Passwords
API Keys
Private Keys
Tokens
Certificates
```

Die lokale `.env`-Datei sollte deshalb in `.gitignore` eingetragen werden:

```gitignore
.env
```

---

## 💻 Lokaler Start

[Hier dokumentieren, wie das Portfolio ohne Container gestartet wird.]

Beispiel:

```bash
nginx -t

sudo systemctl start nginx
```

Status überprüfen:

```bash
systemctl status nginx
```

Anwendung anschließend aufrufen:

```text
http://localhost
```

---

## 🐳 Docker

### Docker Image bauen

```bash
docker build -t web-portfolio:latest .
```

### Container starten

```bash
docker run -d \
  --name web-portfolio \
  -p 8080:80 \
  web-portfolio:latest
```

### Laufende Container überprüfen

```bash
docker ps
```

### Logs anzeigen

```bash
docker logs web-portfolio
```

### Container stoppen

```bash
docker stop web-portfolio
```

### Container entfernen

```bash
docker rm web-portfolio
```

---

## 🐳 Docker Compose

Container starten:

```bash
docker compose up -d
```

Status überprüfen:

```bash
docker compose ps
```

Logs anzeigen:

```bash
docker compose logs -f
```

Umgebung stoppen:

```bash
docker compose down
```

---

## 🔄 CI/CD

### Pipeline-Ziel

Die CI/CD-Pipeline automatisiert:

```text
Code
  │
  ▼
Build
  │
  ▼
Test
  │
  ▼
Package
  │
  ▼
Deploy
```

### Pipeline-Stages

```yaml
stages:
  - build
  - test
  - package
  - deploy
```

### Workflow

```text
Developer
   │
   │ git push
   ▼
Git Repository
   │
   ▼
CI/CD Pipeline
   │
   ├── Build
   ├── Test
   ├── Docker Image
   └── Deployment
```

### Branch-Strategie

| Branch      | Umgebung    | ZweckWelche wichtige Fragen können mich bei der Verfassung einer gut technisch strukturierten Readme-Doku für ein Web-Portfolio-Projekt begleiten? |
| ----------- | ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `feature/*` | Development | Feature-Entwicklung                                                                                                                                |
| `develop`   | Test        | Integration und Tests                                                                                                                              |
| `main`      | Production  | Produktionsstand                                                                                                                                   |

> Branch-Strategie an die tatsächliche Projektstruktur anpassen.

---

## 🚀 Deployment

### Umgebungen

Das Projekt verwendet folgende Umgebungen:

```text
Development
     │
     ▼
Testing
     │
     ▼
Production
```

### Development

[Development-Umgebung beschreiben.]

### Testing

[Testumgebung und Deployment-Prozess beschreiben.]

### Production

[Produktionsumgebung und Deployment-Prozess beschreiben.]

### Rollback

[Dokumentieren, wie eine vorherige funktionierende Version wiederhergestellt werden kann.]

---

## ☸️ Kubernetes

### Kubernetes-Ressourcen

Das Deployment kann folgende Ressourcen verwenden:

```text
Namespace
Deployment
Service
ConfigMap
Secret
Ingress
```

### Deployment ausführen

```bash
kubectl apply -f k8s/
```

### Pods überprüfen

```bash
kubectl get pods
```

### Services überprüfen

```bash
kubectl get services
```

### Deployment überprüfen

```bash
kubectl get deployments
```

### Logs anzeigen

```bash
kubectl logs <POD-NAME>
```

### Detaillierte Fehleranalyse

```bash
kubectl describe pod <POD-NAME>
```

---

## 🧪 Testing

### Welche Tests existieren?

* [ ] Funktionale Tests
* [ ] Integrationstests
* [ ] Container-Tests
* [ ] Nginx-Konfigurationstest
* [ ] Deployment-Test
* [ ] Healthcheck
* [ ] Security Scan

### Beispiel: Nginx-Konfiguration testen

```bash
nginx -t
```

### HTTP-Verfügbarkeit testen

```bash
curl -I http://localhost
```

Erwartetes Ergebnis:

```text
HTTP/1.1 200 OK
```

---

## 📊 Monitoring und Logging

### Docker Logs

```bash
docker logs <CONTAINER>
```

### Kubernetes Logs

```bash
kubectl logs <POD>
```

### Nginx Access Log

```bash
tail -f /var/log/nginx/access.log
```

### Nginx Error Log

```bash
tail -f /var/log/nginx/error.log
```

### Monitoring

[Beschreiben, welche Monitoring-Lösung verwendet wird.]

Beispiele:

```text
Prometheus
Grafana
Kubernetes Metrics
Healthchecks
```

---

## 🔐 Security

Folgende Sicherheitsmaßnahmen werden im Projekt berücksichtigt:

* Keine Secrets im Git-Repository
* Verwendung von `.env` bzw. Secret Management
* HTTPS/TLS für Produktionssysteme
* Minimierung öffentlich erreichbarer Ports
* Regelmäßige Aktualisierung der Container-Images
* Container möglichst ohne Root-Rechte
* Trennung von Development, Testing und Production
* Prüfung externer Dependencies

### Security Checks

[Dokumentieren, welche Security-Tools oder Prüfungen verwendet werden.]

---

## 🔍 Troubleshooting

Dieser Abschnitt dokumentiert reale Fehler, deren Ursachen und Lösungen.

### Problem 1: Nginx liefert `502 Bad Gateway`

**Symptom**

```text
502 Bad Gateway
```

**Analyse**

```bash
systemctl status nginx

curl http://localhost:<BACKEND-PORT>

tail -f /var/log/nginx/error.log
```

**Ursache**

[Ermittelte Ursache dokumentieren.]

**Lösung**

[Durchgeführte Lösung dokumentieren.]

---

### Problem 2: Docker Container startet nicht

**Analyse**

```bash
docker ps -a

docker logs <CONTAINER>

docker inspect <CONTAINER>
```

**Ursache**

[Ursache]

**Lösung**

[Lösung]

---

### Problem 3: Kubernetes Pod startet nicht

**Analyse**

```bash
kubectl get pods

kubectl describe pod <POD>

kubectl logs <POD>
```

**Ursache**

[Ursache]

**Lösung**

[Lösung]

---

## 🧠 Lessons Learned

Dieser Abschnitt dokumentiert wichtige technische Erkenntnisse aus dem Projekt.

### Linux / Nginx

* [Was habe ich gelernt?]
* [Welche Probleme sind aufgetreten?]
* [Wie wurden sie gelöst?]

### Docker

* [Was habe ich über Containerisierung gelernt?]
* [Welche Best Practices habe ich angewendet?]

### CI/CD

* [Was habe ich über Automatisierung gelernt?]
* [Welche Pipeline-Probleme musste ich lösen?]

### Kubernetes

* [Welche Kubernetes-Konzepte habe ich praktisch angewendet?]
* [Welche Troubleshooting-Erfahrungen habe ich gesammelt?]

### DevOps

Zusammenfassend habe ich durch dieses Projekt praktische Erfahrungen in folgenden Bereichen gesammelt:

```text
Linux Administration
Webserver Management
Git
Containerization
CI/CD
Infrastructure Configuration
Deployment Automation
Kubernetes
Monitoring
Troubleshooting
```

---

## 🗺️ Roadmap

### Phase 1 – Grundlagen

* [ ] Repository erstellen
* [ ] Portfolio entwickeln
* [ ] Git-Workflow definieren
* [ ] Nginx konfigurieren

### Phase 2 – Containerisierung

* [ ] Dockerfile erstellen
* [ ] Docker Image bauen
* [ ] Container testen
* [ ] Docker Compose integrieren

### Phase 3 – CI/CD

* [ ] Build automatisieren
* [ ] Tests automatisieren
* [ ] Docker Image automatisch bauen
* [ ] Deployment automatisieren

### Phase 4 – Kubernetes

* [ ] Kubernetes-Manifeste erstellen
* [ ] Deployment konfigurieren
* [ ] Service konfigurieren
* [ ] Ingress konfigurieren
* [ ] Helm integrieren

### Phase 5 – Production Readiness

* [ ] HTTPS/TLS
* [ ] Monitoring
* [ ] Logging
* [ ] Security Hardening
* [ ] Backup-/Rollback-Strategie
* [ ] Dokumentation finalisieren

---

## 👤 Autor

**[Name]**

Software Engineer | DevOps Enthusiast

### Skills

```text
Java
Spring Boot
Linux
Git
Docker
Docker Compose
Nginx
Kubernetes
Helm
Ansible
CI/CD
```

### Kontakt

* Portfolio: `[URL]`
* GitHub/GitLab: `[URL]`
* LinkedIn: `[URL]`

---

## 📄 Lizenz

[Gewünschte Lizenz eintragen.]

Beispiel:

```text
MIT License
```

---

## ⭐ Projektstatus

```text
Status: In Development
```

> Diese README wird parallel zur technischen Entwicklung des Projekts kontinuierlich aktualisiert.

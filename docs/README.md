# NzARVIS 🤖 – Hybrid AI Assistant

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![Java](https://img.shields.io/badge/Java-17%2B-blue)
![Python](https://img.shields.io/badge/Python-3.9+-yellow)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-CLI%20%7C%20IoT%20%7C%20Docker-lightgrey)

> The future of voice, face, and device control is here—locally built and globally connected.

---

## 🌟 Project Description

**NzARVIS** is a modular, hybrid AI assistant built with a Java-based CLI core that routes commands to intelligent microservices running in Docker. It features:

- 📸 Face recognition using OpenCV
- 🎙️ Voice interaction with Whisper STT & TTS
- ☁️ Global chatbot intelligence via OpenAI
- 🔌 IoT device control via MQTT (ESP32, BLE, serial)
- 🐳 Fully containerized deployment using Docker Compose

From natural language queries to real-time hardware control, NzARVIS bridges human input with smart automation.

---

## 📦 Requirements

| Component         | Tool                        |
|------------------|-----------------------------|
| Java Backend      | Java 17+, Spring Boot       |
| AI Modules        | Python 3.9+, FastAPI, OpenCV |
| Messaging         | Mosquitto MQTT              |
| Containerization  | Docker & Docker Compose     |
| Dev Tools         | IntelliJ IDEA, VS Code      |

> See [`docs/onboarding.md`](./docs/onboarding.md) for full installation instructions.

---

## 🚀 Quick Start

>NzARVIS/
├── microservices/
│   ├── cli-engine/         # Java CLI core
│   ├── iot-controller/     # Java: MQTT, Serial, BLE
│   ├── face-recognizer/    # Python: OpenCV + Dlib
│   ├── voice-assistant/    # Python: Whisper, TTS
│   └── chat-nlp/           # Python: OpenAI chatbot
├── common/                 # Shared config, schemas, utils
├── deployment/             # Docker Compose, K8s manifests
├── docs/                   # Architecture & onboarding docs
└── README.md




---

## 🚀 Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/your-username/NzARVIS.git
cd NzARVIS

# 2. Start core services (MQTT, Python modules)
docker-compose up -d

# 3. Run Java CLI engine
cd microservices/cli-engine
mvn spring-boot:run


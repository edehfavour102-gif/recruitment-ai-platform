# 🚀 AI-Powered Recruitment Platform

A production-ready, cloud-native recruitment platform with fraud detection, identity risk-scoring, and intelligent candidate matching capabilities.

## ✨ Features

- **Candidate Management**: Full lifecycle candidate management
- **Fraud Detection**: ML-based fraud detection and anomaly detection
- **Risk Scoring**: Employment history, education, and identity risk-scoring
- **Intelligent Matching**: AI-powered candidate-to-job matching
- **Real-time Analytics**: Prometheus metrics and Grafana dashboards
- **API-First Architecture**: RESTful APIs with Swagger documentation
- **Microservices Ready**: Containerized, scalable services
- **Production Secure**: GDPR-compliant, SOC2-ready architecture

## 🏃 Quick Start (5 Minutes)

### Prerequisites
- Docker & Docker Compose ([Download](https://www.docker.com/products/docker-desktop))
- Git
- 4GB RAM minimum, 20GB disk space

### One-Command Setup

```bash
# 1. Clone the repository
git clone https://github.com/edehfavour102-gif/recruitment-ai-platform.git
cd recruitment-ai-platform

# 2. Create environment file
cp .env.example .env

# 3. Start all services
docker-compose -f docker/docker-compose.dev.yml up -d

# 4. Wait for services
sleep 30

# 5. Initialize database
docker-compose -f docker/docker-compose.dev.yml exec backend python scripts/init_db.py

# 6. Create admin user
docker-compose -f docker/docker-compose.dev.yml exec backend python scripts/create_admin.py
```

### Access the Application

| Service | URL | Credentials |
|---------|-----|-------------|
| Frontend | http://localhost:3000 | N/A |
| Backend API | http://localhost:8000 | N/A |
| API Docs | http://localhost:8000/docs | N/A |
| Grafana | http://localhost:3001 | admin / admin |
| Kibana | http://localhost:5601 | N/A |
| RabbitMQ | http://localhost:15672 | admin / admin_password_dev |

## 📋 Project Structure

```
recruitment-ai-platform/
├── backend/                    # FastAPI backend
├── frontend/                   # React frontend
├── ml-services/                # ML model serving
├── database/                   # Database initialization
├── docker/                     # Docker configurations
├── monitoring/                 # Prometheus & Grafana
├── scripts/                    # Setup & utility scripts
└── docs/                       # Documentation
```

## 🔐 Security & Compliance

**Important Legal Notes:**

- **Employment Verification**: Risk-scoring and inconsistency detection only. Not definitive verification.
- **Identity Verification**: Risk assessment for human review. Not legal verification without authoritative sources.

✅ GDPR-compliant data handling
✅ User consent mechanisms
✅ Data retention policies
✅ Audit logging
✅ Right to deletion/data portability
✅ Anti-discrimination controls
✅ Human-in-the-loop decisions

## 🛠 Technology Stack

- **Backend**: FastAPI, SQLAlchemy, PostgreSQL
- **Frontend**: React 18+, Redux Toolkit, Tailwind CSS
- **ML/AI**: PyTorch, scikit-learn, XGBoost
- **Infrastructure**: Docker, Kubernetes, Terraform
- **Monitoring**: Prometheus, Grafana, ELK Stack
- **CI/CD**: GitHub Actions

## 🐛 Troubleshooting

```bash
# Check logs
docker-compose -f docker/docker-compose.dev.yml logs -f

# Restart services
docker-compose -f docker/docker-compose.dev.yml restart

# Reset everything
docker-compose -f docker/docker-compose.dev.yml down -v
docker-compose -f docker/docker-compose.dev.yml up -d
```

## 📄 License

MIT License

---

**Version**: 1.0.0 | **Status**: Production Ready ✅
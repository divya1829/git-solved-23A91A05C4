# System Architecture

## Overview
DevOps Simulator follows a microservices architecture designed for high availability, scalability, and flexible development.

---

## Components

### 1. Application Server
- **Technology**: Node.js + Express  
- **Production Port**: 8080  
- **Development Port**: 3000 (with hot reload)  
- **Scaling**:  
  - Production → Horizontal auto-scaling enabled  
  - Development → Manual, single instance  
- **Debug**: Chrome DevTools on port 9229 (development only)

---

### 2. Database Layer
- **Database**: PostgreSQL 14  
- **Production Configuration**: Master-slave replication  
- **Development Configuration**: Single local instance (no replication)  
- **Backup**:  
  - Production → Daily automated backups  
  - Development → Manual backups only  
- **Seeding**: Auto-seed with test data on startup (development only)

---

### 3. Monitoring System
- **Tool**: Prometheus + Grafana  
- **Metrics**: CPU, Memory, Disk, Network, Build time  
- **Alerts**:  
  - Production → Email notifications for critical issues  
  - Development → Console warnings only  
- **Dashboard**: In-development web dashboard (development only)

---

### 4. Container Orchestration (Development Only)
- **Tool**: Docker Compose  
- **Services**: App, Database, Redis cache  
- **Volume Mounts**: Code directory for hot reload  

---

### 5. Authentication System
- **Method**: OAuth2 + JWT  
- **Providers**: Google, GitHub (for testing)  
- **Sessions**: Redis-based session storage  

---

## Deployment Strategy
- **Production**: Rolling updates with zero downtime and automatic rollback on failure  
- **Development**: Docker Compose hot reload; rollback via Git checkout  

---

## Security
- **Production**:  
  - SSL/TLS encryption  
  - Database connection encryption  
  - Regular security audits  
- **Development**:  
  - SSL/TLS disabled  
  - Database credentials in plain text  
  - CORS enabled for all origins  
  - Debug endpoints exposed  

---

## Experimental Features (Development Only)
⚠️ *These features are currently experimental and under testing:*  
- Multi-cloud deployment  
- AI-powered log analysis  
- Automatic rollback on anomaly detection  

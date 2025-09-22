---
title: Arquitetura Geral
description: Visão completa da arquitetura técnica do MedPay Saúde
---

# Arquitetura Geral do Sistema

A arquitetura do MedPay Saúde foi projetada para ser altamente escalável, segura e modular, utilizando as melhores práticas de desenvolvimento de software moderno.

## Diagrama de Arquitetura

```mermaid
graph TD
    %% Frontend Layer
    subgraph "Frontend Layer - React/Next.js"
        A[📱 App Paciente<br/>PWA Mobile-First]
        B[💼 Dashboard Prestador<br/>Clínicas/Hospitais]
        C[⚙️ Painel Admin<br/>Backoffice]
    end

    %% API Gateway
    D[🚪 API Gateway<br/>Load Balancer + Auth]

    %% Backend Microservices
    subgraph "Backend Microservices - Node.js"
        E[👤 User Service<br/>Autenticação/Usuários]
        F[💳 Payment Service<br/>Transações/Parcelamento]
        G[🏥 Provider Service<br/>Clínicas/Procedimentos]
        H[📊 Analytics Service<br/>Relatórios/Métricas]
        I[🔔 Notification Service<br/>Alertas/Comunicação]
        J[🤖 AI Service<br/>Anti-Fraude/Chatbot]
    end

    %% Database Layer
    subgraph "Database Layer"
        K[(🗃️ PostgreSQL<br/>Dados Transacionais)]
        L[(📋 MongoDB<br/>Logs/Analytics)]
        M[⚡ Redis<br/>Cache/Sessions]
    end

    %% External Integrations
    subgraph "Integrações Externas"
        N[💰 Celcoin Gateway<br/>Split Payment/Escrow]
        O[✍️ ClickSign<br/>Assinatura Digital]
        P[🏥 Helena CRM<br/>Sistema Médico]
        Q[🏥 NinSaúde<br/>ERP Saúde]
        R[🏦 APIs Bancárias<br/>PIX/Boleto/TED]
        S[📋 Receita Federal<br/>Validação CPF/CNPJ]
    end

    %% Infrastructure
    subgraph "Infraestrutura AWS"
        T[☁️ CloudFront CDN]
        U[🔒 WAF Security]
        V[📊 CloudWatch<br/>Monitoramento]
        W[💾 S3 Storage<br/>Documents/Backups]
    end

    %% Connections
    A --> D
    B --> D
    C --> D
    D --> E
    D --> F
    D --> G
    D --> H
    D --> I
    D --> J
    E --> K
    F --> K
    G --> K
    H --> L
    I --> M
    J --> L
    F --> N
    G --> O
    G --> P
    G --> Q
    F --> R
    E --> S
```

## Camadas da Arquitetura

### 🎨 Frontend Layer
**Tecnologia:** React 18 + Next.js
- **App Paciente:** Interface mobile-first para pacientes
- **Dashboard Prestador:** Painel para clínicas e hospitais
- **Painel Admin:** Interface de administração do sistema

### 🚪 API Gateway
**Função:** Ponto único de entrada para todas as APIs
- Load balancing automático
- Autenticação e autorização centralizadas
- Rate limiting e proteção contra ataques

### 🔧 Backend Microservices
**Arquitetura:** Microserviços em Node.js
- **User Service:** Gestão de usuários e autenticação
- **Payment Service:** Processamento de pagamentos e parcelamentos
- **Provider Service:** Gestão de clínicas e procedimentos
- **Analytics Service:** Relatórios e métricas
- **Notification Service:** Sistema de alertas e comunicação
- **AI Service:** Anti-fraude e funcionalidades inteligentes

### 🗄️ Database Layer
**Tecnologias:** PostgreSQL, MongoDB, Redis
- **PostgreSQL:** Dados transacionais estruturados
- **MongoDB:** Logs, analytics e dados não estruturados
- **Redis:** Cache de sessão e dados temporários

### 🔗 External Integrations
**Integrações Estratégicas:**
- **Celcoin:** Gateway de pagamento com split payment
- **ClickSign:** Assinatura digital de contratos
- **Helena/NinSaúde:** Sistemas médicos existentes
- **APIs Bancárias:** PIX, boleto, TED
- **Receita Federal:** Validação de documentos

### ☁️ Infrastructure AWS
**Serviços Utilizados:**
- **CloudFront:** CDN para distribuição global
- **WAF:** Web Application Firewall
- **CloudWatch:** Monitoramento e alertas
- **S3:** Armazenamento de documentos e backups